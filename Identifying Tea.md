Draft:
```
#include<stdio.h>
int main()
{
    int i,sum=0,j,k;
    int p[4];
    scanf("%d",&i);
    for(k=0;k<5;k++){
        scanf(" %d",&p[k]);
    }
    for (j=0;j<5;j++){
        if(i==p[j]){
            sum=sum+1;
            continue;
        }
        else{
            sum=sum+0;
            continue;
        }
    }
    printf("%d",sum);
    return 0;
}

```