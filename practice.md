# !! Basic start with class definition

## Problem #01

### definig & declaring member function inside class

```c++
    // solution
    #include <iostream>
    using namespace std;
    class Student{
        int rollNo;
        public:
            void setRollNo(int newRollNo){
                rollNo = newRollNo;
            }
    };
    int main(){

        return 0;
    }
```

---

## Problem #02

### defining member func inside but declaring outside of class

```c++
    //solution
    #include <iostream>
    using namespace std;
    class Student{
        int rollNo;
        public:
            void setRollNo(int newRollNo);
    };
    void Student::setRollNo(int newRollNo){
        rollNo = newRollNo;
    }
    int main(){

        return 0;
    }
```

---

## Problem #03

### inline function

```c++
    //solution
    #include <iostream>
    using namespace std;
    inline int area(int len, int height){
        return len * height;
    }
    int main(){
        cout << area(10*20); //inline code will get replaced here / no func call
        return 0;
    }
```

---

## Problem #04

### default inline function in classes

```c++
    //solution
    #include <iostream>
    using namespace std;
    class Student{
        int rollNo;
        public:
            void setRollNo(int newRollNo){
                rollNo = newRolNo;
            }
    };
    int main(){
        Student ibrahim;
        ibrahim.setRollNo(444); //inline code will get replaced / no func call(yet it still depends on compiler)
        return 0;
    }
```

---

## Problem #05

### explicit 'inline' keyword at func definition for func defined outside class

```c++
    //solution
    #include <iostream>
    using namespace std;
    class Student{
        int rollNo;
        public:
            inline void setRollNo(int newRollNo);
    };
    void Student::setRollNo(int newRollNo){
     rollNo = newRollNo;
 }
    int main(){
        Student ibrahim;
        ibrahim.setRollNo(444);//inline code will get replaced here / no func call (yet still depends on compiler)
        return 0;
    }
```

---

## Problem #06

### explicit 'inline' keyword at func definintion for func defined outside class

```c++
    //solution
    #include <iostream>
    using namespace std;
    class Student{
        int rollNo;
        public:
            void setRollNo(int newRollNo);
    };
    inline void Student::setRollNo(int newRollNo){
     rollNo = newRollNo;
 }
    int main(){
        Student ibrahim;
        ibrahim.setRollNo(444);//inline code will get replaced here / no func call (yet still depends on compiler)
        return 0;
    }
```

---

## Problem #06

### explicit 'inline' keyword at both definintion/declaration for func defined outside class (not recommended / rendundant)

```c++
    //solution
    #include <iostream>
    using namespace std;
    class Student{
        int rollNo;
        public:
            inline void setRollNo(int newRollNo);
    };
    inline void Student::setRollNo(int newRollNo){
     rollNo = newRollNo;
 }
    int main(){
        Student ibrahim;
        ibrahim.setRollNo(444);//inline code will get replaced here / no func call (yet still depends on compiler)
        return 0;
    }
```

---

## Problem #07

### Constructors(default/explicit default/overloading)

```c++
    //solution
    #include <iostream>
    using namespace std;
    class Student{
        char *name;
        int rollNo;
        float GPA;
        public:
         Student();//explicit default constr
         Student(char *aName);//for semester exchange stud
         Student(char *aName, int arollNo);//for newly admitted stud
         Student(char *aName, int aRollNo, float aGPA);//for stud who admitt from 5th sem onward, with prev gpa
        void setRollNo(int newRollNo);
    };
    Student::Student(char *aName, int aRollNo){
     if(aRollNo < 0){
      rollNo = 0;
     }else{
      rollNo = aRollNo;
     }
    }
    int main(){
        Student ibrahim;//explicit default constr called
        return 0;
    }
```

---

## Problem #08

### give default values to paremiters instead of overloading multiple constructors

```c++
    //solution
    #include <iostream>
    using namespace std;
    class Student{
        int rollNo;
        public:
        //  Student();
        //  Student(char *aName);
        //  Student(char *aName, int arollNo);
         Student(char *aName, int aRollNo, float aGPA);
         void setRollNo(int newRollNo);
    };
    Student::Student(char *aName = NULL, int aRollNo = 0, float aGPA = 0.0){
     //this constructor will cover all of the 4 constructore scenarios above.
        //so no need for these all{
            //Student();
            //Student(char *aName);
            //Student(char *aName, int arollNo);
        //}
    }
    int main(){
        Student stud1;
        Student stud2("Name");
        Student stud3("Name", 1);
        Student stud4("Name", 1, 4.0);
        return 0;
    }
```

---

## Problem #0

###

```c++
    //solution

```
