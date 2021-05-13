1.UAV10082 告訴我頻率簡化版(不用排序)
```C
#include <stdio.h>
char line[2000];
{
  for(int t=0 ; gets(line ; t++)  // 讀資料一次讀一行
  {
    int ans[256]={};  //將出現次數 ans[]歸0
    for(int i=0 ; line[i]!=0 ; i++)
    char c=line[i];
    ans[c]++;  // 計算字母出現次數
    
    if(t>0)  printf("\n");
    for(int i=0 ; i<256 ; i++)  // 輸出資料
    {
      if(ans[i]>0) printf("%d %d\n",i,ans[i]);
    }
  }

}
```
