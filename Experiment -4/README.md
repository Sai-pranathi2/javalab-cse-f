## Experiment-4
## Experiment-4a
## TITLE:4a)Implement Single Inheritance
## Person.java
```
class Person {
    String name;
    int age;

    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    void displayPersonDetails() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }
}
```
## Employee.java
```
class Employee extends Person {

    double annualSalary;
    int yearOfJoining;
    String nationalInsuranceNumber;

    Employee(String name, int age, double annualSalary, int yearOfJoining,
             String nationalInsuranceNumber) {

        super(name, age);
        this.annualSalary = annualSalary;
        this.yearOfJoining = yearOfJoining;
        this.nationalInsuranceNumber = nationalInsuranceNumber;
    }

    void displayEmployeeDetails() {
        displayPersonDetails();
        System.out.println("Annual Salary: " + annualSalary);
        System.out.println("Year of Joining: " + yearOfJoining);
        System.out.println("National Insurance Number: " + nationalInsuranceNumber);
    }
}
```
## TestEmployee.java
```
class TestEmployee {
    public static void main(String args[]) {

        Employee emp1 = new Employee(
                "pranathi",
                30,
                60000.95,
                2011,
                "2003-2004-2005-2006"
        );

        emp1.displayEmployeeDetails();
    }
}
```
## output
<img width="1920" height="1080" alt="exp4a" src="https://github.com/user-attachments/assets/bb78ac74-3274-4242-a195-59a16837716d" />




## Experiment 4B

## TITLE: Implement mulitiple inheritances

## SOURCE CODE:

---

## BICICYLE:

```

class Bicycle {
    String pedalType;

    void showBicycleInfo() {
        System.out.println("Pedal Type: " + pedalType);
    }
}

```

## MotorBike:

```

  GNU nano 8.7                      Motorbike.java
class Motorbike extends Bicycle {
    int engineCapacity;

    void showMotorbikeInfo() {
        System.out.println("Engine Capacity: " + engineCapacity + " cc");
    }
}

```

## ElectricBike:

```

class ElectricBike extends Motorbike {
    int batteryCapacity;

    void showElectricBikeInfo() {
        System.out.println("Battery Capacity: " + batteryCapacity + " W>
    }
}

```

## TestVechile:

```

public class TestVehicle {
    public static void main(String[] args) {

        ElectricBike eBike = new ElectricBike();

        eBike.pedalType = "Manual Pedals";
        eBike.engineCapacity = 250;
        eBike.batteryCapacity = 500;

        eBike.showBicycleInfo();
        eBike.showMotorbikeInfo();
        eBike.showElectricBikeInfo();
    }
}

```

## output
<img width="1920" height="1080" alt="exp4b" src="https://github.com/user-attachments/assets/dd34de6e-ea0f-427d-80a3-f9a00cdbb5cd" />


## Experiment-4c
## TITLE:4c)To find the areas of different shapes
## Figure
```
abstract class Figure {
    double dim1;
    double dim2;

    Figure(double dim1, double dim2) {
        this.dim1 = dim1;
        this.dim2 = dim2;
}
abstract double area();
}

```
## Rectangle
```
class Rectangle extends Figure {

    Rectangle(double length, double breadth) {
        super(length, breadth);
    }

    double area() {
        return dim1 * dim2;
    }
}
```
##  Triangle
```
class Triangle extends Figure {

    Triangle(double base, double height) {
        super(base, height);
    }

    double area() {
        return 0.5 * dim1 * dim2;
    }
}
```
## Test figure
```
public class TestFigure {
    public static void main(String[] args) {

        Figure f1 = new Rectangle(10, 5);
        System.out.println("Area of Rectangle = " + f1.area());

        Figure f2 = new Triangle(6, 4);
        System.out.println("Area of Triangle = " + f2.area());
    }
}
```


## output
<img width="1920" height="1080" alt="exp4c" src="https://github.com/user-attachments/assets/a78add6a-ca76-4107-8f4d-1473851dd15e" />
