### task
Given an array A , of N integers, print A's elements in reverse order as a single line of space-separated numbers.

## Sample Input
```
4
1 4 3 2
```

## Sample Output
```
2 3 4 1
```
## Code
```
#include <iostream>
using namespace std;
int main()
{
    int *ptr,no,i,temp;
    cin>>no;
    ptr= new int[no];
    for(i=0;i<no;i++)
        cin>>ptr[i];
    for(i=0;i<no/2;i++)
    {
        temp=ptr[no-1-i];
        ptr[no-1-i]=ptr[i];
        ptr[i]=temp;            
    }    
    for(i=0;i<no;i++)
        cout<<ptr[i]<<" ";
    return 0;
}

```
