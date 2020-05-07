### Task

Given a string S, of length N that is indexed from 0 to N-1, 
print its even-indexed and odd-indexed characters as 2 space-separated strings on a single line.

## Sample Input
```
2
Hacker
Rank
```
## Sample Output
```
Hce akr
Rn ak
```
## Code
```
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
#include <string>
using namespace std;

int main()
 {
    int T;
    cin>>T;
    while(T--)
    {
        string s;
        cin>>s;
        for(int i=0;s[i];i+=2)
            cout<<s[i];
         cout<<" ";
        for(int i=1;s[i];i+=2)
        cout<<s[i];
        cout<<endl;
        s='\0';
    }
    return 0;
}
```
