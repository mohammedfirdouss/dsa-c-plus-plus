
#  **Arrays**  
  - **letters** array: `char letters[3];`  
    - Stored **sequentially in memory** (`letters[0] = 'C'`, `letters[1] = 'B'`, `letters[2] = 'A'`).  

- **Array of Pointers**  
  - **ptLetters**: `char * ptLetters[3];`  
    - Each element is a **pointer variable** holding a **memory address** of an element in the **letters** array.  
    - The **ampersand (&)** is the **address operator**, so `ptLetters[i] = &letters[i];` assigns the **memory address** of `letters[i]`.  

- **Array of Pointers to Pointers**  
  - **ptPtLetters**: `char ** ptPtLetters[3];`  
    - Each element is a **pointer to a pointer**: it holds the **address of** an element in **ptLetters** (which itself is a **pointer**).  
    - Code example:
      ```cpp
      ptPtLetters[0] = &ptLetters[2];
      ptPtLetters[1] = &ptLetters[1];
      ptPtLetters[2] = &ptLetters[0];
      ```

- **Reordering Data**  
  - Printing with `cout << **ptPtLetters[i] << endl;` produces `ABC`, even though the **letters** array was originally `C, B, A`.  
  - This happens because the **pointer to pointer** chain redirects which **memory addresses** get accessed.  
  - **Important**: You can **change the order** of data by **juggling memory addresses** (pointers) instead of modifying the original **letters** array.  

- **Real-World Use**  
  - In practice, pointers might point to **client data** (name, address, phone, etc.), letting you reorder large sets of information **efficiently** without altering the actual data.
