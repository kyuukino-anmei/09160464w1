# 【第１題】SOIT106_ADVANCE_002：進階題：分式化簡 
```C
#include <stdio.h>
int main()
{
	int x, y, X, Y;
	scanf("%d%d", &x, &y);
	
	for(int i=2; i<=x; i++) 
	{
		if(x%i==0 && y%i==0)
		{
			X=x/i;
			Y=y/i;
		}
	}
	
	printf("%d %d\n", X, Y);
}
```

# 【第２題】SOIT106_ADVANCE_003：進階題：讀入整數反序列印
```C
#include <stdio.h>
int a[10];
int main()
{
	int c=-1;
	for(int i=0; i<10; i++) 
	{
		scanf("%d", &a[i]);
		if(a[i]!=0) c++;
		else break;
	}
	for(int i=c; i>=0; i--) printf("%d ", a[i]);
	printf("\n");
}
```

# 【第３題】SOIT106_ADVANCE_005_C：進階題：A的B次方函數
```C

```

# 【第４題】SOIT106_ADVANCE_006：進階題：漸增數列相加 
```C

```

# 【第５題】SOIT106_BASE_002：基礎題：找零錢 
```C

```

# 【第６題】SOIT106_BASE_005：基礎題：因數個數 
```C

```

# 【第７題】SOIT106_BASE_010：基礎題：找倍數 
```C

```

# 【第８題】SOIT106_BASE_012：基礎題：整數轉換為等級 
```C

```
