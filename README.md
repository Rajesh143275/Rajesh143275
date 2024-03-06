Q1)Write a program to create a clss and implement default,overloaded,copy constuctor
A)
#DEFAULT 
public class Bike {
    Bike(){
        System.out.print("Bike Is Created");
    }

    public static void main(String[] args) {
        Bike b=new  Bike();
    }
}
#OVERLOADED
public class Add {
Add () {
System.out.println("Hiiii");
}
Add(int a) {
System.out.println("a="+a);
}
Add(char c) {
System.out.println("c="+c);
}
public static void main(String[] args) {
Add obj1=new Add();
Add obj2=new Add(10);
Add obj3=new Add('@');
}
}
#COPY
public class Student1 {
int id;
String name;
Student1(int i, String n) {
id=i;
name=n;
}
Student1(Student1 s) {
id=s.id;
name=s.name;
}
void display () {
System.out.println(id+"      "+name);
}
public static void main(String[] args) {
Student1 s1=new Student1 (111,"Karan");
Student1 s2=new Student1(s1);
s1.display();
s2.display();
}
}
B)OVERLOADING
public class Addition (
void add(){
System.out.println("Zero parameter");
}
void add(char a) {
    System.out.println("character="+a);
}
void add(int a, int b) {
System.out.println("a="+a+"b="+b);
}
void add(int e, float d) {
System.out.println("e="+e+"d="+d);
}
public static void main(String[] args) {
Addition a=new Addition();
a.add();
a.add('@');
a.add(10,20);
a.add(50,60.5F);
}
}
#STATIC
public class Number {
static void greatest() {
int x=10;
int y=20;
if (x>y) {
System.out.println("X is greatest");
}
else{
System.out.println("Y is greatest");
}
return;
}
public static void main(String[] args) {
Number.greatest();
}
}
