![](https://i.imgur.com/pUvhkzr.png)

```c    
#include <stdio.h>
#include <stdlib.h>
char *line=(char*)malloc(32*sizeof(char));
int main()
{
	int n;
	scanf("%d\n", &n);
	
	for(int i=0; i<n; i++)
	{
		gets(line);
		printf("%s\n", line);
	}
}
```
![](https://i.imgur.com/Ba2bbyD.png)
```c
#include <stdio.h>
#include <stdlib.h>
char *line=(char*)malloc(32*sizeof(char));
int main()
{
	int n;
	scanf("%d\n", &n);
	
	for(int i=0; i<n; i++)
	{
		gets(line);
		for(int k=0; line[k]!=0; k++)
		{
			char x=line[k];
			if(x>='A' && x<='Z') printf("大");
			else if(x>='a' && x<='z') printf("小");
			else printf("他");
		}
	}
}
```
![](https://i.imgur.com/vMjJXWF.png)
```c
#include <stdio.h>
#include <stdlib.h>
char *line=(char*)malloc(32*sizeof(char));
int ans[26];
int main()
{
	int n;
	scanf("%d\n", &n);
	
	for(int i=0; i<n; i++)
	{
		gets(line);
		for(int k=0; line[k]!=0; k++)
		{
			char x=line[k];
			if(x>='A' && x<='Z') ans[x-'A']++;
			else if(x>='a' && x<='z') ans[x-'a']++;
		}
	}
	
	for(int i=0; i<26; i++)
	{
		printf("%c %d\n", 'A'+i, ans[i]);
	}
}
```
![](https://i.imgur.com/DIuBoZM.png)
```c
#include <stdio.h>
#include <stdlib.h>
char *line=(char*)malloc(32*sizeof(char));
int ans[26];
char letter[]="ABCDEFGHIJKLMNOPQRSTUVWXYZ";
int main()
{
	int n;
	scanf("%d\n", &n);
	
	for(int i=0; i<n; i++)
	{
		gets(line);
		for(int k=0; line[k]!=0; k++)
		{
			char x=line[k];
			if(x>='A' && x<='Z') ans[x-'A']++;
			else if(x>='a' && x<='z') ans[x-'a']++;
		}
	}
	
	for(int i=0; i<26; i++)
	{
		for(int k=i+1; k<26; k++)
		{
			if(ans[i]<ans[k] || (ans[i]==ans[k] && letter[i]>letter[k]))
			{
				int t=ans[i];
				ans[i]=ans[k];
				ans[k]=t;
				
				char x=letter[i];
				letter[i]=letter[k];
				letter[k]=x;
			}
		}
	}
	
	for(int i=0; i<26; i++)
	{
		if(ans[i]>0) printf("%c %d\n", letter[i], ans[i]);
	}
}
```
![](https://i.imgur.com/5EWZ07C.png)
```c
#include <stdio.h>
#include <stdlib.h>
char *line=(char*)malloc(32*sizeof(char));
typedef struct
{
	int ans;
	char x;
}BOX;
BOX array[26];
int compare(const void *p1, const void *p2)
{
	if(((BOX*)p1)->ans > ((BOX*)p2)->ans) return -1;
	else if(((BOX*)p1)->ans < ((BOX*)p2)->ans) return +1;
	else if(((BOX*)p1)->x < ((BOX*)p2)->x) return -1;
	else if(((BOX*)p1)->x > ((BOX*)p2)->x) return +1;
	else return 0;
}
int main()
{
	for(int i=0; i<26; i++) array[i].x='A'+i;
	
	int n;
	scanf("%d\n", &n);
	
	for(int i=0; i<n; i++)
	{
		gets(line);
		for(int k=0; line[k]!=0; k++)
		{
			char x=line[k];
			if(x>='A' && x<='Z') array[x-'A'].ans++;
			else if(x>='a' && x<='z') array[x-'a'].ans++; 
		}
	}
	
	qsort(array, 26, sizeof(BOX), compare);
	
	for(int i=0; i<26; i++) if(array[i].ans>0) printf("%c %d\n", array[i].x, array[i].ans);
}
```

