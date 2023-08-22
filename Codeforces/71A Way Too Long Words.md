```
#include<stdio.h>

#include<string.h>

int main()

{

    char i[100];

    int k,j,m;

    scanf("%d",&j);

    for(m=1;m<=j;m++){

    scanf("%s",&i);

    k= strlen(i);

    if (k>10){

    printf("%c%d%c\n",i[0],k-2,i[k-1]);

    }

    else

        printf("%s\n",i);

    }

    return 0;

}

```