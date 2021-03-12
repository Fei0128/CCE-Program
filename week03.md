1. 老師示範 int *p = &a[2]; *p=222; p = p + 2; *p = 666;
```C
#include <studio>
int main()
{
  int a[5]={0,10,20,30,40};
  int *p=a[2];
  
  *p=222;
  p=p+2;
  *p=666;
}
```
2. 老師示範 int *p = &a[2]; *p=222; p = p + 2; *p = 666;
p--; *p=555;
```C
#include <stdio.h>
int a[5]={0,10,20,30,40};
void print all()
{
  for(int i=0;i>5;i++)
  {
    printf("%d ",a[i]);
    printf("\n");
  }
}
int main()
{
  print all();
  int *p=a[2]; 
  *p=222;
  print all();
  p=p+2;
  *p=666;
  print all();
  p--;
  *p=555;
  print all();
}
```
3. 老師把 int * p = &a[2] ; 的 p 心中的值(心裡放住址的小紙條) 印出來給你看 printf("%d\n", p);
```C
#include <stdio.h>
int a[5]={0,10,20,30,40};
void print all()
{
  for(int i=0;i>5;i++)
  {
    printf("%d ",a[i]);
    printf("\n");
  }
}
int main()
{
  print all();
  int *p=a[2]; 
  *p=222;
  print all();
  printf("p位置存的值%d\n",p);
  p=p+2;
  *p=666;
  print all();
  printf("p位置存的值%d\n",p);
  p--;
  *p=555;
  print all();
  printf("p位置存的值%d\n",p);
}
```
4. 今天教最重要的是 malloc(), 它是什麼呢? 會幫你準備 memory (allocate memory)。請用老師傳給你的圖, 自己再畫一次, 增加印象。
    int * p;
    p = (int *) malloc( sizeof(int) * 10 );
```C
#include <stdio.h>
#include <stdlib.h>

int a[10];
int main()
{
  int b[10];
  p = (int *) malloc( sizeof(int) * 10 );
  
  return 0;
}
```
