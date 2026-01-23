## Additional Experiment-1
## Title:) Display the substring
## SourceCode
```
import java.util.Scanner;

class SubString {

    public static void main(String args[]) {

        String mainString;
        String subString;
        int position;

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the main String: ");
        mainString = sc.nextLine();

        System.out.print("Enter the sub String: ");
        subString = sc.nextLine();

        System.out.print("Enter the position to insert: ");
        position = sc.nextInt();

        int length = mainString.length() - 1;
        String resultString;

        if (position >= 0 && position <= length) {

            String firstPart = mainString.substring(0, position);
            String secondPart = mainString.substring(position);

            resultString = firstPart + subString + secondPart;

            System.out.println("Resultant string = " + resultString);
        }
        else {

            System.out.println("Substring is not possible to insert");
            System.out.println("Its condition 0 <= position <= length of main string");
        }
    }
}
```
## output
<img width="1920" height="1080" alt="additional 1 output" src="https://github.com/user-attachments/assets/8e614534-4e7e-4dfc-945e-ea085b896810" />
