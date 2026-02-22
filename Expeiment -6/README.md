## EXperiment-6
## Experiment-6a
## Title:)Handling Mechanism
## source Code
```
import java.util.Scanner;

public class Solution {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        // Read size of array
        System.out.print("Enter size of array: ");
        int n = sc.nextInt();

        // Create array
        int[] arr = new int[n];

        // Read array elements
        System.out.println("Enter " + n + " elements:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        // Ask user for index
        System.out.print("Enter index to access: ");
        int index = sc.nextInt();

        // Exception handling
        try {
            System.out.println("Element at index " + index + " is: " + arr[index]);
        } 
        catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Invalid index! Please enter index between 0 and " + (n - 1));
        }

        sc.close();
    }
}
```
## output
<img width="1920" height="1080" alt="Screenshot 2026-02-22 202500" src="https://github.com/user-attachments/assets/0ed3fddf-adb6-4933-b2b7-7412eb6a554b" />
