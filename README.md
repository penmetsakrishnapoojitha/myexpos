# eXpOS – Stage 6: User Program Execution

This repository contains my implementation of **Stage 6** of the **eXpOS (Experimental Operating System)** project developed at NIT Calicut.

## 🎯 Objective of Stage 6
The objective of Stage 6 is to enable **execution of user-level programs** in eXpOS.  
This stage introduces **process creation, user–kernel mode switching, and system call handling**, allowing a user program to run correctly on the XSM machine.

## 🧩 Key Concepts Implemented

### 1. User Program Execution
- User programs are written in **SPL**
- Programs execute in **user mode**
- Direct access to kernel memory or hardware is restricted

### 2. INIT Process Creation
- During system boot, the kernel creates the **INIT process**
- A **Process Control Block (PCB)** is initialized
- PCB stores process-related information such as:
  - Process ID
  - State
  - Stack pointer
  - Instruction pointer

### 3. Loading User Program
- The user program is loaded into **user memory**
- Stack and entry point are initialized
- Program Counter is set to the starting instruction

### 4. Kernel → User Mode Switch
- CPU switches from **kernel mode** to **user mode**
- Control is transferred to the user program
- Protection mechanisms prevent illegal access

### 5. System Call Handling
- User programs request kernel services using **software interrupts**
- Control switches to kernel mode
- Kernel executes the requested service
- Control returns to user mode after completion

### 6. Program Termination
- User program terminates using the `Exit` system call
- Process state is updated
- Control returns to the kernel

## 🛠 Tools & Environment
- SPL (System Programming Language)
- XSM Simulator
- Docker / Colima (for macOS)
- Linux-based environment

## ▶️ How to Run
1. Compile SPL modules using the SPL compiler
2. Load kernel and user programs into disk image
3. Boot the XSM machine
4. Observe user program execution through console output

## 📚 References
- eXpOS Documentation: https://exposnitc.github.io/expos-docs/
- eXpOS Roadmap: https://exposnitc.github.io/Roadmap.html

## 👩‍💻 Author
**Poojitha Penmetsa**

