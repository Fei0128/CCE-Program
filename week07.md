1.進階題：迴文判斷 : 題目內容：從鍵盤讀入1個4位數的整數(1000-9999)。如果該數字構成廻文(即由左而右，由右而左，順序相同)，則顯示YES。如果該數字未構成廻文，則顯示NO。 
```C
#include <stdio.h>
#include <string.h>
int main()
{
	int i;
	char a[4];
	scanf("%s",&a);
	
	int len=strlen(a);
	for(i=0;i<(len/2);i++)
	{
		if(a[i]!=a[len-1-i]) break;	
	}
	if(i==(len/2)) printf("YES\n");
	else printf("NO\n");
	
	
	
	
	
}
```
2. 進階題：函數反序排列數字 : 設計一個函數f(n)，該函數可以傳回整數n的數字反序排列所組成的整數。 
數字範圍：整數 1 – 9999 (不含10的倍數)  
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
	int n;
	scanf("%d",&n);
	printf("%d%\n",f(n));
}
```

3.進階題：陣列找出現次數 : 讀入一個正整數的數列(逐一輸入正整數，輸入0表示結束，數列至多包含10個整數)，之後再讀入一個正整數，程式可以找出該整數出現在數列中的次數。 
數字範圍：正整數 1 – 9  
```C
#include <stdio.h>
int main()
{
	int a[10];
	int n,ans=0,r=0;
	for(int i=0;i<10;i++)
	{
		scanf("%d",&a[i]);
		if(a[i]==0) break;
		r++;
	}
	scanf("%d",&n);
	for(int i=0;i<r;i++)
	{
		if(a[i]==n) ans++;
	}
	printf("%d\n",ans);
}
```

4.進階題：判斷大小 : 寫一方法能傳入2個整數，如果第一個數字比第二個數字小，則回傳-1;如果兩個數字相等，則回傳0; 如果第一個數字比第二個數字大，則回傳1。印出比較後的結果。  
```C
#include <stdio.h>
int f(int a,int b){
	if(a<b) return -1;
	else if(a==b)return 0;
	else return 1;
}
int main(){
    int a, b;
    scanf("%d %d", &a, &b);
    printf("%d",f(a,b));
    return 0;
}
```
5.進階題：計算一列整數的總和 : 請撰寫一個程式計算並印出數個整數的加總。假設以999當成警示值。 
```C
#include <stdio.h>
int main()
{
	printf("Enter an integer ( 999 to end ): \n");
	int n;
	scanf("%d",&n);
	int ans=0;
	while(n!=999)
	{
		ans=ans+n;
		printf("Enter an integer ( 999 to end ): \n");
		scanf("%d",&n);
	}
	printf("The total is: %d",ans);
}
```

