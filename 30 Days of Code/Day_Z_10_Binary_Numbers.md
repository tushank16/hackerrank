## Task 
Given a base-10 integer, n, convert it to binary (base-2). Then find and print the base-10 integer denoting the maximum number of consecutive 1's in n's binary representation.


## Sample Input 1
```
5
```
## Sample Output 1
```
1
```
## Sample Input 2
```
13
```
## Sample Output 2
```
2
```
## Code
```
#include <bits/stdc++.h>

using namespace std;

int main()
{
    int n, a[10],i,count, cnt=0;
    cin >> n;
    cin.ignore(numeric_limits<streamsize>::max(), '\n');
    for(i=0; n>0;i++)
    {
        a[i]=n%2;
        n=n/2;
        if(a[i]==0)
        {
            count=0;
        }
        if(a[i]==1)
        {
            count++;
            
            if(cnt<count)
            cnt=count;
            
        }
    }
    if(count>cnt)
    cout<<count<<endl;
    else 
    cout<<cnt<<endl;
    return 0;
}
```
