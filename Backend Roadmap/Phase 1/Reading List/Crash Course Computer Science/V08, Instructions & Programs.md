This episode delves into how CPUs are given instructions to execute programs, moving beyond the hardware to explore the software that drives it. It discusses instruction sets, opcodes, and how a CPU fetches, decodes, and executes these instructions, including concepts like jumps, loops, and conditional execution.

## ⚙️ From Hardware to Software
*   A CPU's power comes from its **programmability**; by changing the sequence of instructions, the CPU performs different tasks.
*   The CPU is **hardware controlled by software** that is easy to modify.
*   Instructions and data are stored in the same memory locations, using binary numbers.
*  The **HALT instruction** is important for separating instructions from data.

## 📝 Instruction Format
*   Instructions for a hypothetical CPU consist of an **opcode** (operation code) and an address or register.
*  In the example, the **first four bits specify the opcode**, and the **second four bits specify an address or register**.
*   For example, `0010 1110` can be understood as the instruction "LOAD\_A 14", where `0010` is the opcode for `LOAD_A` and `1110` (14 in decimal) is the memory address.

## 🧮 Basic Instructions
*   **LOAD\_A \[address]:** Loads the value from the specified memory address into register A.
*   **LOAD\_B \[address]:** Loads the value from the specified memory address into register B.
*   **ADD:** Adds the values in registers B and A, storing the result in register A.
*  **STORE\_A \[address]:** Stores the value in register A into the specified memory address.
*  **SUBTRACT:** Subtracts the value in register B from register A, storing the result in register A.
*   **JUMP \[address]:** Overwrites the instruction address register, causing the program to "jump" to a new location.
* **JUMP_NEGATIVE \[address]:** Jumps to the specified address only if the ALU's negative flag is set to true.
*   **HALT:** Stops the CPU from processing.

## 🔄 Program Execution
*   The CPU steps through instructions in the order they are given.
*   A program is simply a sequence of instructions.
*   **Loops** can be created by using `JUMP` instructions, which can cause the same sequence of instructions to repeat.
    * An **infinite loop** is a program that runs forever because of a repeating jump.
*   **Conditional jumps**, like `JUMP_NEGATIVE`, allow programs to perform different actions based on conditions.
*  By using `JUMP_NEGATIVE` in combination with a `SUBTRACT` instruction, the program can loop until the result of the subtraction is negative.

## 🔢 Example Program
*   The episode steps through several example programs.
*   One program adds two numbers together.
*   Another program counts up by repeatedly adding one.
*   A final program calculates the remainder of dividing 11 by 5 by using a conditional jump.
    *  This program executes 13 instructions but is only 7 instructions long due to looping.
    *  This demonstrates that software can provide functionality that the hardware does not, such as division.
*   The same program could be used to calculate the remainder of any two numbers.

## ⚖️ Instruction Set Limitations
*   The hypothetical CPU is limited because it only uses 8-bit instructions, with 4 bits for the opcode and 4 bits for addresses, so it can only have 16 instructions and address 16 memory locations.
*  Real, modern CPUs use larger instructions with more bits (32 or 64 bits), called the **instruction length**.
*  Modern CPUs also use **variable length instructions**, with opcodes that may be different lengths.
    *  An instruction can include an **immediate value**, which is saved in memory right after the instruction.

## 🚀 Real CPU Example
*   The **Intel 4004**, the first single-chip CPU released in 1971, used 46 instructions, many similar to the ones covered in the episode, including `JUMP`, `ADD`, `SUBTRACT` and `LOAD`.
    * The 4004 also used 8-bit immediate values.
*   Modern CPUs, like Intel Core i7, have thousands of instructions and variants, with instructions ranging from 1 to 15 bytes in length.
    *   There are dozens of opcodes for different types of additions.

## 💫 Abstraction and Power
*   The growth in instruction set size is due to added features to processor designs over time.
*   **Software** can give a computer functionality that it does not have in its hardware (like division).
*   Software allows new levels of abstraction.

This episode shows how software instructions control the hardware of the CPU to perform complex operations, emphasizing the crucial role of instructions, jumps, and loops, and how these have evolved from simple 8 bit instructions to much more complex instruction sets.
