
```java
import java.util.Scanner;

public class Hello {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();   // Read the input string
        char ch1 = sc.next().charAt(0);   // Read first character
        char ch2 = sc.next().charAt(0);   // Read second character
        sc.close();
        
        // Replace all occurrences of ch1 with ch2 in str
        String modifiedStr = str.replace(ch1, ch2);
        
        // Print the modified string
        System.out.print(modifiedStr);
    }
}
```

### **Explanation of Filled Blanks:**
1. `String str = sc.nextLine();` → Reads the full string input.
2. `char ch1 = sc.next().charAt(0);` → Reads the first character.
3. `char ch2 = sc.next().charAt(0);` → Reads the second character.
4. `String modifiedStr = str.replace(ch1, ch2);` → Replaces **ch1** with **ch2**.
5. `System.out.print(modifiedStr);` → Prints the modified string.

---

### **Example Runs**
#### **Input:**
```
robotics
o e
```
#### **Processing:**
- Replace 'o' with 'e' in `"robotics"`.
#### **Output:**
```
rebetics
```

#### **Input:**
```
EtherNet
N n
```
#### **Processing:**
- Replace 'N' with 'n' in `"EtherNet"`.
#### **Output:**
```
Ethernet
```

This should work perfectly! 🎯 Let me know if you need any changes. 😊
