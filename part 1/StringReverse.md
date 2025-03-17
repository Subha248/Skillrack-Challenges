
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        String S = scan.nextLine(); // Read input string

        // Using StringBuilder to reverse the string
        String reversed = new StringBuilder(S).reverse().toString();

        System.out.println(reversed); // Print reversed string
        scan.close();
    }
}
```

### **Explanation:**
1. **`new StringBuilder(S)`** → Converts the input string into a `StringBuilder` object.  
2. **`.reverse()`** → Reverses the characters in the `StringBuilder`.  
3. **`.toString()`** → Converts the reversed `StringBuilder` back to a `String`.  
4. **Prints the reversed string.**  

### **Example Execution:**
#### **Input 1:**  
```plaintext
abcde
```
#### **Process:**  
`"abcde"` → `"edcba"`

#### **Output:**  
```plaintext
edcba
```

#### **Input 2:**  
```plaintext
look
```
#### **Process:**  
`"look"` → `"kool"`

#### **Output:**  
```plaintext
kool
```


```java
String reversed = new StringBuilder(S).reverse().toString();
```

### **Step 1: Convert the String to a StringBuilder**  
`new StringBuilder(S)`  
- `StringBuilder` is a special tool in Java that allows us to **change** (modify) a string easily.  
- We put `S` (the input string) inside `StringBuilder` to prepare it for reversing.

### **Step 2: Reverse the String**  
`.reverse()`  
- This flips the string backward.  
- Example: `"abcde"` becomes `"edcba"`.

### **Step 3: Convert Back to a String**  
`.toString()`  
- After reversing, we need to **convert it back** to a normal string so we can print it.

### **Final Output**  
The reversed string is now stored in `reversed`, and we can print it with:  
```java
System.out.println(reversed);
```

### **Example Execution**
#### **Input:**
```
hello
```
#### **Processing:**
1. `"hello"` → Goes into `StringBuilder`
2. Reversed → `"olleh"`
3. Converted back to string → `"olleh"`

#### **Output:**
```
olleh
```

