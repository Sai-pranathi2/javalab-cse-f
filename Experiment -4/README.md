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
