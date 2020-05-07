### Task
Given n names and phone numbers, assemble a phone book that maps friends' names to their respective phone numbers. 
You will then be given an unknown number of names to query your phone book for. For each name queried, 
print the associated entry from your phone book on a new line in the form name=phoneNumber; 
if an entry for name is not found, print *Not found* instead.

## Sample Input
```
3
sam 99912222
tom 11122222
harry 12299933
sam
edward
harry
```

## Sample Output
```
sam=99912222
Not found
harry=12299933
```
## Code
```
#include <iostream>
#include <map>
#include <string>
using namespace std;

int main() 
{
    std::map<std::string , unsigned int> name_map;
      int n;
      string name;
   // cout<<"Enter the no of values"<<endl;
    cin>>n;
    
    for(int i=0;i<n;i++)
    {
        int a;
        string s;
        //cout<<"Enter string"<<endl;
        cin>>s;
        //cout<<"Enter no"<<endl;
        cin>>a;
        name_map.insert(std::pair<std::string , unsigned int>(s,a));
    }
    
   
     std::map<std::string ,  unsigned int>::iterator it;    //Set up iterator.
    
    while(cin >> name)    //Loop for user queries.
    {
        it = name_map.find(name);
        
        if(it != name_map.end())
        {
            string key = it->first;
            
            int value = it->second;
            
            cout << key << "=" << value << endl;
        }
        else
            cout << "Not found" << endl;
    }
    name_map.clear();
    return 0;
}

```
