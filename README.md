![](https://i.imgur.com/FL9JPy6.png)
```c
#include <stdio.h>
int a[5]={0,10,20,30,40};
int main()
{
    int *p=&a[2];
    *p=222;
    
    p+=2;
    *p=666;
}
```
![](https://i.imgur.com/FUzXYNX.png)

```c
#include <stdio.h>
int a[5]={0,10,20,30,40};
void printAll()
{
    for(int i=0; i<5; i++)
    {
        printf("%d", a[i]);
    }
    printf("\n");
}
int main()
{
    int *p=&a[2];
    *p=222;
    printAll();
    
    p+=2;
    *p=666;
    printAll();
    
    p--;
    *p=555;
    printAll();
}
```
![](https://i.imgur.com/3cct5MQ.png)

```c
#include <stdio.h>
int a[5]={0,10,20,30,40};
void printAll()
{
    for(int i=0; i<5; i++)
    {
        printf("%d", a[i]);
    }
    printf("\n");
}
int main()
{
    int *p=&a[2];
    *p=222;
    printAll();
    
    int *p2=p+4;
    p2=666;
    printAll();
    
    p2--;
    *p2=555;
    printAll();
    
    return 0;
}
```
![](https://i.imgur.com/JZluJn0.png)

```c
#include <stdio.h>
#include <stdlib.h>

int a[10];
int main()
{
    int b[10];
    
    int *p=(int*)malloc(sizeof(int)*10);
    
    return 0;
}
```