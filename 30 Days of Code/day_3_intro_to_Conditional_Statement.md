**Task**
* Given an integer n, perform the following conditional actions:
* If n is odd, print Weird
* If n is even and in the inclusive range of 2 to 5, print Not Weird
* If n is even and in the inclusive range of 6 to 20, print Weird
* If n is even and greater than 20, print Not Weird

'''
#include <bits/stdc++.h>
using namespace std;
int main()
{
    int N;
    cin >> N;
    cin.ignore(numeric_limits<streamsize>::max(), '\n');
    /*If n is odd, print Weird*/
    if(N%2!=0)
    {
        printf("Weird");
    }
    /*If n is even and in the inclusive range of 2 to 5, print Not Weird*/
    else if(N%2==0 && 2<=N && N<=5)
    {
        printf("Not Weird");
    }
    /*If n is even and in the inclusive range of 6 to 20, print Weird*/
    else if(N%2==0 && 6<=N && N<=20)
    {
        printf("Weird");
    }
    /*If n is even and greater than 20 , print Not Weird*/
    else if(N%2==0 && N>20)
    {
        printf("Not Weird");
    }
    return 0;
}

'''
