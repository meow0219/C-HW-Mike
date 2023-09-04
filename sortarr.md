```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

void sw(int*, int*);

int main() {
    int a[5] = { 2,3,5,4,1 };
    for (int i = 0;i < sizeof(a)/sizeof(int) - 1;i++) {
        for (int j = 0;j < sizeof(a) / sizeof(int) - i - 1;j++) {
            if (a[j] < a[j + 1]) {               
                sw(&a[j], &a[j + 1]);
            }
        }
    }
    for (int i = 0;i < sizeof(a) / sizeof(int);i++) {
        printf("%d", a[i]);
    }
    return 0;
}

void sw(int* a, int* b) {
    int temp = *a;
    *a = *b;
    *b = temp;
}
