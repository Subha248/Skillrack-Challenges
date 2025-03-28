Here's your formatted Java program with explanation, structured to suit GitHub markdown:

```java
// Importing Scanner class to take user input
import java.util.Scanner;

public class Hello {
    public static void main(String[] args) {
        // Creating a Scanner object to read input from the user
        Scanner sc = new Scanner(System.in);
        
        // Reading the input as a full line to handle cases with spaces
        String s = sc.nextLine();  
        
        // Splitting the input string using ":" as a delimiter
        String[] parts = s.split(":");  

        // Checking if we got exactly 3 parts to avoid runtime errors
        if (parts.length == 3) {  
            // Parsing each part as an integer after trimming extra spaces
            int A = Integer.parseInt(parts[0].trim());  
            int B = Integer.parseInt(parts[1].trim());  
            int C = Integer.parseInt(parts[2].trim());  

            // Performing the operation (A + B) / C and printing the result
            System.out.print((A + B) / C);
        } else {
            // Handling cases where input format is incorrect
            System.out.println("Invalid input format");  
        }

        // Closing the Scanner to prevent resource leaks
        sc.close();
    }
}
```

### Line-by-Line Explanation

1. `import java.util.Scanner;` → Imports the Scanner class to read user input.

2. `public class Hello {` → Defines a public class named Hello.

3. `public static void main(String[] args) {` → Main method where execution starts.

4. `Scanner sc = new Scanner(System.in);` → Creates a Scanner object to read input.

5. `String s = sc.nextLine();` → Reads the entire input as a string, ensuring spaces are included.

6. `String[] parts = s.split(":");` → Splits the string into an array using `:` as the separator.

7. `if (parts.length == 3) {` → Checks if the input contains exactly three parts (to avoid errors).

8. `int A = Integer.parseInt(parts[0].trim());` → Converts the first part into an integer after removing spaces.

9. `int B = Integer.parseInt(parts[1].trim());` → Converts the second part into an integer.

10. `int C = Integer.parseInt(parts[2].trim());` → Converts the third part into an integer.

11. `System.out.print((A + B) / C);` → Computes the result `(A + B) / C` and prints it.

12. `} else {` → If input is not in the correct format, execute this block.

13. `System.out.println("Invalid input format");` → Displays an error message.

14. `sc.close();` → Closes the Scanner to free resources.

This structure should fit well within GitHub repositories as both code and explanation are clearly separated. Let me know if you'd like further refinements!
