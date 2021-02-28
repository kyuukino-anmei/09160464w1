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
#include <stdio.h>
int MYPOWER(int a, int b)
{
	int x=1;
	for(int i=0; i<b; i++) 
	{
		x*=a;
		
	}
	return x;	
}
int main(void)
{
	int a,b;
	scanf("%d%d",&a,&b);
	printf("[%d]",MYPOWER(a,b));
	return 0;
}
```

# 【第４題】SOIT106_ADVANCE_006：進階題：漸增數列相加 
```C
#include <stdio.h>
int main()
{
	int n ,sum=0, ans;
	scanf("%d", &n);
	
	for(int i=n; i>0; i--)
	{
		ans=i*(i-1);
		sum+=ans;
	}
	printf("%d\n", sum);
}
```

# 【第５題】SOIT106_BASE_002：基礎題：找零錢 
```C
#include <stdio.h>
int main()
{
	int x, a, b, c;
	scanf("%d", &x);
	
	a=x/50;
	b=x%50/5;
	c=x%5;
	
	printf("%d=50*%d+5*%d+1*%d\n", x, a, b, c);
}
```

# 【第６題】SOIT106_BASE_005：基礎題：因數個數 
```C
#include <stdio.h>
int main()
{
	int x, c=0;
	scanf("%d", &x);
	for(int i=1; i<=x; i++)
	{
		if(x%i==0) c++;
	}
	printf("%d\n", c);
}
```

# 【第７題】SOIT106_BASE_010：基礎題：找倍數 
```C
#include <stdio.h>
int main()
{
	int x, c=0;
	for(int i=0; i<10; i++)
	{
		scanf("%d", &x);
		if(x%3==0) c++;
	}
	printf("%d\n", c);
}
```

# 【第８題】SOIT106_BASE_012：基礎題：整數轉換為等級 
```C
#include <stdio.h>
int main()
{
	int x;
	scanf("%d", &x);
	
	if(x>=90) printf("A\n");
	else if(x>=80) printf("B\n");
	else if(x>=60) printf("C\n");
	else printf("F\n");
}
```
