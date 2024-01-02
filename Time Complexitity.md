# Constant Time(O1)
## When execution time do not changes every time the code runs.

1. Assignment Operation
2. Mathematical Operation
3. Comparison Operation
4. Function Calling
```C++
#include<bits/stdc++.h>
using namespace std;
int main()
{
    int a,b; 
    cin>>a>>b; 
    int sum= a+b; //2
    sum+=1;//2
    sum+=4;//2
    sum*=4;//2
    cout<<sum<<endl; // theoratically it is always 8/constant
    return 0;
}
```

# Linear Time
## 