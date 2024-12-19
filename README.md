//create a program that demonstrates inheritance by defining a base lass student to store details like roll no and name, a //derived class result to store marks for three subjects and calculate the total and percentage 
#include <iostream>
#include <string>
using namespace std;

class student {

protected:
int rollNo;
string name;

public:
void setStudentDetails(int r, string n)
{
rollNo = r;
name = n;
}
void displayStudentDetails{
cout<<"Roll no is:"<<rollNo<<endl;
cout<<"Name is:"<<name<<endl;
}
};
class Result: public Student
{
private:
float marks[3];
float total;
float percentage;
public:
void setMarks(float m1, float m2, float m3)
{
marks[0]=m1;
marks[1]=m2;
marks[2]=m3;
}
void calculateResult() {
total = marks[0]+marks[1]+marks[2];
percentage = total / 3.0;
}
void displayResult() {
displayStudentDetails();
cout<<"Marks in subject1: "<<marks[0]<<endl;
cout<<"Marks in subject2: "<<marks[1]<<endl;
cout<<"Marks in subject3: "<<marks[2]<<endl;
cout<<"The total is: "<< total << endl;
cout<<"Percentage is: "<< percentage << "%" << endl;
}
};
int main()
{
Result student;
int rollNo;
string name;

cout<<"Enter th#include <iostream>
#include <string>
using namespace std;

// Base class
class Student {
protected:
    int rollNo;
    string name;

public:
    void setStudentDetails(int r, string n) {
        rollNo = r;
        name = n;
    }

    void displayStudentDetails() {
        cout << "Roll Number: " << rollNo << endl;
        cout << "Name: " << name << endl;
    }
};

// Derived class
class Result : public Student {
private:
    float marks[3];  // Array to store marks of 3 subjects
    float total;
    float percentage;

public:
    void setMarks(float m1, float m2, float m3) {
        marks[0] = m1;
        marks[1] = m2;
        marks[2] = m3;
    }

    void calculateResult() {
        total = marks[0] + marks[1] + marks[2];
        percentage = total / 3.0;
    }

    void displayResult() {
        displayStudentDetails();
        cout << "Marks in Subject 1: " << marks[0] << endl;
        cout << "Marks in Subject 2: " << marks[1] << endl;
        cout << "Marks in Subject 3: " << marks[2] << endl;
        cout << "Total Marks: " << total << endl;
        cout << "Percentage: " << percentage << "%" << endl;
    }
};

int main() {
    Result student;

    // Input student details
    int rollNo;
    string name;
    cout << "Enter Roll Number: ";
    cin >> rollNo;
    cin.ignore();  // To ignore the newline character left in the buffer
    cout << "Enter Name: ";
    getline(cin, name);

    student.setStudentDetails(rollNo, name);

    // Input marks
    float m1, m2, m3;
    cout << "Enter marks for three subjects: ";
    cin >> m1 >> m2 >> m3;

    student.setMarks(m1, m2, m3);
    student.calculateResult();

    // Display student details and result
    cout << "\nStudent Details and Result:" << endl;
    student.displayResult();

    return 0;
}
e roll no: ";
cin>>rollNo;
cout<<"Enter the name: ";
cin>>name;
student.setStudentDetails(rollNo, name);

float m1, m2 m3;
cout << "Enter marks for three subjects: ";
cin >> m1 >> m2 >> m3;

    student.setMarks(m1, m2, m3);
    student.calculateResult();

    cout << "\nStudent Details and Result:" << endl;
    student.displayResult();
    return 0;
}

