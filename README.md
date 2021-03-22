#HW04
![](https://i.imgur.com/8R6hK87.png)
```C
#include <stdio.h>
struct DATA
{
    float x, y, z;
};
int main()
{
    
}
```
![](https://i.imgur.com/4f6Adxt.png)
```C    
#include <stdio.h>
struct DATA
{
    float x, y, z;
} point1;
int main()
{
    point1.x=3;
    point1.y=5;
    point1.z=7;
    printf("%f %f %f\n", point1.x, point1.y, point1.z);
}
```
![](https://i.imgur.com/TNIdkbl.png)
```C 
#include <stdio.h>
struct DATA
{
    float x, y, z;
} point1;
struct DATA points[5];
int main()
{
    for(int i=0; i<5; i++)
    {
        points[i].x=i*10;
        points[i].y=20;
        points[i].z=0;
        printf("%f %f %f\n", points[i].x, points[i].y, points[i].z);    
    }
}
```
![](https://i.imgur.com/jQkNIcf.png)
```C  
#include <stdio.h>
struct DATA
{
    float x, y, z;
} a, b, c;
struct DATA points[5];
int main()
{
    for(int i=0; i<5; i++)
    {
        points[i].x=i*10;
        points[i].y=20;
        points[i].z=0;
        printf("%f %f %f\n", points[i].x, points[i].y, points[i].z);    
    }
}
```
![](https://i.imgur.com/Ihj4qVw.png)
```C   
include <stdio.h>
struct DATA
{
    float x, y, z;
} a, b;
struct DATA c, d;
int main()
{
    struct DATA e;
    struct DATA f={1,2,3};
    
    printf("%f %f %f\n", a.x, a.y, a.z);
    printf("%f %f %f\n", b.x, b.y, b.z);
    printf("%f %f %f\n", c.x, c.y, c.z);
    printf("%f %f %f\n", d.x, d.y, d.z);
    printf("%f %f %f\n", e.x, e.y, e.z);
    printf("%f %f %f\n", f.x, f.y, f.z);
}
```
