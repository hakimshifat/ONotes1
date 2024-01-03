Basically Array without size limitation and with a lot of advantages

```C++
#include<bits/stdc++.h>
using namespace std;
int main()
{
    vector<int>v; //declaration

    v.push_back(1);
    v.push_back(2);
    v.push_back(3); //putting values in
    v.push_back(4);//the vector
    v.push_back(5);
    v.push_back(6);
    v.push_back(7);
    cout<<"Printing Entire Vector before using clear() function"<<endl;

    if(v.empty()){
        cout<<"\nThe function is empty"<<endl; //empty() checks if a vector is empty or not
    }
    else{
        cout<<"\n Not empty"<<endl;
    }
    cout<<"\nThe size of the vector is "<<v.size()<<endl;
    for(int i=0; i<v.size(); i++) //v.size() determines size of the vector
    {

        cout<<v[i]<<" and "<< v.at(i) <<endl;
    }
    //Two ways of printing
    // 1.Like array-> v[1] ,will print garbage value if not in range
    // 2. v.at(1) , will show error if not in range

    cout<<"The vector after using pop_back() function.It deletes the last element"<<endl;
    v.pop_back();
    cout<<"\nThe size of the vector "<<v.size()<<endl;
        for(int i=0; i<v.size(); i++) //v.size() determines size of the vector
    {

        cout<<v[i]<<" and "<< v.at(i) <<endl;
    }

    cout<<"Erase() function erases elements from vector.It can be done one by one or more then one"<<endl;
    int e;
    cout<<"Tell the index number of the value you want to delete using erase function"<<endl;
    cin>>e;
    v.erase(v.begin()+e);
            for(int i=0; i<v.size(); i++) //v.size() determines size of the vector
    {

        cout<<v[i]<<" and "<< v.at(i) <<endl;
    }

    int f,g;
    cout<<"Tell the index number of starting and ending you want to delete"<<endl;
    cin>>f>>g;
    v.erase(v.begin()+f,v.begin()+g);
            for(int i=0; i<v.size(); i++) //v.size() determines size of the vector
    {

        cout<<v[i]<<" and "<< v.at(i) <<endl;
    }

    cout<<"\nUse of front() function->"<<"\n "<< v.front() <<" It represent the first element of the vector"<<endl;
    cout<<"\nUse of back() function->"<<"\n "<< v.back() <<" It represent the last element of the vector"<<endl;

    //Empty function clears the vector
    v.clear();
    cout<<"\nThe vector after using clear() function"<<endl;
    cout<<"\nThe size of the vector "<<v.size()<<endl;

        if(v.empty()){
        cout<<"\nThe function is empty"<<endl;
    }
    else{
        cout<<"\n Not empty"<<endl;
    }
    return 0;
}
```
