### Task 
Write a factorial function that takes a positive integer, N  as a parameter and prints the result of  N!( factorial).

## Sample Input
```
3
```
## Sample Output
```
6
```
## Code

```

#include <iostream>
using namespace std;
int factorial(int n) 
{
    int a;
    if(n>1)
     a= n*(factorial(n-1));
    else 
        return 1; 
    return a;
}
int main()
{
    int n;
    cin >> n;
    cin.ignore(numeric_limits<streamsize>::max(), '\n');
    int result = factorial(n);
    cout << result << "\n";
    return 0;
}
```
