1. UVA10226 Hardwood species 

```C
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
char line[1000];
char tree[1000000][32];
int compare( const void*p1 , const void*p2)
{
	return strcmp( (char*)p1,(char*)p2);
}
int main()
{
	int T;
	scanf("%d\n\n",&T);
	
	for(int t=0; t<T ;t++)
	{
		int N=0;
		while( gets(line)!=NULL )
		{
			if( strcmp(line,"")==0) break;
			
			strcpy(tree[N],line);
			N++;
			
		}
		if(t>0) printf("\n");
		int ans=1;
	
		qsort( tree , N ,32 ,compare);
		printf("%s ",tree[0]);
		for(int i=0;i<N-1;i++)
		{
			if( strcmp(tree[i],tree[i+1])==0)
			{
				ans++;
			}
			else
			{
				printf("%.4f\n",100*ans/(float)N);
				ans=1;
				printf("%s ",tree[i+1]);
			}
		}
		printf("%.4f\n",100*ans/(float)N);
	}
}
```
2.進階題：最大公因數gcd : 輸入二整數 a b，輸出a b最大公因數 

```C
#include <stdio.h>
int main()
{
	int a,b,ans;
	printf("Enter two integers: \n");
	scanf("%d%d",&a,&b);
	if(a>b)
	{
		for(int i=1;i<=b;i++)
		{
			if(a%i==0 && b%i==0) 
			ans=i;
		}
		printf("The greatest common divisor of %d and %d is %d\n",a,b,ans);
	}
	else if(a<b)
	{
		for(int i=1;i<=a;i++)
		{
			if(a%i==0 && b%i==0)
			ans=i;
		}
		printf("The greatest common divisor of %d and %d is %d\n",a,b,ans);
	}
	
}
```
3.進階題：字串長度 : 輸入兩個很大的正整數a與 b，如果a>b則輸出 1，如果 a<b則輸出 -1, 如果 a=b 則輸出 0。 (暗示：可用字串輸入，用字串的觀點來比大小。) 

```C
#include <stdio.h> 
#include <string.h>
 int main()
 {
 	char a[100],b[100];
 	scanf("%s %s",a,b);
 	
 	int lena,lenb;
 	lena=strlen(a);
 	lenb=strlen(b);
 	if(lena>lenb) printf("1");
 	else if(lena<lenb) printf("-1");
 	else {printf("%d",strcmp(a,b));}
 }

```
4.進階題：函數判斷質數 : 設計一個函數prime(n)，可以判斷n是否為質數：如果是質數則回傳1，否則回傳0。 

```C
#include <iostream>
using namespace std;
int prime(int n)
{
	int ans=0;
	for(int i=1;i<n;i++)
	{
		if(n%i==0) ans++;
	}
	if(ans==1) return 1;
	else return 0;
}
int main(){
  int n;cin>>n;
  cout<<"["<<prime(n)<<"]";
  return 0;
}
/*
int main(void){
    int n;
    scanf("%d", &n);
    printf("[%d]", prime(n));
    return 0;
}
*/
```
5.進階題：判斷迴文 : 讀入一個至多80個字的字串，判斷字串是否為迴文(即由左而右，由右而左，順序相同，大小寫字母視為相異)。如果是迴文則輸出YES，如果不是則輸出NO。 

```C
#include <stdio.h>
#include <string.h>
int main()
{
	char c[81];
	int i;
	int len;
	scanf("%s",&c);
	
	len=strlen(c);
	for(i=0;i<(len/2);i++)
	{
		if(c[i] !=c[len-1-i])
		break;
	}
	if(i==(len/2)) printf("YES");
	else printf("NO");
}
```
