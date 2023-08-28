```c
void merge(int* nums1, int nums1Size, int m, int* nums2, int nums2Size, int n){
    int i=0;
    int j=0;
    int nums3[m+n];
    while(i<m && j<n){
        if(nums1[i]<nums2[j]){
            nums3[i+j]=nums1[i];
            i++;
        }
        else{
            nums3[i+j]=nums2[j];
            j++;
        }
    }
    while(i<m){
        nums3[i+j]=nums1[i];
        i++;
    }
    while(j<n){
        nums3[i+j]=nums2[j];
        j++;
    }
    for(int k=0;k<m+n;k++){
        nums1[k]=nums3[k];
    }
}
