This episode dives into the world of **software**, the "softer" side of computing that allows us to interact with hardware in more versatile ways. We move from the raw, binary instructions that computers understand to the human-readable languages we use to program them.

## From Hardware to Software ⚙️➡️ 💽

- Early computing involved programming directly in **machine language** (or machine code), the raw binary instructions that CPUs natively speak. This was cumbersome and inflexible.
- Programmers wrote out instructions in English (or another high-level language) called **Pseudo-Code**, then translated them by hand to binary using **opcode tables**. 🤯
- This tedious process led to the development of **assembly languages**, which used **mnemonics** (simple names for opcodes) and **operands** instead of binary. For example, `LOAD_A 14` instead of `0010 1110`.
- **Assemblers** were created as helper programs that automatically translate text-based assembly language into machine code. They also helped with things like automatically figuring out **JUMP addresses** by using labels.
- While assembly language is more human-readable, it is still a very thin veneer over machine code with a one-to-one mapping to machine instructions, and it is inherently tied to the underlying hardware.

## The Rise of High-Level Languages 📈

- **Dr. Grace Hopper** developed the first high-level programming language, A-0, and the first **compiler** in 1952.
- A **compiler** translates "source" code written in a high-level language to a low-level language, like assembly or machine code.
- A single line of code in a high-level language can result in dozens of instructions being executed by the CPU.
- High-level languages, like **Python**, use variables instead of registers and memory locations. The compiler handles those details, making programming much simpler.
- **FORTRAN** ("Formula Translation") was released by IBM in 1957 and became the first widely used high-level language. Programs written in FORTRAN were 20 times shorter than equivalent assembly code.
- **COBOL** (Common Business-Oriented Language) was created to allow programs to be written once and run anywhere. This "write once, run anywhere" concept is a benefit of moving away from assembly and machine code which is CPU specific.
    - Each computer architecture required a unique COBOL compiler, but all compilers could accept the same COBOL source code.

## Impact and Abstraction 🤯

- High-level languages reduced the barrier to entry for programming, allowing people from many fields to incorporate computation into their work.
- **Abstraction** in programming enabled computer experts to create increasingly sophisticated programs that would have been incredibly difficult to write in assembly code.
- Programming languages have continued to evolve, with languages like **ALGOL, LISP, BASIC, Pascal, C, Smalltalk, C++, Objective-C, Perl, Python, Ruby, Java, Swift, C#,** and **Go** emerging over time. Each new language attempts to leverage new abstractions to make programming easier or more powerful.
- The "holy grail" of programming is using plain English to tell a computer what to do. 🗣️➡️💻

## Conclusion and Next Steps 🎬

This episode sets the stage for future explorations of how programming languages and software are used to create incredible things. The next episodes will continue to build an understanding of these concepts.
