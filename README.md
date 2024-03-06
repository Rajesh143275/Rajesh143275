Q1)Write a program to create a class and implement default,overloaded,copy constuctor
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
public class Addition {
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
C)STATIC
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


Q2)Write a program to implement the concept of Inheritance and method overriding
#INHERITANCE
class Employee {
float salary=40000;
}
public class Programmer extends Employee {
int bonus=10000;
public static void main(String[] args) {
Programmer p = new Programmer();
System.out.println("Programmer salary is: "+p.salary);
System.out.println("Bonus of Programmer is: "+p.bonus);
}
}
#SINGLE INHERITANCE
class Animal {
void eat () {
System.out.println("Eating.....");
}
}
Class Dog extends Animal {
void bark() {
System.out.println("Barking........ ");
}
}
public class Test inheritance {
public static void main(String[] args) {
Dog d=new Dog();
d.bark();
d.eat();
}
}
#MULTIPLE INHERITANCE
class Animal {
void eat (){
System.out.println("Eating.......");
}
}
class Dog extends Animal{
void bark() {
System.out.println("Barking......");
}
}
class BabyDog extends Dog{
void weep(){
System.out.println("Weeping......");
}
}
public class Testinheritance2 {
public static void main(String[] args) {
BabyDog d=new BabyDog();
d. weep();
d.bark();
d.eat();
}
}
#HIERARCHIAL INHERITANCE
class Animal {
void eat () {
System.out.println("Eating...");
}
}
class Dog extends Animal {
void bark() {
System.out.println("Barking...");
}
}
class Cat extends Animal {
void meow() {
System.out.println("Meowing......");
}
}
public class Testinheritance3 {
public static void main(String[] args) {
Cat c=new Cat();
c.meow();
c.eat();
}
}
#METHOD OVERRIDING
class Bank{
int getRateOfInterest () {
return 0;
}
}
class SBI extends Bank{
int getRateOfInterest () {
return 8;
}
}
class ICICI extends Bank{
int getRateOfInterest () {
return 7;
}
}
class AXIS extends Bank{
int getRateOfInterest () {
return 9;
}
}
public class Test2 {
public static void main(String[] args) {
SBI s=new SBI();
ICICI i=new ICICI();
AXIS a=new AXIS();
System.out.println("SBI Rate Of Interest: "+s.getRateOfInterest());
System.out.println("ICICI Rate Of Interest: "+i.getRateOfInterest());
System.out.println("AXIS Rate of Interest: "+a.getRateOfInterest());
}
}
#B)Write a program to implement the concepts of Abstract classes and
methods.
abstract class Bike {
abstract void run();
}
public class Honda4 extends Bike {
void run() {
System.out.println("running safely...");
}
public static void main(String[] args) {
Bike obj=new Honda4();
obj.run();
}
}
#C)Write a program to implement the concept of Interfaces.
interface Drawable {
void draw();
}
class Rectangle implements Drawable {
public void draw() {
System.out.println("Drawing Rectangle");
}
}
class Circle implements Drawable {
public void draw() {
System.out.println("Drawing Circle");
}
}
public class Testinterfacel1{
public static void main(String[] args) {
Drawable d=new Circle();
d.draw();
}
}


Q3)
A)Write a program to raise built-in exception and raise them as per the
requirements.
import java.io.*;
public class Divide {
public static void main(String[] args) throws IOException {
int a,b,res;
BufferedReader br=new BufferedReader(new InputStreamReader(System.in));
String str;
System.out.println("Enter two numbers:");
str=br.readLine();
a=Integer.parseInt(str);
str=br.readLine();
b=Integer.parseInt(str);
res=a/b;
System.out.println("The Quotient="+res);
}
}
B)Write a program to define user defined exceptions and raise them as per
the requirements.
import java.io.*;
public class Divide12 {
public static void main(String[] args) throws IOException{
int a=0,b=0,res;
BufferedReader br=new BufferedReader(new InputStreamReader(System.in));
String str;
System.out.println("Enter two numbers:");
try{
str=br.readLine();
a=Integer.parseInt(str);
str=br.readLine();
b=Integer.parseInt(str);
try{
res=a/b;
System.out.println("The Quotient="+res);
}
catch (ArithmeticException ae) {
System.out.println("Exception has occured. You have entered the divisor as zero");
}
}
catch (NumberFormatException ne) {
System.out.println("Invalid Number");
}
}
}


