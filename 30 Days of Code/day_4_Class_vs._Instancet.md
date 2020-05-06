**Task**
* Write a Person class with an instance variable,age, and a constructor that takes an integer, initialAge,as a parameter. 
The constructor must assign initialAge to age after confirming the argument passed as initialAge is not negative; if a negative argument is passed as initialAge, 
the constructor should set age to 0 and *print Age is not valid, setting age to 0.*. 
In addition, you must write the following instance methods:

1. yearPasses() should increase the Age instance variable by 1.
2. amIOld() should perform the following conditional actions:
* If age<13 print You are young..
* If age>=13 and age<18, print You are a teenager..
* Otherwise, print You are old..
---
```
using namespace std;
#include <iostream>
class Person
{
    public:
        int age;
        Person(int initialAge);
        void amIOld();
        void yearPasses();
};
Person::Person(int initialAge)
{
    if(initialAge>0)
    {
        this->age=initialAge;
    }
    else
    {   cout<<"Age is not valid, setting age to 0."<<endl;
        this->age=0;
    }     
}

void Person::amIOld()
{
    if(this->age<13) 
    {
        cout<<"You are young."<<endl;
    }
    else if(this->age<18 && this->age>=13 ) 
    {
        cout<<"You are a teenager."<<endl;
    }
    else if(this->age>=18) 
    {
        cout<<"You are old."<<endl;
    }
}
void Person::yearPasses()
{
    this->age=age+1;
}
int main()
{
    int t;
	int age;
    cin >> t;
    for(int i=0; i < t; i++) {
    	cin >> age;
        Person p(age);
        p.amIOld();
        for(int j=0; j < 3; j++) {
        	p.yearPasses(); 
        }
        p.amIOld();
      
		cout << '\n';
    }

    return 0;
}
```
