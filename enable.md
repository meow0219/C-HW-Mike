```c
int main() {
    int fun1 = true, fun2 = false;
    int a[] = { fun1,fun2 };
    for (int i = 0;i < 2;i++) {

        if (a[i] == 1) {
            printf("fun%d is enable\n", i+1);
        }
        else {
            printf("fun%d is disable\n", i+1);
        }
    }
    return 0;
}
```
