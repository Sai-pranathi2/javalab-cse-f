## Additional Experiment-3
## Title:)display the palindrome  or not
##  SourceCode
```
import java.util.Scanner;

class Palindrome {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the string: ");
        String str = sc.nextLine();

        int start = 0;
        int end = str.length() - 1;
        boolean flag = true;

        while (start < end) {

            if (str.charAt(start) != str.charAt(end)) {
                flag = false;
                break;
            }

            start++;
            end--;
        }

        if (flag) {
            System.out.println("String is a palindrome");
        } else {
            System.out.println("String is not a palindrome");
        }
    }
}
```
## output
<img width="1920" height="1080" alt="additional 3 output" src="https://github.com/user-attachments/assets/e5fd9802-5cb3-4327-b1ff-0deca05c9594" />
