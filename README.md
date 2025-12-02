# Oops
Oops programming 
#### index
1. acess modifiers
2. encapsulation
3. constructor
   
### syntax explanation 
``` Cpp
#include <iostream>
using namespace std;
class Teacher {
    private:
    double salary;
    public:
    string name;
    string dept;
    string subject;
    
void changeDept (string newDept) {
    dept = newDept;
}

//setter
void setSalary (double s) {
    salary = s;
}

double getSalary() {
return salary;
}

};
int main() {
    Teacher t1 ;
    t1.name = "Shradha";
    t1.subject = "C++";
    t1.dept = "Computer Science";
    cout << t1.name << endl;
    return 0;
}
```

##### encapsulation 
combine data and other function

```cpp
#include <iostream>
using namespace std;
class Teacher {
    double salary;
    public:
    string name;
    string dept;
    string subject;
    
//setter
void setSalary (double s) {
    salary = s;
}

double getSalary() {
return salary;
}
```

##### constructor
object creation used for initialisation

```cpp
public:
Teacher() {
cout << "Hi, I am constructor\n";
}
```
```
public:
Teacher () {
    dept = "Computer Science";
}
```
```public:
//non-parameterized
Teacher() {
dept = "Computer Science";

//parameterized
Teacher(string n, string d, string s, double sal) {
name = n;
dept =xd;
subject = s;
salary = sal;
}

```
```
//copy constructor
Teacher(Teacher &org0bj) {
    cout << "i am custom copy constructor ... \n";
    this->name = org0bj.name;
    this->dept = org0bj.dept;
    this->subject = org0bj.subject;
    this->salary = org0bj. salary;
}
```
