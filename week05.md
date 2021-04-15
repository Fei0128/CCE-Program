1.字串排序 :按照字母順序排列
```C
#include <stdio.h>
#include <string.h>
char line[100][10];
int main()
{
	int n;
	scanf("%d",&n);
	
	for(int i=0;i<n;i++)
	{
		scanf("%s",line[i]);
	}
	char temp[10];
	for(int i=0;i<n;i++)
	{
		for(int j=i+1;j<n;j++)
		{
			if(strcmp(line[i],line[j])>0)
			{
				strcpy(temp,line[i]);
				strcpy(line[i],line[j]);
				strcpy(line[j],temp);
			}
		}
	}
	for(int i=0;i<n;i++)
	{
		printf("%s\n",line[i]);
	}
}
```

2.進階題：反序數字 : 輸入1個正整數，將該整數所有數字反序排列後組成一個的新整數，計算出兩者相加的結果。 
數字範圍：整數 1 – 10000  
```C
#include <stdio.h>

int f(int n)
{
	int p;
	int m=0;
	
	while(n>0)
	{
		p=n%10;
		n=n/10;
		m=p+m*10;
	}
	return m;
}

int main()
{
	int n,m;
	scanf("%d",&n);
	printf("%d+%d=%d\n",n,f(m),n+f(m));
}
```

3.進階題：絕對值函數 : 
題目名稱：絕對值函數。
題目內容：設計一個函數f(n)，會回傳n的絕對值。
數字範圍：整數1 – 10000
程式限制：不得使用abs()函數。不得變更已給定的主程式。
主程式：
int main(void)
{
	int n;
	scanf("%d",&n);
	printf("[%d]",f(n));
	return 0;
}
```C
#include <stdio.h>
int f(int n)
{
	if(n<0) return n*(-1);
	else return n;
}
int main(void)
{
	int n;
	scanf("%d",&n);
	printf("[%d]",f(n));
	return 0;
}
```

4.基礎題：N數之和 : 輸入一個整數N，之後讀入N個整數，請輸出其和。 
數字範圍：N=整數1 – 10，其餘整數1 – 100。  
```C
#include <stdio.h>
int main()
{
	int a[10];
	int ans=0,n;
	scanf("%d",&n);
	for(int i=0;i<n;i++)
	{
		scanf("%d",&a[i]);
		ans=ans+a[i];
	}
	printf("%d\n",ans);
}
```

5.基礎題：三數極大 : 輸入三個正整數，輸出其最大值。 
數字範圍：整數1 – 100  
```C
#include <stdio.h>
int main()
{
	int a,b,c;
	scanf("%d%d%d",&a,&b,&c);
	
	if(a>b && a>c) printf("%d\n",a);
	else if(b>a && b>c) printf("%d\n",b);
	else printf("%d\n",c);
}
```

6.基礎題：計算商數 : 輸入兩個整數a，b，輸出a除以b的商。 
數字範圍：整數 1 – 10000  
```C
#include <stdio.h>
int main()
{
	int a,b;
	scanf("%d%d",&a,&b);
	
	printf("%d\n",a/b);
}
```
