# 42 Warmup

A comprehensive collection of warmup exercises for 42 School, featuring solutions to **Piscine Reloaded** and **P2P-101** modules. This repository serves as a foundational review of C programming concepts and peer-to-peer evaluation practices.

## 📋 Description

This repository contains completed exercises from the 42 School warmup curriculum, designed to refresh and strengthen fundamental programming skills before diving into the main curriculum. It includes both technical C programming challenges and reflective exercises on communication and peer evaluation.

## 🛠️ Technology Stack

- **Language**: C (C89/C90 standard)
- **Build System**: Make
- **Compiler**: Clang with flags `-Wall -Wextra -Werror`
- **Shell Scripting**: Bash
- **Tools**:
  - Standard UNIX utilities (`find`, `grep`, `awk`, `ifconfig`)
  - Archive tools (`tar`)
  - File I/O operations

## 📁 Project Structure

```
42_warmup/
├── piscine_reloaded/     # C programming exercises (ex00-ex27)
│   ├── ex00/             # Basic shell commands and tar archives
│   ├── ex01-ex05/        # Shell scripting fundamentals
│   ├── ex06-ex08/        # Basic output functions
│   ├── ex09-ex11/        # Pointer manipulation
│   ├── ex12-ex14/        # Algorithms (factorial, sqrt)
│   ├── ex15-ex19/        # String manipulation and arguments
│   ├── ex20-ex21/        # Dynamic memory allocation
│   ├── ex22-ex23/        # Header files and structures
│   ├── ex24/             # Library creation with Makefile
│   ├── ex25-ex26/        # Function pointers
│   └── ex27/             # File I/O operations
└── p2p-101/              # Peer-to-peer evaluation scenarios
    ├── ex01/             # Non-violent communication
    └── ex02/             # Peer evaluation scenarios (15 scenarios)
```

## 🎯 Key Features

### Piscine Reloaded (27 Exercises)

1. **Shell Basics** (ex00-ex05):
   - File creation and manipulation
   - Shell script writing
   - Pattern matching with special characters

2. **Core C Functions** (ex06-ex11):
   - Character and number printing
   - Pointer operations
   - Basic mathematical operations

3. **Algorithms** (ex12-ex14):
   - Iterative and recursive factorial
   - Square root calculation

4. **String Operations** (ex15-ex21):
   - String output and comparison
   - Dynamic memory allocation
   - String duplication and range creation

5. **Advanced Concepts** (ex22-ex27):
   - Macro definitions
   - Structure definitions
   - Static library creation
   - Function pointers
   - File display utility

### P2P-101 Module

- **Communication Skills**: Reflections on non-violent communication in peer evaluation contexts
- **Evaluation Scenarios**: 15 real-world peer evaluation scenarios covering:
  - Time management during evaluations
  - Handling disagreements professionally
  - Providing constructive feedback
  - Dealing with technical issues
  - Maintaining integrity in peer reviews

## 🚀 Getting Started

### Prerequisites

- GCC compiler (or compatible C compiler)
- Make build system
- UNIX-like operating system (Linux, macOS)
- Basic understanding of C programming

### Compilation

Most exercises can be compiled individually. For exercises with Makefiles:

```bash
# For ex24 (library)
cd piscine_reloaded/ex24
make

# For ex27 (file display)
cd piscine_reloaded/ex27
make
```

For individual C files without Makefiles:

```bash
# Example compilation
cc -Wall -Wextra -Werror ft_function.c -o ft_function
```

### Running Shell Scripts

```bash
# Make the script executable
chmod +x script.sh

# Run the script
./script.sh
```

## 💡 Exercise Highlights

### Notable Implementations

- **ex12/ex13**: Factorial functions demonstrating both iterative and recursive approaches
- **ex14**: Integer square root calculation with overflow protection
- **ex19**: Command-line argument sorting using bubble sort
- **ex24**: Complete static library (`libft.a`) with modular architecture
- **ex25/ex26**: Function pointer usage for higher-order functions
- **ex27**: Robust file display utility with error handling

### Code Quality Standards

All C code follows the **42 Norm** (Norminette):
- Maximum 25 lines per function
- Maximum 80 characters per line
- Specific naming conventions for variables and functions
- Header files with include guards
- Proper indentation and formatting
- English variable names and comments

## 🧪 Testing

Each exercise should be tested with:
- **Normal cases**: Standard input/output
- **Edge cases**: NULL pointers, empty strings, boundary values
- **Error handling**: Invalid inputs, memory allocation failures
- **Memory leaks**: Use `valgrind` for dynamic memory exercises

Example testing:

```bash
# For factorial functions
cc -Wall -Wextra -Werror ft_iterative_factorial.c main.c
./a.out

# For memory leak detection
valgrind --leak-check=full ./program
```

## 📚 Learning Outcomes

By completing these exercises, you will:

- ✅ Master fundamental C programming concepts
- ✅ Understand memory management and pointers
- ✅ Write clean, normed code following strict standards
- ✅ Create and use Makefiles for project builds
- ✅ Implement algorithms recursively and iteratively
- ✅ Work with function pointers and callbacks
- ✅ Practice effective peer evaluation techniques
- ✅ Apply non-violent communication principles

## 🤝 Contributing

This repository represents personal solutions to 42 School exercises. While direct contributions are not expected, you are welcome to:

- Use this as a reference for learning
- Report issues or suggest improvements
- Share alternative approaches (via issues/discussions)

**Note**: If you are a current 42 student, please complete the exercises independently before consulting external solutions.

## 📖 P2P-101 Scenarios

The P2P-101 module includes reflective exercises on:
- Handling absent evaluators
- Managing time pressure during evaluations
- Dealing with failed evaluations constructively
- Resolving interpretation differences
- Addressing suspected cheating
- Providing meaningful feedback
- Testing in different environments
- Supporting less experienced peers

These scenarios prepare students for the collaborative, peer-driven learning environment at 42 School.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
Copyright (c) 2025 Pedro Monteiro
```

## 🎓 Author

**Pedro Monteiro** (peda-cos)
- 42 School Student
- Completion Date: October 2024

---

**Note**: This repository is part of the 42 School curriculum. The exercises and structure follow the official 42 Network pedagogy and evaluation system.
