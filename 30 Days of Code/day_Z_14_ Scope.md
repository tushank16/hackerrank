### Task
Complete the Difference class by writing the following:

* A class constructor that takes an array of integers as a parameter and saves it to the *elements* instance variable.
A computeDifference method that finds the maximum absolute difference between any *2* numbers in *N* and stores it in the *maximumDifference* instance variable.

### Sample Input
```
3
1 2 5
```
### Sample Output
```
4
```
### Code
```
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>

using namespace std;

class Difference
{
    private:
    vector<int> elements;
  
  	public:
  	int maximumDifference;
    
    void computeDifference()
    {
        sort(elements.begin(), elements.end()); 
        this->maximumDifference=elements[elements.size()-1]-elements[0];
    }
    
    Difference (vector<int> a)
    {
        this->elements=a;
    }
};

int main() 
{
    int N;
    cin >> N;
    
    vector<int> a;
    
    for (int i = 0; i < N; i++) {
        int e;
        cin >> e;
        
        a.push_back(e);
    }
    
    Difference d(a);
    
    d.computeDifference();
    
    cout << d.maximumDifference;
    
    return 0;
}  
```
