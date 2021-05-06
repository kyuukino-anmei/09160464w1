![](https://i.imgur.com/Q7H2ncV.png)
```c
#include <stdio.h>
typedef struct data
{
    char c;
    int ans;
}DATA;
DATA listA;
int main()
{
    listA.c='A';
    listA.ans=1;
    printf("%c %d\n", listA.c, listA.ans);
}

```
![](https://i.imgur.com/xIavWlB.png)
```c
#include <stdio.h>
typedef struct data
{
    char c;
    int ans;
}DATA;
DATA listA;
int main()
{
    listA.c='A';
    listA.ans=1;
    printf("%c %d\n", listA.c, listA.ans);
}
```
![](https://i.imgur.com/mnvJ74c.png)
```c
#include <stdio.h>
#include <stdlib.h>
int compare(const void *p1, const void *p2)
{
    int d1=*((int*)p1);
    int d2=*((int*)p2);
    if(d1>d2) return 1;
    if(d1==d2) return 0;
    if(d1<d2) return -1;
}
int a[10]={4,8,3,2,5,7,9,1,6,10};
int main()
{
    qsort(a, 10, sizeof(int), compare);

    for(int i=0; i<10; i++)
    {
        printf("%d ", a[i]);
    }
}
```
![](https://i.imgur.com/ifoZpQb.png)
```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
char kuni[2000][80];
char hoka[80];
int compare(const void *p1, const void *p2)
{
	return strcmp((char*)p1, (char*)p2);
}
int main()
{
	int n;
	scanf("%d", &n);
	
	for(int i=0; i<n; i++)
	{
		scanf("%s", kuni[i]);
		gets(hoka);
	}
	
	qsort(kuni, n, 80, compare);
	
	int ans=1;
	printf("%s ", kuni[0]);
	for(int i=0; i<n-1; i++)
	{
		if(strcmp(kuni[i], kuni[i+1])==0) ans++;
		else 
		{
			printf("%d\n", ans);
			printf("%s ", kuni[i+1]);
			ans=1;
		}
	}
	printf("%d\n", ans);
}
```
![](https://i.imgur.com/4oB9R3P.png)
```c
#include <stdio.h>
char line[1001];
int main()
{
	for(int t=0; gets(line)!=NULL; t++)
	{
		if(t>0) printf("\n");
		printf("blahblah");
		printf("blahblah");
		printf("blahblah");
	}
}
```
![](https://i.imgur.com/b5Smnro.png)
```c
#include <stdio.h>
char line[1001];
int ans[256];
int main()
{
	for(int t=0; gets(line)!=NULL; t++)
	{
		for(int i=0; i<256; i++) ans[i]=0;
		
		for(int i=0; line[i]!=0; i++)
		{
			char c=line[i];
			ans[c]++;
		}
		
		if(t>0) printf("\n");
		
		for(int i=0; i<256; i++) if(ans[i]>0) printf("%d %d\n", i, ans[i]);
		
	}
}
```
