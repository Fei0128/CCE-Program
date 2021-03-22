進階題：除惡務盡 : 輸入一個字串，將所有字元2去除後輸出。 
```C
#include <stdio.h>
char a[100];
int main()
{
	
	scanf("%s",&a);
	
	int i=0;
	while(a[i]!='\0')
	{
		if(a[i]!='2')
		{
			printf("%c",a[i]);
		}
		i++;
	}
	printf("\n");
}
```
2.進階題：擲骰統計 : 輸入一字串為擲骰的結果，統計1到6點出現的狀況。 
```C
#include <stdio.h>
int main()
{
	char count[7]={0}, a[100];
	scanf("%s",&a);
	int i=0;
	while(a[i]!='\0')
	{
		count[a[i]-'0']++;
		i++;
	}
	for(int i=1;i<=6;i++)
	{
		printf("%d:%d\n",i,count[i]);
	}
}
```
3.進階題：函數找整數的最大數字 : 設計一個函數max_digit(n)，找出組成正整數n中的最大數字，例如：183的最大數字為8。 
```C
#include <stdio.h>
int main()
{
	char a[100];
	scanf("%s",&a);
	
	char ans=a[0];
	int i=0;
	
	while(a[i]!='\0')
	{
		if(a[i] > ans) ans=a[i];
		i++;
	}
	printf("[%c]",ans);
}
```
4.進階題：星星等腰三角 : 輸入1個正整數n，作為輸出星星三角的層數 
```C
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	
	for(int i=0;i<n;i++)
	{
		for(int s=n-i-1;s>0;s--)
		{
			printf(" ");
		}
		
		for(int k=0;k<2*i+1;k++)
		{
			printf("*");
		}
	
		printf("\n");
	}
	
}
```
5.基礎題：分開整數的每個數字 : 撰寫一個程式，輸入一個五位數的數字，將這個數字分成個別的數字，然後分別印出每個數字，數字中間必須相隔3個空格。例如，若輸入42139，則程式必須印出： 4 2 1 3 9  
 ```C
 #include <stdio.h>
#include <string.h>
int main()
{
	char a[5];
	scanf("%s",&a);
	int i=0;
	
	while(i<(strlen(a)-1))
	{
		printf("%c   ",a[i]);
		i++;
	}
	
	printf("%c",a[i]);
	
}
 ```
 6.基礎題：字元判別 : 輸入一個字元，若其為大寫字母則輸出U，若其為小寫字母則輸出L，若其為數字則輸出D，若為其他則輸出O。 
```C
#include <stdio.h>
int main()
{
	char a;
	scanf("%c",&a);
	if('A'<=a && a<='Z')
		printf("U");
	else if('a'<=a && a<='z')
	    printf("L");
	else if('0'<=a && a<='9')
	    printf("D");
	else
		printf("O");
}
```
7.基礎題：數字之首 : 輸入一個整數N，請找出這個數字的首位數。 
```C
#include <stdio.h>
int main()
{
	char a[100];
	scanf("%s",&a);
	printf("%c",a[0]);
}
```
8.基礎題：輸出從0到N的偶數 : 輸入一正整數Ｎ後，利用迴圈概念輸出所有0～N內的偶數 
```C
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	
	
	for(int i=1;i<=n;i++)
	{
		if(i%2==0) printf("%d ",i);
	}
}
```
