![](https://i.imgur.com/4lbsiMx.png)
```java
void setup()
{
  size(400,200); 
}
void draw()
{
  background(#05DCFF); 
  ellipse(50,50, 80,80);
}
```
![](https://i.imgur.com/cfNVlZt.png)
```java
void setup()
{
  size(400,200); 
}
void draw()
{
  background(#05DCFF); 
  fill(#FF5863);
  ellipse(50,50, 80,80);
  fill(#F7BEC2);
  float stop=mouseX/50.0;
  text(stop, 100,100);
  arc(50,50, 80,80, 0, stop);
}
```
![](https://i.imgur.com/RlJU4ya.png)
```java
void setup()
{
  size(400,200); 
}
void draw()
{
  background(#05DCFF); 
  fill(#FF5863);
  ellipse(50,50, 80,80);
  fill(#F7BEC2);
  float start=mouseX/50.0;
  text(start, 100,100);
  arc(50,50, 80,80, 0+start, 0.1+start);
}
```
![](https://i.imgur.com/h6XVqtG.png)
```java
void setup()
{
  size(400,200); 
}
void draw()
{
  background(#05DCFF); 
  fill(#FF5863);
  ellipse(50,50, 80,80);
  fill(#F7BEC2);
  float start=mouseX/50.0;
  text(start, 100,100);
  for(int i=0; i<24; i++)
  {
    float shift=2*PI*i/24.0;
    if(i%3==0) fill(#00FF0E);
    if(i%3==1) fill(#FFFFFF);
    if(i%3==2) fill(#000000);
    arc(50,50, 80,80, shift+0+start, shift+0.1+start);
  }
}
```
![](https://i.imgur.com/x4E4vdR.png)
```java
void setup()
{
  size(400,200); 
}
void draw()
{
  background(#05DCFF); 
  fill(#FF5863);
  ellipse(100,100, 180,180);
  fill(#F7BEC2);
  float start=mouseX/50.0;
  text(start, 100,100);
  for(int i=0; i<24; i++)
  {
    float shift=2*PI*i/24.0;
    if(i%3==0) fill(#00FF0E);
    if(i%3==1) fill(#FFFFFF);
    if(i%3==2) fill(#000000);
    if(i==0) fill(#FF8008);
    arc(100,100, 180,180, shift+0+start, shift+PI/12.0+start);
  }
}
```
![](https://i.imgur.com/yPmcllo.png)
```java
void setup()
{
  size(400,200); 
}
float start=0;
void draw()
{
  background(#05DCFF); 
  fill(#FF5863);
  ellipse(100,100, 180,180);
  if(start<10) start+=0.01;
  fill(#F7BEC2); 
  text(start, 200,150);
  for(int i=0; i<24; i++)
  {
    float shift=2*PI*i/24.0;
    if(i%3==0) fill(#00FF0E);
    if(i%3==1) fill(#FFFFFF);
    if(i%3==2) fill(#000000);
    if(i==0) fill(#FF8008);
    arc(100,100, 180,180, shift+0+start, shift+PI/12.0+start);
  }
}
```
![](https://i.imgur.com/aiDkO2E.png)
```java
void setup()
{
  size(400,200); 
}
float start=0, v=0.07;
void draw()
{
  background(#05DCFF); 
  if(v>0.001)
  {
    start+=v;
    v*=0.999;
  }
  fill(#F7BEC2); text(start, 200,150); text(v, 200, 170);
  for(int i=0; i<24; i++)
  {
    float shift=2*PI*i/24.0;
    if(i%3==0) fill(#00FF0E);
    if(i%3==1) fill(#FFFFFF);
    if(i%3==2) fill(#000000);
    if(i==0) fill(#FF8008);
    arc(100,100, 180,180, shift+0+start, shift+PI/12.0+start);
  }
}
```
![](https://i.imgur.com/8nrChGs.png)
```java
void setup()
{
  size(400,200); 
}
float start=0, v;
void draw()
{
  background(#05DCFF); 
  if(v>0.001)
  {
    start+=v;
    v*=0.999;
  }
  fill(#F7BEC2); text(start, 200,150); text(v, 200, 170);
  for(int i=0; i<24; i++)
  {
    float shift=2*PI*i/24.0;
    if(i%3==0) fill(#00FF0E);
    if(i%3==1) fill(#FFFFFF);
    if(i%3==2) fill(#000000);
    if(i==0) fill(#FF8008);
    arc(100,100, 180,180, shift+0+start, shift+PI/12.0+start);
  }
}
void mousePressed()
{
  v=random(1); 
}
```




