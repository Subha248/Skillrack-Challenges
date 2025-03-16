### **📌 Line-by-line Explanation of the Java Program**

```java
import java.util.Scanner;
```
- This **imports the Scanner class**, which allows us to take user input.

---

```java
public class Main {
```
- Declares a **public class** named `Main`.  
- Every Java program must have a **class**, and `Main` is the entry point.

---

```java
public static void main(String[] args) {
```
- This is the **main method**, where the program execution begins.  
- The `main()` method is required in all Java programs.

---

```java
Scanner scan = new Scanner(System.in);
```
- Creates a **Scanner object** named `scan`.  
- `System.in` tells Java to take **input from the keyboard**.

---

```java
String S = scan.nextLine();
```
- Reads an **entire line of text** (string) from the user and stores it in **variable `S`**.  
- Example: If the user inputs `"hello world"`, then `S = "hello world"`.

---

```java
char C = scan.next().charAt(0);
```
- Reads a **single character input** from the user.  
- `scan.next()` reads the next **word** (until a space).  
- `.charAt(0)` extracts **the first character** of the input.  
- Example: If the user enters `"o"`, then `C = 'o'`.

---

```java
for (int i = 0; i < S.length(); i++) {
```
- This is a **loop** that runs from `i = 0` to `i < S.length()`.  
- It **iterates through each character** in string `S`.  
- `S.length()` gives the **total number of characters** in the string.

---

```java
System.out.print(S.charAt(i));
```
- Prints the **character at index `i`** from the string `S`.  
- Example: If `S = "hello world"` and `i = 0`, it prints `'h'`.  

---

```java
if (S.charAt(i) == C) {
```
- **Checks if the current character `S.charAt(i)` is equal to `C`**.  
- If this condition is `true`, it means we **found the first occurrence of `C`**.

---

```java
break;
```
- **Stops the loop immediately** when `C` is found.  
- This ensures we only print **up to the first occurrence** of `C`.

---

```java
scan.close();
```
- Closes the **Scanner object** to prevent memory leaks.  
- Though not mandatory in small programs, it’s a **good practice**.

---

### **📌 Example Execution**

#### **Input**
```
hello world
o
```
#### **Loop Execution**
| `i` | `S.charAt(i)` | Printed | Condition `S.charAt(i) == 'o'` | Action |
|----|----|----|----|----|
| 0 | 'h' | `h` | ❌ No | Continue |
| 1 | 'e' | `e` | ❌ No | Continue |
| 2 | 'l' | `l` | ❌ No | Continue |
| 3 | 'l' | `l` | ❌ No | Continue |
| 4 | 'o' | `o` | ✅ Yes | **Break** |

#### **Output**
```
hello
```
(Since `'o'` occurs at index `4`, it stops printing after `'o'`.)

---

### **📌 Edge Cases**
1. **If `C` is not in `S`**
   ```
   Input:
   skillrack
   z

   Output:
   skillrack
   ```
   - The loop runs **fully**, printing the entire string.

2. **If `C` is at the beginning**
   ```
   Input:
   apple
   a

   Output:
   a
   ```
   - The loop stops immediately after the first letter.

3. **If `C` is the last letter**
   ```
   Input:
   skillrack
   k

   Output:
   skillrack
   ```
   - The entire string gets printed before stopping.

---

### **💡 Summary**
- This program **reads a string and a character**.
- It **prints characters** from the string **until it finds `C`**.
- Uses a **loop to iterate** and a **break statement to stop early**.
- If `C` is **not found**, the **entire string is printed**.

