```
#include <iostream>
#include <iomanip>
#include <limits>

using namespace std;

int main() 
{
    int i = 4;
    double d = 4.0;
    string s = "HackerRank ";
    int a;
    double b;
    string c;
       // Declare second integer, double, and String variables.
    
    cin>>a>>b;
    cin.ignore();
    getline(cin,c);
    // Read and save an integer, double, and String to your variables.
    // Note: If you have trouble reading the entire string, please go back and review the Tutorial closely.
    
    // Print the sum of both integer variables on a new line.
    
    cout<<i+a<<endl;
    b=b+d;
    // Print the sum of the double variables on a new line.
    //cout<<b<<endl;
    printf("%.1f\n",b);
    // Concatenate and print the String variables on a new line
    cout<<s+c<<endl;
    // The 's' variable above should be printed first.
        return 0;
}
```
OUTPUT:-
![Image][1]
⋮
[1]: https://github.com/tushank16/hackerrank/blob/master/30%20Days%20of%20Code/images/Annotation%202020-05-04%20202215.png
