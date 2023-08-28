```c
#include <stdlib.h>
#include <stdio.h>

int *addArray(int arr1[], int arr2[], int size) {
    int i;
    int *res = (int*)malloc(size*sizeof(int));
    for (i = 0; i < size; i++)
        res[i] = arr1[i] + arr2[i];
    return res;
}

int main() {
    int arr1[] = { 1, 2, 3 };
    int arr2[] = { 9, 8, 7 };

    int *ptr1 = addArray(arr1, arr2, 3);
    printf("ptr1: %d\n", *ptr1);
    free(ptr1);
    // free memory
    return 0;
}
