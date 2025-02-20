# **Declaring an Array**

1. **In Java**, there are two techniques for declaring an **array**:
   - Where **memory** is allocated at **compile time**.  
   - Where **memory** is **dynamically allocated** at **runtime**.  
   - **Allocation** is another way of saying **reserving memory**.

2. Declaring an **array** with **memory** reserved at **compile time** is similar in **Java**, **C**, and **C++**, except in **Java** you must **initialize** the **array** when it is declared.  
   - Four components of a statement that declares an **array**:  
     1. **Data type**  
     2. **Array name**  
     3. Total number of **array elements** to create  
     4. Semicolon (;)
   
   - Example in **C** and **C++**:  
     ```cpp
     int grades[10];
     ```  
   - Example in **Java** (compile-time allocation and initialization):  
     ```java
     int[] grades = {0,0,0,0,0,0,0,0,0,0};
     ```
     The size of the **array** is automatically determined by the number of values in the braces.

3. The **data type** is a **keyword** that tells the computer how much **memory** to reserve for each **array element**. In the example, the computer is told to reserve enough **memory** to store an **integer** for each **array element**.

4. The **array name** is used to reference **array elements** in a program. In this example, the **array name** is `grades`. The number within the square brackets is the total number of **elements** in the **array** (10 in this case).

5. **Avoid a common rookie mistake**:
   - The **index** for the first **array element** is **zero**, not one. Thus, the tenth **array element** has the **index** 9, not 10.  
   - Some programs mistakenly declare `int grades[9]` thinking it creates 10 **elements**, but it actually creates 9.  
   - Remember: the value in the square brackets in the **array** declaration is the total number of **elements**, **not** the highest **index**.  
   - If you need 10 **elements**, you declare `[10]`. To access the tenth element, you use **index** 9.

6. To allocate **memory** at **compile time**, you must know the number of **array elements** in advance. Sometimes you do not know this (e.g., when loading data from a fluctuating **database**).

7. The solution in **Java** is to allocate **memory** at **runtime**, also called **dynamically allocating memory**. You do this using the **new operator**:
   ```java
   int grades[] = new int[10];
   ```
   - This creates the same **array** as the previous example.  
   - The **new operator** tells the computer to reserve 10 **array elements**, each the size of an **int data type**, and returns a **reference** to the allocated **memory**.  
   - `int grades[]` declares a **reference** to an **int data type** called `grades`.  
   - That **reference** is then assigned the **memory** returned by the **new operator**.

8. This can be confusing even for experienced programmers. Think of the **visitor’s locker room** example: a stadium has a locker room labeled “Visitors.” This is like the **reference** `grades[]`. Different visiting teams (i.e., different data) use the same **visitor’s locker room** (i.e., the **allocated memory**). Similarly, `grades[]` refers to the **allocated memory** returned by the **new operator**.
