In the given Java program, you need to fill in the blanks to read an alphabet and print its ASCII value.

Here’s how you should complete the blanks:

```java
import java.util.Scanner;

public class Hello {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        char ch = sc.next().charAt(0); // Reads a single character
        System.out.print((int) ch); // Prints the ASCII value of the character
    }
}
```

### Explanation:
1. `sc.next().charAt(0);` → Reads the first character from user input.
2. `(int) ch` → Converts the character to its ASCII value.
3. `System.out.print((int) ch);` → Prints the ASCII value.

This should work correctly for your **SkillRack** challenge. 🎯🚀
