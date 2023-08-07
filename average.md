2-1
```c
#include <stdio.h>
int main() {
    int input;
    float sum = 0, x = 0;
    int count = 0;
    scanf_s("%d", &input);

    while (input >=0)
    {
        sum += input;
        count += 1;
        x = sum / count;
        printf("averge: %f, (input < 0 to exit)\n", x);
        scanf_s("%d", &input);
    }
    return 0;
}
```
2-2
```c
#include <stdio.h>
int main() {
    int input;
    float sum = 0, x = 0;
    int count = 0;

    while (scanf_s("%d", &input)!=EOF)
    {
        sum += input;
        count += 1;
        x = sum / count;
        printf("averge: %f, (EOF to exit)\n", x);
    }
    return 0;
}
```
