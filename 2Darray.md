```c
#include <stdio.h>
#define X 2
#define Y 3
#define Z 1
void matrix_multiplication_static(int x, int y, int z, int m1[X][Y], int m2[Y][Z], int m3[X][Z])
{
    for (int i = 0;i < x;i++) {
        for (int j = 0;j < z;j++) {
            m3[i][j] = 0;
            for (int k = 0;k < y;k++) {
                m3[i][j] = m3[i][j] + m1[i][k] * m2[k][j];
            }
            printf("%d", m3[i][j]);
        }
        printf("\n");
    }
}
void matrix_multiplication_dynamic(int x, int y, int z, int* m1, int* m2, int* m3)
{
    int i = 0;
    for (int k = 0;k < x * z;k++) {
        int j = 0;
        *(m3 + k) = 0;
        while (j != y) {
            *(m3 + k) = *(m3 + k) + *(m1 + i) * *(m2 + j);
            i++;
            j++;
        }
        printf("%d", *(m3 + k));
        printf("\n");
    }
    printf("\n");         
}
int main()
{
    int m1[X][Y] = { {1, 2, 3}, {4, 5, 6} };
    int m2[Y][Z] = { {1}, {0}, {-1} };
    int m3[X][Z];

    matrix_multiplication_static(X, Y, Z, m1, m2, m3);
    matrix_multiplication_dynamic(X, Y, Z, *m1, *m2, *m3);

    return 0;
}
