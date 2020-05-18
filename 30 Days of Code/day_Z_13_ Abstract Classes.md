### Task
Given a Book class and a Solution class, write a MyBook class that does the following:

* Inherits from Book
* Has a parameterized constructor taking these 3 parameters:
> * string **title**
> * string **author**
> * int **price**

Implements the Book class' abstract display() method so it prints these  lines:
* **title**, a space, and then the current instance's .**title**
* **author**, a space, and then the current instance's .**author**
* **price**, a space, and then the current instance's .**price**

### Sample Input

The following input from stdin is handled by the locked stub code in your editor:
```
The Alchemist
Paulo Coelho
248
```
### Sample Output
T
he following output is printed by your display() method:
```
Title: The Alchemist
Author: Paulo Coelho
Price: 248
```
### Code
```
class Book 
{
    constructor(title, author)
    {
        if (this.constructor === Book)
        {
            throw new TypeError('Do not attempt to directly instantiate an abstract class.'); 
        }
        else 
        {
            this.title = title;
            this.author = author;
        }
    }
    
    display()
    {
        console.log('Implement the \'display\' method!')
    }
};
class MyBook: public Book
{
protected:
    int price;   
public:
    MyBook(string title,string author,int price): Book(title, author)
    {
        this->price=price;
    }
    void display()
    {
        cout<<"Title: "<<title<<endl<<"Author: "<<author<<endl<<"Price: "<<price<<endl;
    }
};
function main()
{
    let title = readLine()
    let author = readLine()
    let price = +readLine()

    let book = new MyBook(title, author, price)
    book.display()
}

```
