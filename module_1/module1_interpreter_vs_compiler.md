# Module 1: Interpreter vs Compiler

## 1. Introduction
Understanding the difference between interpreters and compilers is fundamental to learning how programming languages are executed. Python is an interpreted language, but it's important to know how both approaches work.

---

## 2. What is an Interpreter?
- An interpreter translates and executes code **line by line**.
- It does not produce a separate machine code file; instead, it runs the code directly.
- Errors are reported as soon as they are encountered, making debugging easier for beginners.
- Example languages: Python, JavaScript, Ruby, PHP.

### How Python Uses an Interpreter
- Python source code (`.py` files) is executed by the Python interpreter.
- The interpreter converts code to an intermediate form called **bytecode**, which is then executed by the Python Virtual Machine (PVM).
- No separate compilation step is required.

---

## 3. What is a Compiler?
- A compiler translates the entire source code into **machine code** (or intermediate code) before execution.
- Produces an executable file (e.g., `.exe` on Windows).
- Errors are reported after the entire code is analyzed.
- Example languages: C, C++, Java (compiles to bytecode, then interpreted by JVM).

### Compilation Process
- Source code → Compiler → Machine code (executable)
- The executable can be run multiple times without recompiling.

---

## 4. Key Differences
| Feature                | Interpreter                        | Compiler                          |
|------------------------|------------------------------------|-----------------------------------|
| Translation            | Line by line                       | Whole program at once             |
| Output                 | No separate file                    | Generates executable file         |
| Error Detection        | Stops at first error                | Reports all errors after analysis |
| Execution Speed        | Slower (interpreted every time)     | Faster (runs compiled code)       |
| Memory Usage           | Less (no executable stored)         | More (stores executable)          |
| Example Languages      | Python, JS, Ruby                    | C, C++, Java                      |

---

## 5. Python: Interpreted Language
- Python code is executed by the interpreter, making it easy to test and debug.
- No need to compile before running scripts.
- Interactive mode (REPL) allows quick experimentation.

## 6. How Python Code is Executed
1. **Source Code**: You write Python code in a text file with a `.py` extension.
2. **Interpreter**: When you run the code, the Python interpreter reads the file.
3. **Tokenization**: The interpreter breaks the code into tokens (keywords, operators, etc.).
4. **Parsing**: The tokens are analyzed to create a parse tree, representing the code structure.
5. **Bytecode Compilation**: The parse tree is compiled into bytecode, a low-level representation.
6. **Execution**: The bytecode is executed by the Python Virtual Machine (PVM).
7. **Error Handling**: If an error occurs during execution, the interpreter stops and displays an error message, allowing the programmer to fix the issue.
8. **Output**: The result of the execution is returned to the user, whether it's a printed output or a returned value from a function.
9. **Garbage Collection**: Unused memory is reclaimed by the garbage collector, which automatically manages memory allocation and deallocation.

---

## Summary
- **Interpreter:** Executes code line by line, easier for beginners, slower execution.
- **Compiler:** Converts code to machine code before execution, faster but less flexible for rapid testing.
- Python uses an interpreter, which is why you can run scripts directly without compiling.

---

*Prepared by Zaid Kamil.*