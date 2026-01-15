# eXpOS – Stage 7: ABI and Executable Format

This repository contains my implementation of **Stage 7** of the **eXpOS (Experimental Operating System)** project developed at NIT Calicut.

## 🎯 Objective of Stage 7
The objective of Stage 7 is to understand and implement the **Application Binary Interface (ABI)** and the **executable file format** used by eXpOS.

This stage ensures that **user programs, libraries, and the OS kernel follow a common convention** for execution, memory layout, and system call interaction.

---

## 🧩 Key Concepts Implemented

### 1. Application Binary Interface (ABI)
- Defines a standard interface between:
  - User programs
  - Library code
  - Kernel
- Specifies:
  - Register usage conventions
  - Stack layout
  - Parameter passing mechanism
  - Return value conventions

### 2. Executable File Format
- User programs are stored as **`.xsm` executable files**
- Executables follow a predefined memory layout
- Entry point address is fixed according to ABI rules

### 3. Register Conventions
- Dedicated registers used for:
  - Stack pointer
  - Return address
  - System call arguments
- Ensures consistency across user and kernel code

### 4. Stack and Memory Layout
- User stack is initialized as per ABI
- Code, stack, and heap regions are clearly separated
- Paging is configured to respect ABI-defined regions

### 5. INIT Program Execution
- INIT program compiled using ABI-compliant format
- Loaded into memory by the OS startup module
- Executed in **user mode** following ABI rules

---

## 🧠 Concepts Learned
- Importance of ABI in operating systems
- Executable loading and entry point handling
- Register and stack discipline
- Interaction between user programs and kernel

---

## 🛠 Tools & Environment
- SPL (System Programming Language)
- XSM Simulator
- xfs-interface
- Docker / Colima (macOS)
- Linux-based environment

---

## ▶️ How to Run
1. Compile user programs using ABI-compliant SPL compiler
2. Load library, INIT program, and OS startup code using `xfs-interface`
3. Boot the XSM machine
4. Verify correct execution of ABI-compliant user programs

---

## 📚 References
- eXpOS Documentation: https://exposnitc.github.io/expos-docs/
- eXpOS Roadmap: https://exposnitc.github.io/Roadmap.html

---

## 👩‍💻 Author
**Poojitha Penmetsa**


