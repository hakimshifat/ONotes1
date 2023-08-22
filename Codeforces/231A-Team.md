
```
#include<stdio.h>
int main()
{
    int i,j,k,l,m,sum=0;
    scanf("%d",&i);
    for(m=1;m<=i;m++){

    scanf("%d %d %d",&j, &k, &l);
    if(j==1){
        if((k==1) || (l==1)) {
            sum=sum+1;
        }
        else
        {
            sum=sum+0;
        }
    }

       else if(k==1){
        if((j==1) || (l==1)) {
            sum=sum+1;
        }
        else
        {
            sum=sum+0;
        }
    }

        else if(l==1){
        if((k==1) || (j==1)) {
            sum=sum+1;
        }
        else
        {
            sum=sum+0;
        }
    }
    else{
        sum=sum+0;
    }

    }
    printf("\n%d",sum);
    return 0;
}


```