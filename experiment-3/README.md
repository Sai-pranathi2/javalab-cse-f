## EXPERIMENT-3

## EXperiment-3a

## TITLE:3a)Implementing constructor Ovverrloading.
## SourceCode
```
class Student {
String name;
int age;
double marks;
Student(){
}
Student(String name,int age,double marks){
this.name=name;
this.age=age;
this.marks=marks;
}
void display(){
System.out.println("Name:"+name);
System.out.println("Age:"+age);
System.out.println("marks:"+marks);
}
}
```
## Main.java
```
class Main{
public static void main(String args[]){
Student std = new Student();
std.display();
Student std1 = new Student("Hari",40,67.8);
std1.display();
}
}
```
## output
<img width="1920" height="1080" alt="Screenshot 2026-01-22 144034" src="https://github.com/user-attachments/assets/38515323-a5f0-40cf-a2de-0f49c8a9085f" />



