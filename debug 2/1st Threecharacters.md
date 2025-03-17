
```java
import java.util.Scanner;

public class FirstThreeCharacters {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Taking a string as input
        System.out.print("Enter a string: ");
        String str = sc.nextLine();

        // Extracting the first three characters
        // If the string length is less than 3, print the entire string
        String firstThree = str.length() >= 3 ? str.substring(0, 3) : str;

        // Displaying the result
        System.out.println("First three characters: " + firstThree);

        sc.close();
    }
}
```

### **Example Runs:**
```
Enter a string: Hello
First three characters: Hel
```
```
Enter a string: Hi
First three characters: Hi
```
```
Enter a string: Java
First three characters: Jav
```

