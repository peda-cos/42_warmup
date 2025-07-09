# 🏊‍♂️ 42 Warmup Project

[![42 School](https://img.shields.io/badge/42-School-000000?style=flat&logo=42&logoColor=white)](https://42sp.org.br)
[![C](https://img.shields.io/badge/C-A8B9CC?style=flat&logo=c&logoColor=white)](https://en.wikipedia.org/wiki/C_(programming_language))
[![License](https://img.shields.io/badge/License-Public%20Domain-blue.svg)](LICENSE)

> A comprehensive collection of 42 School warmup exercises designed to refresh and strengthen fundamental programming concepts.

## 📋 Table of Contents

- [🎯 Overview](#-overview)
- [📁 Project Structure](#-project-structure)
- [⚙️ Prerequisites](#️-prerequisites)
- [🚀 Installation](#-installation)
- [💻 Usage](#-usage)
- [🧪 Testing](#-testing)
- [📚 Exercises](#-exercises)
- [🤝 Peer Evaluation Guide](#-peer-evaluation-guide)
- [🛠️ Development](#️-development)
- [📖 Resources](#-resources)
- [⚖️ License](#️-license)

## 🎯 Overview

This project serves as a comprehensive warmup for 42 School students, covering:

- **C Programming Fundamentals**: Basic functions, algorithms, and data structures
- **System Administration**: Shell scripting and file operations
- **Peer Evaluation Skills**: Practical scenarios for conducting fair and constructive evaluations

Perfect for indie developers looking to solidify their programming foundations or prepare for technical interviews! 🎓

## 📁 Project Structure

```
42_warmup/
├── 📄 README.md                 # You are here!
├── 📄 LICENSE                   # Public domain license
├── 📂 piscine_reloaded/        # C programming exercises (ex00-ex27)
│   ├── 📂 ex00-ex05/           # Shell & basic setup
│   ├── 📂 ex06-ex21/           # Core C functions
│   ├── 📂 ex22-ex23/           # Headers & structures
│   ├── 📂 ex24/                # Library project with Makefile
│   ├── 📂 ex25-ex26/           # Function pointers
│   └── 📂 ex27/                # File operations
└── 📂 p2p-101/                # Peer evaluation training
    ├── 📂 ex01/                # Communication guidelines
    └── 📂 ex02/                # Evaluation scenarios
```

## ⚙️ Prerequisites

### System Requirements
- **OS**: Linux, macOS, or WSL2 on Windows
- **Compiler**: Clang with C99 standard support
- **Shell**: Bash (for shell scripts)
- **Memory**: Minimum 512MB RAM
- **Storage**: ~50MB free space

### Development Tools
```bash
# Essential tools
sudo apt update && sudo apt install -y \
    clang \
    make \
    libc6-dev \
    gdb \
    valgrind \
    git
```

## 🚀 Installation

### Quick Start

```bash
# Clone the repository
git clone https://github.com/yourusername/42_warmup.git
cd 42_warmup

# Make all scripts executable
find . -name "*.sh" -type f -exec chmod +x {} \;

# Test compilation (ex24 - library project)
cd piscine_reloaded/ex24
make
ls -la libft.a  # Should see the compiled library
cd ../..
```

### Alternative: Direct Download

```bash
# Download as ZIP
wget https://github.com/yourusername/42_warmup/archive/main.zip
unzip main.zip
cd 42_warmup-main
```

## 💻 Usage

### 🔧 Compiling Individual Exercises

Most exercises can be compiled standalone:

```bash
# Basic function compilation
cd piscine_reloaded/ex12
gcc -Wall -Wextra -Werror -o test ft_iterative_factorial.c main.c
./test

# For exercises requiring ft_putchar
cd piscine_reloaded/ex06
gcc -Wall -Wextra -Werror -o test ft_print_alphabet.c ft_putchar.c
./test
```

### 📦 Building the Complete Library (ex24)

```bash
cd piscine_reloaded/ex24

# Build the library
make

# Clean object files
make clean

# Clean everything
make fclean

# Rebuild from scratch
make re
```

### 🗃️ File Display Utility (ex27)

```bash
cd piscine_reloaded/ex27

# Build the utility
make

# Display a file
./ft_display_file filename.txt

# Test error cases
./ft_display_file                    # Should show "File name missing."
./ft_display_file file1.txt file2.txt  # Should show "Too many arguments."
```

### 🐚 Running Shell Scripts

```bash
# Find all .sh files (ex03)
cd piscine_reloaded/ex03
./find_sh.sh

# Get MAC addresses (ex04)
cd piscine_reloaded/ex04
./MAC.sh

# Clean temporary files (ex02)
cd piscine_reloaded/ex02
bash clean  # Removes files ending with ~ and #*#
```

## 🧪 Testing

### Automated Testing Script

Create a simple test runner:

```bash
#!/bin/bash
# save as test_runner.sh

echo "🧪 Running 42 Warmup Tests..."

# Test library compilation
echo "📦 Testing library compilation..."
cd piscine_reloaded/ex24
if make > /dev/null 2>&1; then
    echo "✅ Library compiled successfully"
    make clean > /dev/null
else
    echo "❌ Library compilation failed"
fi
cd ../..

# Test file display utility
echo "🗃️ Testing file display utility..."
cd piscine_reloaded/ex27
if make > /dev/null 2>&1; then
    echo "✅ ft_display_file compiled successfully"
    # Test with this README
    echo "📄 Testing file display..."
    ./ft_display_file ../../README.md | head -5
    make clean > /dev/null
else
    echo "❌ ft_display_file compilation failed"
fi
cd ../..

echo "🎉 Testing complete!"
```

### Manual Testing Examples

```bash
# Test factorial functions
cd piscine_reloaded/ex12
cat > test_factorial.c << 'EOF'
#include <stdio.h>
int ft_iterative_factorial(int nb);

int main() {
    printf("5! = %d\n", ft_iterative_factorial(5));  // Should be 120
    printf("0! = %d\n", ft_iterative_factorial(0));  // Should be 1
    printf("-1! = %d\n", ft_iterative_factorial(-1)); // Should be 0
    return 0;
}
EOF

gcc -o test ft_iterative_factorial.c test_factorial.c
./test
rm test test_factorial.c
```

## 📚 Exercises

### 🏗️ Foundation Exercises (ex00-ex05)

| Exercise | Description | Key Concepts |
|----------|-------------|--------------|
| **ex00** | TAR archive | File compression |
| **ex01** | Print 'Z' | File output |
| **ex02** | Clean script | File pattern matching |
| **ex03** | Find .sh files | Shell scripting |
| **ex04** | MAC addresses | Network commands |
| **ex05** | Special characters | File naming |

### 🧠 Core C Programming (ex06-ex21)

| Exercise | Function | Description |
|----------|----------|-------------|
| **ex06** | `ft_print_alphabet` | Print a-z |
| **ex07** | `ft_print_numbers` | Print 0-9 |
| **ex08** | `ft_is_negative` | Check if number is negative |
| **ex09** | `ft_ft` | Set pointer to 42 |
| **ex10** | `ft_swap` | Swap two integers |
| **ex11** | `ft_div_mod` | Division and modulo |
| **ex12** | `ft_iterative_factorial` | Iterative factorial |
| **ex13** | `ft_recursive_factorial` | Recursive factorial |
| **ex14** | `ft_sqrt` | Integer square root |
| **ex15** | `ft_putstr` | Print string |
| **ex16** | `ft_strlen` | String length |
| **ex17** | `ft_strcmp` | String comparison |
| **ex18** | `ft_print_params` | Print program arguments |
| **ex19** | `ft_sort_params` | Sort and print arguments |
| **ex20** | `ft_strdup` | Duplicate string (malloc) |
| **ex21** | `ft_range` | Create integer array |

### 🗂️ Advanced Concepts (ex22-ex27)

| Exercise | Topic | Description |
|----------|-------|-------------|
| **ex22** | Macros | `ABS` macro definition |
| **ex23** | Structures | Point structure |
| **ex24** | Makefile | Complete library project |
| **ex25** | Function pointers | `ft_foreach` |
| **ex26** | Function pointers | `ft_count_if` |
| **ex27** | File I/O | Display file contents |

## 🤝 Peer Evaluation Guide

The `p2p-101` section contains practical scenarios for conducting effective peer evaluations:

### 📖 Communication Principles (ex01)

Key concepts from Non-Violent Communication:
- **Active listening** 👂
- **Empathy and mutual understanding** 💝
- **Respectful dialogue** 🤝
- **Emotional awareness** 🧠

### 🎭 Evaluation Scenarios (ex02)

Practice scenarios covering:
- **No-show situations** 🕐
- **Time management** ⏰
- **Technical difficulties** 🔧
- **Academic integrity** 📚
- **Constructive feedback** 💬

## 🛠️ Development

### 🎨 Code Style Guidelines

This project follows 42 School's strict coding standards:

```c
/* Standard 42 header */
/* ************************************************************************** */
/*                                                                            */
/*                                                        :::      ::::::::   */
/*   filename.c                                         :+:      :+:    :+:   */
/*                                                    +:+ +:+         +:+     */
/*   By: username <marvin@42.fr>                    +#+  +:+       +#+        */
/*                                                +#+#+#+#+#+   +#+           */
/*   Created: YYYY/MM/DD HH:MM:SS by username          #+#    #+#             */
/*   Updated: YYYY/MM/DD HH:MM:SS by username         ###   ########.fr       */
/*                                                                            */
/* ************************************************************************** */

// Function implementation follows...
```

**Key Rules:**
- Maximum 25 lines per function
- Maximum 80 characters per line
- No more than 5 functions per file
- Strict error handling
- No global variables

### 🔍 Debugging Tips

```bash
# Compile with debug symbols
gcc -g -Wall -Wextra -Werror your_file.c

# Use GDB for debugging
gdb ./your_program
(gdb) break main
(gdb) run
(gdb) step

# Memory leak detection
valgrind --leak-check=full ./your_program

# Static analysis
cppcheck --enable=all your_file.c
```

### 🏃‍♂️ Performance Optimization

```bash
# Compile with optimization
gcc -O2 -Wall -Wextra -Werror your_file.c

# Profile your code
time ./your_program
```

## 📖 Resources

### 📚 Learning Materials

- [C Programming Language (K&R)](https://en.wikipedia.org/wiki/The_C_Programming_Language)
- [42 School Documentation](https://42.fr)
- [GCC Manual](https://gcc.gnu.org/onlinedocs/)
- [Makefile Tutorial](https://www.gnu.org/software/make/manual/)

### 🔗 Useful Links

- [C Reference](https://en.cppreference.com/w/c)
- [POSIX Standards](https://pubs.opengroup.org/onlinepubs/9699919799/)
- [Shell Scripting Guide](https://www.shellscript.sh/)
- [Git Best Practices](https://git-scm.com/book)

### 🛠️ Development Tools

```bash
# Recommended VS Code extensions
code --install-extension ms-vscode.cpptools
code --install-extension ms-vscode.makefile-tools
code --install-extension formulahendry.code-runner
```

## 🚀 Deployment

### For Personal Use

```bash
# Create your own fork
git clone https://github.com/yourusername/42_warmup.git
cd 42_warmup

# Add your solutions
git add .
git commit -m "Add: my solutions to warmup exercises"
git push origin main
```

### For Educational Institutions

```bash
# Deploy to a server
scp -r 42_warmup/ user@server:/path/to/course/materials/

# Or use with containers
docker run -v $(pwd):/workspace -it gcc:latest bash
```

## 🤝 Contributing

While this is primarily an educational project, contributions are welcome:

1. 🍴 Fork the repository
2. 🌟 Create a feature branch (`git checkout -b feature/amazing-addition`)
3. 💻 Commit your changes (`git commit -m 'Add: amazing feature'`)
4. 📤 Push to the branch (`git push origin feature/amazing-addition`)
5. 🎯 Open a Pull Request

## ⚖️ License

This project is dedicated to the **public domain**. Feel free to use, modify, and distribute as you see fit! 🎉

See the [LICENSE](LICENSE) file for full details.

---

## 💝 Acknowledgments

- **42 School** for the excellent curriculum design
- **The C Programming Community** for continuous inspiration
- **Fellow 42 students** for peer learning and support

---

<div align="center">

**Happy Coding!** 🚀✨

Made with ❤️ for the 42 Community

[⬆️ Back to Top](#-42-warmup-project)

</div>
