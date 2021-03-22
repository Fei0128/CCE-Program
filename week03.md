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
5.進階題：計算陣列的平方值 : 輸入一個整數N，再依序輸入N個整數置於陣列中，計算各元素的平方值，再列出此算出平方值後的陣列。 
數字範圍：整數N範圍 1 – 10；其他整數1 – 100  
```C
#include <stdio.h>
int a[10];
int main()
{
	int n,ans=0;
	scanf("%d",&n);
	for(int i=0;i<n;i++)
	{
		scanf("%d",&a[i]);
		ans=a[i]*a[i];
		printf("%d,",ans);
	}
	printf("\n");
	
}
```
6.進階題：大小寫轉換 : 讀入一個字串(至多10個字元)，將字串中的大小寫英文字母相互轉換(大寫轉為小寫，小寫轉為大寫)後輸出。  
 ```C
 #include <stdio.h>
int a[10];
int main()
{
	int n,ans=0;
	scanf("%d",&n);
	for(int i=0;i<n;i++)
	{
		scanf("%d",&a[i]);
		ans=a[i]*a[i];
		printf("%d,",ans);
	}
	printf("\n");
	
}
7.基礎題：計算幾週與幾天 : 一週有7 天，讀入天數，計算該天數是幾週又幾天。 
數字範圍：整數1 – 365  
```C
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	
	printf("%d %d\n",n/7,n%7);
}
```
8.基礎題：計程車資計算 : 輸入里程公尺數，輸出應付的車資。計程車資計算方式為：起跳100 元(2000公尺)，續跳5元(每500公尺)。 
數字範圍：整數1 – 100000。  
```C
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	
	if(n<2000) printf("100");
	else if(n>2000 && n%500==0)printf("%d",100+(n-2000)/500*5);
	else printf("%d",100+(n-2000)/500*5+5);
	printf("\n");
}
```
9.基礎題：兩數間可被5整除的整數 : 輸入兩個整數，找出兩數之間所有可以被5整除的整數。 
數字範圍：2個整數1 – 10000  
```C
#include <stdio.h>
int main()
{
	int a,b,ans=0;
	scanf("%d%d",&a,&b);
	if(a<b)
	{
		for(int i=a;i<=b;i++)
		{
			if(i%5==0)
			
			printf("%d\n",i);	
		}
	}
	if(a>b)
	{
		for(int i=b;i<=a;i++)
		{
			if(i%5==0)
			
			printf("%d\n",i);	
		}
	}

}
```
10.基礎題：整數間最大距離 : 輸入3個相異整數，找出整數間最大的距離。 
數字範圍：整數1 – 10000  
```C
#include <stdio.h>
int main()
{
	int a,b,c;
	scanf("%d%d%d",&a,&b,&c);
	
	if(a>b && b>c) printf("%d",a-c);
	else if(a>c && c>b) printf("%d",a-b);
	else if(b>a && a>c) printf("%d",b-c);
	else if(b>c && c>a) printf("%d",b-a);
	else if(c>a && a>b) printf("%d",c-b);
	else printf("%d",c-a);
	printf("\n");
}
```
