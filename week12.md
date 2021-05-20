 1. UVA299 交換火車
 ```C
  #include <stdio.h>
int a[100];
int main()
{
	int T;
	scanf("%d",&T);
	
	for(int t=0;t<T;t++) // 讀資料
	{
		int N;
		scanf("%d",&N);
		for(int i=0;i<N;i++)
		{
			scanf("%d",&a[i]);
		}
		int ans=0;
		for(int k=0;k<N-1;k++)
		{
			for(int i=0;i<N-1;i++) // N-1 因為只能比到倒數第2個(N-1)
			{
				if(a[i]>a[i+1]) // 比大小 泡泡排序法
				{
					int temp = a[i]; 
						a[i] = a[i+1];
						a[i+1] = temp;
						ans++;
				}
			}
		
		}
		printf("Optimal train swapping takes %d swaps.\n",ans);
	
	}
	

}
 ```
 2. UVA10062 Tell me frequencies
 ```C
 #include <stdio.h>
char line[2000];

int main()
{
	for(int t=0 ; gets(line) ; t++) // 讀資料 
	{
		int ans[256]={};
		char c[256]={};
		for(int i=0;i<256;i++) c[i]=i;
		
		for(int i=0;line[i];i++) //計算出現次數
		{
			char c=line[i];
			ans[c]++;
		}
	
		for(int i=0 ; i<256 ;i++)
		{
			for(int j=i+1;j<256;j++)
			{
				if(ans[i]>ans[j]) //右邊數字由小到大排列
				{
					int temp=ans[i]; 
					ans[i]=ans[j];
					ans[j]=temp;
          
					char t=c[i]; 
					c[i]=c[j];
					c[j]=t;
				}
					if(ans[i]==ans[j] && c[i]<c[j]) //右邊數字相等時 左邊由大到小排列
				{
					int temp=ans[i];
					ans[i]=ans[j];
					ans[j]=temp;
					char t=c[i];
					c[i]=c[j];
					c[j]=t;
				}
			}
		}
		if(t>0) printf("\n");
		for(int i =0;i<256;i++)
		{
			if(ans[i]>0) printf("%d %d\n",c[i],ans[i]);
		}
	
	}
	
}
 ```
