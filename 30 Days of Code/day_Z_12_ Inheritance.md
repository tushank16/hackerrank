### Task 

* You are given two classes, Person and Student, where Person is the base class and Student is the derived class. Completed code for Person and a declaration for Student are provided for you in the editor. Observe that Student inherits all the properties of Person.
* Complete the Student class by writing the following:
A Student class constructor, which has  parameters:
* A string, **firstname**.
* A string, **lastname**.
* An integer, **id**.
An integer array (or vector) of test scores, **scores**.
A char calculate() method that calculates a Student object's average and returns the grade character representative of their calculated average:

### Sample Input
```
Heraldo Memelli 8135627
2
100 80
```
### Sample Output
```
 Name: Memelli, Heraldo
 ID: 8135627
 Grade: O
 ```
 ### Code
 ```
 #include <iostream>
#include <vector>

using namespace std;


class Person{
	protected:
		string firstName;
		string lastName;
		int id;
	public:
		Person(string firstName, string lastName, int identification){
			this->firstName = firstName;
			this->lastName = lastName;
			this->id = identification;
		}
		void printPerson(){
			cout<< "Name: "<< lastName << ", "<< firstName <<"\nID: "<< id << "\n"; 
		}
	
};

class Student :  public Person
{
      private:
        vector<int> testScores;
        int sum=0, subs=0;
        double avg=0.0;
    public:
       Student(string firstN, string lastN, int idS, vector<int> scores): Person(firstN,lastN,idS)
       {
         this->testScores=scores;
         subs=testScores.size();
       }
      char calculate()
        {
           char g;
           for(unsigned int i=0; i<subs; ++i)
            {
               sum+=testScores[i];
            }
           avg=sum/subs;
           if     (avg>=90 && avg<=100)
                  g='O';
           else if(avg>=80 && avg<=90)
                  g='E';
           else if(avg>=70 && avg<=80)
                  g='A';
           else if(avg>=55 && avg<=75)
                  g='P';
           else if(avg>=40 && avg<=55)
                  g='D';
           else if(avg<40)
                  g= 'T';
            return g;
        }

};

int main() {
	string firstName;
  	string lastName;
	int id;
  	int numScores;
	cin >> firstName >> lastName >> id >> numScores;
  	vector<int> scores;
  	for(int i = 0; i < numScores; i++){
	  	int tmpScore;
	  	cin >> tmpScore;
		scores.push_back(tmpScore);
	}
	Student* s = new Student(firstName, lastName, id, scores);
	s->printPerson();
	cout << "Grade: " << s->calculate() << "\n";
	return 0;
}
 ```
