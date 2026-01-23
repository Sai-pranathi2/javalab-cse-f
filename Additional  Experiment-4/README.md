## Additional Experiment-4
## Title:) Dsiplay  Perferct number or not
```
import java.util.Scanner;

class Perfect {

    public static void main(String args[]) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the positive number: ");
        int num = sc.nextInt();

        int sum = 0;

        for (int i = 1; i < num; i++) {

            if (num % i == 0) {
                sum = sum + i;
            }
        }

        if (sum == num) {
            System.out.println("num is a perfect number");
        }
        else {
            System.out.println("num is not a perfect number");
        }
    }
}
```
## output
<img width="1920" height="1080" alt="additional  4output" src="https://github.com/user-attachments/assets/792e5f3b-513e-470d-9813-d6ad2ecf9f17" />
