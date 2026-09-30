# RAMIPSY - Ramadan Attuwaybi's MIPS Simulator

A MIPS32 assembler and simulator that runs in the browser, on Windows laptops,
Android phones and tablets. Nothing to install, and it keeps working offline
after the first visit. 

- **Programmer:** Eng. Ramadan Attuwaybi
- **Course:** EE434 - University of Tripoli - Faculty of Engineering - Department of EEE
- **Fall 2026-2027 - Version 1.1 - 01-10-2026**

## Features

- Integer MIPS32 instruction set plus common pseudo-instructions (`li`, `la`, `move`, `blt`, `bge`, …)
- MARS-compatible memory layout (`.text` at `0x00400000`, `.data` at `0x10010000`) and syscall numbers
- Run, step, step back, pause, reset and breakpoints
- Registers, data memory, labels and machine code (hex, with R/I/J field breakdown)
- Console input and output (syscalls 1, 4, 5, 8, 9, 10, 11, 12, 17, 30, 32, 34–36, 40–42)
- Clear assembler and runtime error messages with line numbers



RAMIPSY - Ramadan Attuwaybi's MIPS Simulator
EE434 Computer Architecture and Organization - University of Tripoli
Version 1.1
======================================================================

LINK
  https://ramadan-att.github.io/ramipsy/

  Works on Windows laptops, Android phones/tablets and iPhones.
  Nothing to install. Open the link once while online; after that it
  also works without internet.

INSTALL IT AS AN APP (recommended)
  Android (Chrome) : menu (3 dots) > "Add to Home screen" / "Install app"
  iPhone (Safari)  : Share button > "Add to Home Screen" > Add

WRITING AND RUNNING A PROGRAM
  1. Write your code in the Edit tab, or choose a program from Examples.
  2. Press Assemble (F3). Errors appear under Messages; tap an error to
     jump to its line.
  3. Press Run (F5) to run the whole program, or
     Step (F7) to run one instruction at a time.
     Back (F8) undoes the last instruction. Reset (F4) starts again.
  4. When the program asks for input, type it in the Input box under
     the console and press Enter.

WHAT YOU SEE
  Execute   : the machine code. The yellow row is the NEXT instruction.
              Tap the small circle on a row to set a breakpoint.
              Below it: memory (data segment) and your labels.
  Registers : all 32 registers plus pc, hi, lo. Green = just changed.
              Switch between Hex and Dec at the top.
  Console   : Run I/O shows your program's output.
              Messages shows assembler and runtime errors.
  Speed     : choose a slow speed to watch the program run step by step.

MOST USED SYSCALLS  (put the number in $v0, then write: syscall)
  1  print integer   ($a0 = value)
  4  print string    ($a0 = address of the string)
  5  read integer    (result in $v0)
  8  read string     ($a0 = buffer, $a1 = size)
  11 print character ($a0 = character)
  10 exit
  Full list: press Help inside RAMIPSY.

MEMORY LAYOUT (same as MARS)
  .text starts at 0x00400000     .data starts at 0x10010000
  $sp starts at 0x7fffeffc       $gp = 0x10008000

IMPORTANT
  - Your code is kept in the browser, but browsers can clear it.
    Use Save (or Copy) to keep your own copy of important programs.
  - Only integer instructions are supported (no floating point).
  - Programs written for MARS run in RAMIPSY without changes.

----------------------------------------------------------------------
Programmer: Eng. Ramadan Attuwaybi
EE434 - University of Tripoli - Faculty of Engineering - Department of EEE
Fall 2026-2027
