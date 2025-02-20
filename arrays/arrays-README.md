## Arrays

An array is a way to reference a series of memory locations using the same name. Each memory location is an array element, identified by an index value (a number inside square brackets []).


## Example :

```cpp
grades[0]  // First element
grades[1]  // Second element
grades[2]  // Third element
```
- Each array element functions like a variable, but instead of a name, it is accessed using an index.

## Example :
```cpp
int maryGrade;  // Variable
int grades[1];  // Array
maryGrade = 90;
grades[0] = 90;
```

### Using an Array
Just like variables, array elements can store and retrieve values using assignment statements:

```cpp
bobGrade = maryGrade;
grades[0] = grades[1];
grades[0] = bobGrade;
```
Arrays allow easy manipulation of data just like variables.

### **Summary of Arrays**  

#### **What is an Array?**  
An **array** is a way to reference a series of **memory locations** using the same **name**. Each memory location is an **array element**, identified by an **index value** (a number inside square brackets `[]`).  

Example:  
```cpp
grades[0]  // First element
grades[1]  // Second element
grades[2]  // Third element
```
Each **array element** functions like a **variable**, but instead of a name, it is accessed using an **index**.  

Example:  
```cpp
int maryGrade;  // Variable
int grades[1];  // Array
maryGrade = 90;
grades[0] = 90;
```

#### **Using an Array**  
Just like variables, array elements can store and retrieve values using **assignment statements**:  
```cpp
bobGrade = maryGrade;
grades[0] = grades[1];
grades[0] = bobGrade;
```
Arrays allow easy manipulation of data **just like variables**.

---

### **Why Use an Array?**  

#### **1. Handling Large Data Sets**  

If you had **100 grades**, using **100 variables** would be **inefficient**. Instead, an **array** allows looping through elements **efficiently**:  
```cpp
sum = 0;
for (int i = 0; i < 100; i++) {
    sum = sum + grades[i];
}
```
This **eliminates** the need to manually reference multiple variables.  

#### **2. Memory Organization**  
- **Array elements** are stored **next to each other in memory** (contiguous).  
- **Variables** are stored **anywhere** in memory.  
- **Why does this matter?**  
  - When using **pointers**, moving through **array elements** is **more efficient** than moving between variables.  

Arrays make working with **large data** and **memory management** easier!
