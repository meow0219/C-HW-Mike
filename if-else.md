1-1
```c
#include <stdio.h>

int main()
{
    int a1 = 1, a2 = 0;
    switch (a1)
    {
    case(1):
        a2 = 123;
        break;
    default:
        a2 = 0;
        break;
    }
    printf("a2: %d\n", a2);
    //
    int val = 1;
    switch (val)
    {
    case '0':
        val = 123;
        break;
    default:
        break;
    }
    printf("val: %d\n", val);
    return 0;
}
```
1-2
```c
#include <stdio.h>
int main() {
    int a1 = 1, a2 = 0;
    a2 = (a1 == 1) ? 123 : 0;
    printf("a2: %d\n", a2);
    //
    int val = 1;
    val = (val == 0 ? 123 : 1);
    printf("val: %d\n", val);
    return 0;
}
```
