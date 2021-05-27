Processing :

1.點擊畫面變色並己算點擊次數
```C
void setup(){
  size(1024,400);
}
void draw(){
  if(mousePressed) background(255,0,255);
  else background(15,162,249);
  textSize(50);
  text(a,100,100);
}
int a=0;
void mousePressed(){
a++;
}
```
2.倒數計時器
```C
void setup(){
  size(1024,400);
  text(creatFont("標楷體"50));
}
void draw(){
  background(#319EE5);
  textSize(50);
  int h=hour();
  int m=minunte()
  int s=secend();
  fill(255,0,0);
  text("Now:" + h + ":" + m + ":" + s ,100,100);
  int total= h*60*60+m*60+s;
  text(total,100,200);
  
  int total12=13*60*60+30*60+0;
  int ans = total12-total; //還剩多久
  int ss = ans%60;
  int mm = ans/60%60;
  int hh = ans/60/60%60;
  
  text("剩下" + hh + ":" + mm + ":" + ss ,100,300);
  text("剩下" + nf(hh,2) + ":" + nf(mm,2) + ":" + nf(ss,2) ,100,350)
}
```
