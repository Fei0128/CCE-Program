# CCE-Program
2021/2/26 Work

1.基礎題 找零錢

```C
#include <stdio.h>
int main()
{
  int n;
  scanf("%d",&n);
  
  printf("("%d=50*%d+5*%d+1*%d\n",n,n/50,n%50/5,n%5");
}
```

2.基礎題 因數個數

```C
#include <stdio.h>
int main()
{
  intn,m=0;
  scanf("%d",&n);
  
  for(int i=1;i<=n;i++)
  {
    if(n%i==0) m=m+1;
  }
  printf("%d",m);
}
```
