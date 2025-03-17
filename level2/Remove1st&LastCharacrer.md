## **Program: Remove First and Last Character from a String**  

### **Explanation (Step by Step)**  

```java
import java.util.Scanner;  // Import Scanner class to take user input
```
- This imports the `Scanner` class, which helps us take input from the user.  

---

```java
public class Hello {
```
- This defines the class `Hello`, which contains our `main` method.

---

```java
    public static void main(String[] args) {
```
- The `main` method is where the execution of our program starts.

---

```java
        Scanner scanner = new Scanner(System.in);
```
- Creates a `Scanner` object to take user input.

---

```java
        String S = scanner.nextLine();
```
- Reads the user input as a **string** and stores it in the variable `S`.

---

```java
        if (S.length() >= 3) {
```
- **Condition Check:**  
  - The program only works if the string has **at least 3 characters**.  
  - This ensures that after removing the **first** and **last** character, at least **one character** remains.  

---

```java
            String result = S.substring(1, S.length() - 1);
```
- The `substring(1, S.length() - 1)` function extracts the part of the string **excluding** the first and last character.  
  - Example:  
    - Input: `"hello"`  
    - `substring(1, 4)` → `"ell"`  

---

```java
            System.out.println(result);
```
- Prints the modified string.

---

```java
        scanner.close();
```
- **Closes** the scanner to free resources.

---

### **Example Execution**
#### **Input:**
```
Skillrack
```
#### **Processing:**
- Original string: `"Skillrack"`
- After removing the first and last character: `"killrac"`

#### **Output:**
```
killrac
```

---

### **Optimized Code (GitHub Ready)**
```java
import java.util.Scanner;

/**
 * This program removes the first and last character from a given string.
 * It ensures the input string has at least 3 characters before processing.
 */
public class RemoveFirstLastChar {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String S = scanner.nextLine(); // Read input string

        // Ensure the string has at least 3 characters
        if (S.length() >= 3) {
            System.out.println(S.substring(1, S.length() - 1)); // Remove first & last char
        }

        scanner.close();
    }
}
```
