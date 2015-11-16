# PaZcal-Compiler
Compiler for the imaginary language PaZcal 


This is a compiler for the imaginary language PaZcal, which was created with the contribution of Kostis Lolos (lolosk). The compiler generates Intel i386 assembly, which uses GNU assembler syntax. In order to run the executable of the Compiler, you must execute 'make' in the central folder. 

In order to compile a program execute: ./pazcal program.pz 
The above produces code without optimizations and creates two files with endings .imm (for the intermediate code) and .asm (for the final code). The assembly produced is 32bit. So, the press: as program.asm -o program.o --32. Then, in order to produce the executable code use: ld -m elf_i386 program.o lib/*.o -o program.

Our compiler supports 4 flags, which alter its use: 

1. -d: debugging mode: prints in standard output both the intermediate and the final code + the type of the variables used

2. -i: prints intermediate code in standard output

3. -f: prints final code in standard output

4. -o: activates optimizations of intermediate code

Flags d, i, f cannot be used together. Flag o can be used together with one of the rest of the flags. 

Read the report.pdf for more information.
