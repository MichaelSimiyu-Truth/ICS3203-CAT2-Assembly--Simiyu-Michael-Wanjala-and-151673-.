# ICS3203-CAT2-Assembly--Simiyu-Michael-Wanjala-and-151673-.
This repository contains four assembly language programs developed for the ICS3203 CAT 2 practical assignment. These programs demonstrate fundamental assembly language concepts, including control flow, array operations, modular programming, and hardware simulation. Each task highlights specific assembly techniques, providing a deeper understanding of low-level programming.

---

## Repository Structure
ICS3203-CAT2-Assembly--<Simiyu-Michael-Wanjala-151673>
│
├── README.md
├── task1.asm  # Control Flow and Conditional Logic
├── task2.asm  # Array Manipulation with Looping and Reversal
├── task3.asm  # Modular Program with Subroutines for Factorial Calculation
└── task4.asm  # Data Monitoring and Control Using Port-Based Simulation


---

## Task Descriptions

### 1. **Control Flow and Conditional Operations** (`task1.asm`)

This program takes an integer input from the user and classifies it as:
- **POSITIVE**: if the number is greater than zero.
- **NEGATIVE**: if the number is less than zero.
- **ZERO**: if the number is exactly zero.

#### Detailed Explanation:
- **Input Handling**: The program starts by reading the input number using system calls or direct memory addressing (depending on the assembler).  
- **Conditional Logic**: Implements **conditional jumps** (`je` for equality, `jl` for less than) to decide the classification. The program uses branching logic to determine which message to display.  
- **Unconditional Jumps**: Includes an unconditional jump (`jmp`) to ensure the program flow smoothly transitions to the output section regardless of the condition met.

**Key Takeaways**:  
- Highlighted the importance of structured branching for clear logic flow.  
- Efficient use of jumps ensured the program operated predictably in all scenarios.

---

### 2. **Array Manipulation and Reversal** (`task2.asm`)

This program reverses an array of integers in place, directly modifying the original array without using any additional memory.

#### Detailed Explanation:
- **Initialization**: The program first prompts the user to input the size of the array and the elements.  
- **Pointers and Indexing**: Two pointers (or indices) are initialized, one at the start and the other at the end of the array. These pointers move toward each other as elements are swapped.  
- **Looping**: A loop structure is employed to iterate through the array. At each iteration, the elements pointed to by the two pointers are swapped until the pointers meet or cross.  
- **Memory Efficiency**: By modifying the array in place, the program avoids the overhead of additional memory allocation.

**Key Takeaways**:  
- Showcased efficient memory usage through in-place operations.  
- Reinforced the importance of pointer arithmetic in assembly programming.  

---

### 3. **Modular Programming for Factorial Calculation** (`task3.asm`)

This program computes the factorial of a user-provided number using a recursive subroutine, showcasing modular programming in assembly.

#### Detailed Explanation:
- **Recursive Subroutine**: A dedicated subroutine calculates the factorial. If the input number is greater than 1, the subroutine calls itself with the decremented number.  
- **Stack Management**: During each recursive call, the program uses the stack to save the current state of registers and intermediate values, ensuring previous calculations are not lost.  
- **Base Case**: The recursion halts when the number reaches 1, returning 1 to the calling function.  
- **Result Storage**: The final factorial value is stored in a general-purpose register for output or further use.

**Key Takeaways**:  
- Demonstrated the power of modular design in assembly programming.  
- Emphasized the need for careful stack management during recursion to prevent data corruption.  

---

### 4. **Port-Based Simulation for Data Monitoring** (`task4.asm`)

This program simulates a basic hardware control system, involving motor control and alarm activation based on sensor values.

#### Detailed Explanation:
- **Sensor Simulation**: The program simulates sensor values by assigning them to specific memory locations. These values are used as input for decision-making.  
- **Motor Control**: A motor is started or stopped based on the sensor reading. For example, if the value exceeds a threshold, the motor stops; otherwise, it runs.  
- **Alarm Activation**: When the sensor reading surpasses a critical value, an alarm is triggered.  
- **Memory Operations**: Logical conditions are evaluated by accessing and comparing the simulated sensor values in memory. The control actions are implemented through branching instructions.

**Key Takeaways**:  
- Provided insights into hardware simulation using assembly.  
- Highlighted the ability to replicate hardware interactions creatively within a software environment.  

---

## Compilation and Execution

### **Prerequisites**
- An assembler, such as **NASM** or **MASM**, to compile the programs.  
- A compatible system (32-bit or 64-bit) for executing the binaries.  

### **Compilation**
To compile and run the programs using NASM, follow these steps:  
1. Open a terminal and navigate to the directory containing the program files.  
2. Use the following commands to assemble and link the programs:
   ```bash
   nasm -f elf64 task1.asm -o task1.o
   ld task1.o -o task1
   ./task1

### Replace `task1` with the respective program name for other tasks.

#### Example Execution:
For `task2.asm`, reversing an array:
1. Run the program:
   ```bash
   ./task2
