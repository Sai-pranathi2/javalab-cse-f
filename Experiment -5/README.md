## Experiment-5
## Experiment-5a
## Title:)Java program to implement interface
## Sortable
```
public interface Sortable {
    void sort(int[] arr);
}

```
## Bubblesort
```
public class BubbleSort implements Sortable {

    public void sort(int[] arr) {
        int n = arr.length;
        for (int i = 0; i < n - 1; i++) {
            for (int j = 0; j < n - i - 1; j++) {
                if (arr[j] > arr[j + 1]) {
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
            }
        }
    }
```
## SelectionSort
```
public class SelectionSort implements Sortable {

    public void sort(int[] arr) {
        int n = arr.length;
        for (int i = 0; i < n - 1; i++) {
            int min = i;
            for (int j = i + 1; j < n; j++) {
                if (arr[j] < arr[min]) {
                    min = j;
                }
            }
            int temp = arr[min];
            arr[min] = arr[i];
            arr[i] = temp;
        }
    }
}
```
## Testsort
```
import java.util.Scanner;

public class TestSort {

    static void printArray(int[] arr) {
        for (int x : arr) {
            System.out.print(x + " ");
        }
        System.out.println();
    }

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        // -------- Bubble Sort Input --------
        System.out.print("Enter number of elements for Bubble Sort: ");
        int n1 = sc.nextInt();

        int[] arr1 = new int[n1];
        System.out.println("Enter elements:");
        for (int i = 0; i < n1; i++) {
            arr1[i] = sc.nextInt();
        }

        Sortable ref = new BubbleSort();
        ref.sort(arr1);
        System.out.println("Array sorted using Bubble Sort:");
        printArray(arr1);

        // -------- Selection Sort Input --------
        System.out.print("Enter number of elements for Selection Sort: ");
        int n2 = sc.nextInt();

        int[] arr2 = new int[n2];
        System.out.println("Enter elements:");
        for (int i = 0; i < n2; i++) {
            arr2[i] = sc.nextInt();
        }

        ref = new SelectionSort();
        ref.sort(arr2);
        System.out.println("Array sorted using Selection Sort:");
        printArray(arr2);

        sc.close();
    }
}
```
## Output
<img width="1920" height="1080" alt="Screenshot 2026-02-13 160505" src="https://github.com/user-attachments/assets/9ecd7635-0f8c-4b42-bbaa-46ac6416931f" />




##  Exp-5b
## Title:)Implement Runtime 
## Vehicle
```
class vehicle {

    void run() {
        System.out.println("vehicle is running");
    }
}
```
## Car
```                             
class car extends vehicle {

    @Override
    void run() {
        System.out.println("car is running on four wheels");
    }
}
```
## Bike
```
class Bike extends vehicle {

    @Override
    void run() {
        System.out.println("bike is running on two wheels");
    }
}
```
##  TestVehicle
```
public class TestVehicle {

    public static void main(String[] args) {

        vehicle v;   // base class reference

        v = new car();
        v.run();     // calls car's run()

        v = new Bike();
        v.run();     // calls bike's run()

        v = new vehicle();
        v.run();     // calls vehicle's run()
    }
}
```
## Output
<img width="1920" height="1080" alt="Screenshot 2026-02-13 161125" src="https://github.com/user-attachments/assets/3d447729-80c1-4d27-98ca-1c0e22a2b2b3" />




## Experiment-5c
## Title:)JAVA program using StringBuffer to delete, remove character.
## SourceCode
```
  GNU nano 8.7                        StringBufferDeleteDemo.java
public class StringBufferDeleteDemo {

    public static void main(String[] args) {

        // Create StringBuffer object
        StringBuffer sb = new StringBuffer("Java Programming");

        // Display original string
        System.out.println("Original String: " + sb);

        // Delete a single character at index 4
        sb.deleteCharAt(4);
        System.out.println("After deleting character at index 4: " + sb);

        // Delete a range of characters from index 0 to 4
        sb.delete(0, 4);
        System.out.println("After deleting characters from index 0 to 4: " + sb);
    }
}
```
## OutPut
<img width="1920" height="1080" alt="Screenshot 2026-02-13 160018" src="https://github.com/user-attachments/assets/347a6ba4-98c7-4d1a-9ffe-7b21283542b8" />




