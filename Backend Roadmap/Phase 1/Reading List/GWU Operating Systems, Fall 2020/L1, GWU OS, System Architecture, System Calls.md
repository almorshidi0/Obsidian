This lecture lays the foundation for understanding how software interacts on modern systems, focusing on the architecture and structure of operating systems. It moves beyond just memorization and dives deep into logical and critical thinking.

## 🤔 What is the Focus of Operating Systems?

- **Logical Thinking**: Deductions from parts to the whole system. 🧩
- **Relationships**: Understanding how different system aspects relate. 🔗
- **Critical Thinking**: Analyzing trade-offs and design choices. 🤔
- **Less on Memorization**: Focus is on building structures of thought. 🧠

## 🧱 Atoms vs. Molecules Analogy

The lecture uses an analogy of atoms and molecules to explain system architecture:

- **Atoms**: The smallest units provided by the hardware. ⚛️
    - Examples: Registers, stacks, dual-mode execution, system calls, interrupts, I/O, DMA, exceptions, page tables, virtual address spaces, cache lines, atomic instructions.
- **Molecules**: Compositions of different atoms. 🧪
    - Examples: Networking stacks, file systems.
- **Full Systems**: Built from molecules. 🏢
    - The goal is to understand the logic behind how systems are structured, from the hardware level to the full systems we use today.

## 🥪 The Operating System Sandwich

The operating system is conceptualized as a sandwich:

- **Top Bread**: Applications (boring, caloric, horrible bread) 🍞
- **Bottom Bread**: Hardware (boring, empty calories) ⚙️
- **Filling**: The Operating System (the interesting stuff) 🥬🍅🥩

This leads to two key questions: * How do operating systems and applications interact? ❓ * How do operating systems and hardware (especially I/O) interact? ❓

The lecture focuses on the **top interaction** between applications and the OS.

## 💻 How Normal Computations Work

To understand OS interactions, we look at how simple C programs execute:

- **Execution Stack**: Function calls manipulate an execution stack.
- **Registers**: EIP, EAX, EDX (32-bit x86 microarchitecture).
- **Stack**: Used to store local variables and function call information.
    - **Activation Record**: Stores local variables for a function on the stack while it's active.
- **Function Calls**: Arguments are pushed onto the stack, return addresses are also pushed onto the stack and then execution jumps to the function's code. Local variables are stored on the stack as part of the activation record.
- **Calling Convention (Cdecl)**: Determines how arguments and return values are allocated (registers or stack).

### Storage Hierarchy

- Registers: Fastest, smallest. Managed by the compiler.
- L1/L2/L3 Cache: Fast, medium size. Managed by hardware.
- Memory: Large, slower. Managed by the operating system.
- Solid State Drives/Magnetic Hard Drives: Slowest, largest. Managed by the operating system. The goal is to achieve access speed of registers with storage of disk. The compiler tries to keep things in registers as much as possible and pushes things onto the stack when it needs to.

## 🛡️ Why Separate the OS from User Applications?

- **Protection**: Applications need to be protected from each other.
- **Resource Management**: The OS manages resources like memory among applications.
- **Kernel Protection**: The OS needs to be protected from applications.

## 🔒 Dual-Mode Protection

- **User Mode**: Where user-level applications run.
- **Kernel Mode**: Where the operating system runs.
- A single bit in the processor indicates the current mode.
- **User Mode Restrictions**: Cannot access kernel memory.
- **Kernel Mode Powers**: Access to kernel memory and protected instructions.

## 📞 System Calls

- **Controlled Switching**: Special ISA instructions (system calls) are needed to switch between user and kernel mode.
- **System Call Process**:
    1. User-level application executes a system call instruction.
    2. Switches to Kernel Mode (mode bit set to 0).
    3. Starts executing at a fixed system call address in the kernel.
    4. The kernel performs the requested action.
    5. A special instruction returns execution back to the user level.
- **Separate Kernel Stack**: A separate stack is used by the kernel for system calls.
    - User-level data is copied onto the kernel stack.
- **Traps**: Mechanisms to switch from user to kernel level
    - Traps include system calls, exceptions and interrupts
    - **Software-triggered events**: Exceptions and System calls
        - **Exceptions**: CPU errors (e.g. divide by zero, segmentation faults).
        - **System Calls**: Deliberate requests by a program to access the kernel (e.g. write).
    - **Interrupts**: Hardware device state changes.

## 📝 System Call Example: `printf`

- `printf` (a C library function) eventually calls the `write` system call.
- **Steps:**
    1. `printf` calls `write` in the C library.
    2. The `write` function puts the system call number (e.g., 4 for `write`) in a register.
    3. The file descriptor, and the string address are either put into registers or pushed onto the stack.
    4. System call ISA instruction is invoked (`sysenter` or `int`).
    5. The system switches to kernel mode and starts executing at a kernel-defined system call instruction address.
    6. The kernel looks up the system call in the system call table and invokes the function.
    7. After completing the system call the kernel then returns to user level.
- **Return from System Call**: Special instructions restore application registers and return to user level.

## 👾 xv6 Example

- `write` is implemented in assembly in `uces.s` which puts 16 into the `eax` register before invoking a system call.
- The `int` instruction traps the kernel and the xv6 kernel starts executing at `alltraps` in `trapasm.s`..
- Registers are pushed onto the stack and then the `trap` function in `trap.c` is called.
- The kernel decides which system call to make by looking up the `syscall` array of function pointers and invoking the corresponding function.

## 🔑 Key Takeaways

- Function calls use calling conventions and the stack.
- System calls are needed because we need to isolate the kernel and protect the kernel from applications.
- Dual-mode execution provides this isolation.
- System calls allow user applications to invoke kernel functions safely.

This lecture provides a strong base for the rest of the course, focusing on the core concepts and mechanisms that drive operating systems. 🚀