# Oops
Oops programming 
#### index
1. acess modifiers
2. encapsulation
3. constructor
4. shallow vs deep copy
5. destructor
6. inheritance
   
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

//shallow copy
Student(Student &obj) {
    this->name = obj.name;
    this->cgpaPtr = obj.cgpaPtr;
}

//deep copy
Student(Student &obj){
    this->name = obj.name;
    cgpaPtr = new double;
    cgpaPtr = *obj.cgpaPtr;
}

```
```cpp
int main() {
    Student s1("rahul kumar", 8.9);
    Student s2(s1); //"neha kumar"

    s1.getInfo();
    *(s2.cgpaPtr) = 9.2;
    s1.getInfo();

    s2.name = "neha";
    s2.getInfo();
    return 0;
}
```
```cpp
//destructor
~Student() {
    cout << "Hi, I delete everything\n";
}
```
```cpp
class Student : public Person {
public:
    int rollno;

    void getInfo() {
        cout << "name : << name << endl;
        cout << "age : " << age << endl;
        cout << "rollno : " << rollno << endl;
}
```
##### inherittance
###### multilevel inheritance
```cpp
class GradStudent : public Student {
public:
    string researchArea;
};

int main() {
    GradStudent s1;
    s1.name = "tony stark";
    s1.researchArea = "quantum physics";
    cout << s1.name << endl;
    cout << s1.researchArea << endl;
    return 0;
}
```
###### multiple inheritance
```cpp
class Student {
public:
    string name;
    int rollno;
};

class Teacher {
public:
    string subject;
    double salary;
};

class TA : public Student, public Teacher {
public:
    string researchArea;
};
```
###### hierarchial inheritance
```cpp
class Person {
public:
    string name;
    int age;
};

class Student : public Person {
public:
    int rollno;
}

class Teacher : public Person{
public:
    string subject;
}
```
