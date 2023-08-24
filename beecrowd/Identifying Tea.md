
```
#include<stdio.h>
int main()
{
    int i,sum=0,j,k,m;
    int p[4];
    scanf("%d",&i);
    m=i;
    for(k=0;k<5;k++){
        scanf("%d",&p[k]);
    }
    for (j=0;j<5;j++){
        if(p[j] == m){
            sum=sum+1;
        }
        else{
            sum=sum+0;
        }
    }
   printf("%d",sum);
    return 0;
}

}

```