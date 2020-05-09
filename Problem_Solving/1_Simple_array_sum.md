### Task
Given an array of integers, find the sum of its elements.
For example, if the array **ar = [1,2,3], 1+2+3 =6 **, so return **6** .

## Sample Input

6
1 2 3 4 10 11

## Sample Output

31

## Code

#include <bits/stdc++.h>
#include <iostream>
using namespace std;

int main()
{
    int n, *ptr,sum=0;
    cin>>n;
    ptr= new int[n];
    for(int i=0;i<n;i++)
    {
        cin>>ptr[i];
        sum=sum+ptr[i];
    }
    cout<<sum;
    return 0;
}

