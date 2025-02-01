This episode explores how computers store data using memory circuits. It starts with simple circuits that can store a single bit of information and scales up to complex memory modules used in modern computers, explaining concepts like latches, registers, memory addressing, and Random Access Memory (RAM).

## 💾 The Need for Memory
*   After performing calculations with the Arithmetic Logic Unit (ALU), it's essential to **store the results** for later use.
*   **Random Access Memory (RAM)** is used for active data storage, such as the state of a game, and requires power to maintain the information.
*   **Persistent memory** can store information even without power, and is used for things like long term storage.

## 🎛️ Basic Memory Circuits
*   The episode starts by building circuits that can store one bit of information.
*   A basic **OR gate** with its output fed back into one of its inputs can record a "1" but cannot be changed.
*   An **AND gate** circuit can record a "0" in a similar fashion.

### 🔄 AND-OR Latch
*   Combining the two circuits creates an **AND-OR Latch**.
*   It has two inputs: a "set" input to set the output to 1, and a "reset" input to set the output to 0.
*   If both set and reset are 0, the circuit **remembers the last input**.
*   This is called a "latch" because it "latches onto" a value.
*   The process of putting data into memory is called **writing**, and getting data out is called **reading**.

### 🚦 Gated Latch
*   A **Gated Latch** is a more practical memory circuit with a single data input wire and a write enable wire.
*   The write enable wire acts like a "gate", allowing data to be written into the latch when enabled, and preventing changes when disabled.
*   When the write enable wire is on, data on the data line is saved to the latch.
*  When the write enable line is off, the latch remains unchanged, and the data on the input line has no effect.

## 🗄️ Registers
*   Multiple latches can be combined to store more bits.
*   A **register** is a group of latches that stores a number; for example, eight latches can hold an 8-bit number.
*   The **width** of a register refers to the number of bits it can store.
    * Early computers used 8-bit registers.
    * Modern computers often use registers that are 64-bits wide.
*   A single write enable wire can control all the latches in a register.

## 🧮 Memory Matrix
*   To store a large number of bits, latches are arranged in a **matrix**, like a grid of rows and columns.
*   Each latch is at the intersection of a row and column wire.
*   An **AND gate** is used to activate a single latch at a specific intersection by turning on the corresponding row and column wires.
*   Using this design, a **single shared write enable wire** and a single shared data wire can be used, saving a significant number of wires.
*    A **read enable wire** can be used to read data from a specific latch.
*   Each latch in the grid has a unique **address**, like a street address, which consists of a row address and a column address.

### 🗺️ Memory Addressing
*   A **multiplexer** is used to convert the address into signals that select the correct row and column.
*   The multiplexer connects the input line to a corresponding output line.
*  A multiplexer is needed to handle the rows and another for the columns.

### 📦 Memory Module
*   The 256-bit memory matrix is treated as a single component with an 8-bit address input (4 bits for row, 4 bits for column).
*   The module also has read and write enable wires and a single data wire.

## 🧱 Scaling Up Memory
*   Multiple memory modules can be arranged in a row, with each module storing one bit of a number.
*   For example, 8 memory modules together can store an 8-bit byte.
*  This results in a uniform bank of addressable memory.

### 📍 Random Access Memory (RAM)
*   The memory described in this episode is called **Random Access Memory (RAM)** because any memory location can be accessed at any time and in a random order.
*   RAM is the computer's short-term memory, where it stores data needed for currently running programs and processes.
*  Modern computers scale to gigabytes of memory by packaging smaller bundles of memory into larger arrangements.
*  **32-bit addresses** are needed to address a gigabyte of memory.

### 🔬 Physical Memory
*   A physical stick of RAM contains multiple memory modules.
*   Each module contains multiple squares of memory, and each square is comprised of multiple blocks, and each block has a matrix of individual bits.
*   The discussed stick of RAM from the 1980's has 1 megabyte (8 million bits) of memory.
*  Modern RAM can store gigabytes or more of data.

### ⚡ Types of RAM
*   **SRAM (Static Random-Access Memory)** uses latches to store bits.
*   Other types of RAM include **DRAM, Flash memory, and NVRAM**, which use different circuits like capacitors or charge traps to store bits.
*  All these types of RAM are organized into massively nested matrices of memory cells.

This episode explains the fundamental principles of computer memory, from basic latches to complex memory modules and RAM, and how these are arranged in nested matrices. It highlights the layers of abstraction that make the complexity manageable, like a set of Russian dolls.
