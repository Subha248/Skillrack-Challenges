
```java
import java.util.Scanner;

public class PreviousAlphabet {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        // Read the character input
        char ch = sc.next().charAt(0);
        
        // Print the previous alphabet character
        System.out.print((char) (ch - 1));
        
        sc.close();
    }
}
```

### Explanation:
1. **Import `Scanner`** → To read user input.
2. **Create Scanner object (`sc`)** → Reads input from the console.
3. **Read the character (`ch`)** → `sc.next().charAt(0)` gets the first character from input.
4. **Print the previous character** → `(char) (ch - 1)` gets the previous alphabet.
5. **Close the scanner** → To prevent resource leaks.

This code is structured properly and can be copied directly into a GitHub repository. 🚀
