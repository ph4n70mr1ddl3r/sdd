# Hello World Program

A simple C++ program demonstrating code quality, testing standards, and consistent user experience.

## Overview

This project implements a basic "Hello, World!" program in C++17 that serves as a foundational example for:
- Modern C++ development practices
- Test-driven development (TDD) with Catch2
- CMake and Makefile build systems
- Clear, maintainable code structure

## Requirements

- **C++ Compiler**: g++ 7+ or clang++ 5+
- **Build Tools**: Make (for simple builds) or CMake 3.10+ (for advanced builds)
- **Platform**: Linux, macOS, Windows (with appropriate compiler)

## Quick Start

### Build and Run

#### Using Make (Simplest)
```bash
make              # Build the program
./hello-world     # Run it
make test         # Build and run tests
```

#### Using CMake (Standard)
```bash
mkdir build
cd build
cmake ..
make              # or cmake --build .
./bin/hello-world # Run the program
make test         # Run tests
```

## Expected Output

```bash
$ ./hello-world
Hello, World!
$ echo $?
0
```

## Build Targets

### Makefile Targets
- `make` - Build the hello-world executable
- `make test` - Build and run unit tests
- `make run` - Build and run the program
- `make clean` - Remove build artifacts
- `make help` - Show available targets

### CMake Build Targets
- `cmake --build build` - Build all targets
- `cmake --build build --target test` - Run tests
- `cmake --build build --target test_run` - Run with detailed output

## Project Structure

```
.
├── src/
│   └── hello_world.cpp           # Main program source
├── tests/
│   ├── catch2/
│   │   └── catch.hpp             # Catch2 testing framework
│   ├── unit/
│   │   └── test_hello_world.cpp   # Unit tests
│   └── integration/
│       └── test_execution.cpp     # Integration tests
├── CMakeLists.txt                # CMake build configuration
├── Makefile                       # Simple Make build script
└── README.md                      # This file
```

## Development

### Test-Driven Development (TDD)

1. **Write tests first** in `tests/unit/test_hello_world.cpp`
   ```bash
   make test  # Tests should initially FAIL
   ```

2. **Implement functionality** in `src/hello_world.cpp` to make tests pass

3. **Verify tests pass**
   ```bash
   make test  # All tests should now PASS
   ```

### Testing Commands

```bash
# Run all tests
make test

# Build and run with CMake
cd build
cmake ..
make test

# Run specific test
./test_runner
```

## Quality Standards

This project adheres to three core principles:

### I. Code Quality & Maintainability
- Modern C++17 practices
- Clear, descriptive naming
- Comprehensive comments
- Simple, understandable structure

### II. Rigorous Testing Standards
- Tests written before implementation (TDD)
- >80% code coverage target
- Fast test execution (<100ms)
- Catch2 framework for clean test organization

### III. User Experience Consistency
- Predictable output: "Hello, World!"
- Error-free execution (exit code 0)
- Clear, well-documented interface
- Works across multiple environments

## Troubleshooting

### Compiler not found
```bash
# Ubuntu/Debian
sudo apt install g++ make cmake

# macOS
brew install gcc make cmake

# Fedora/RHEL
sudo dnf install gcc-c++ make cmake
```

### Permission denied
```bash
chmod +x hello-world
./hello-world
```

### CMake configuration fails
Ensure you have CMake 3.10 or later:
```bash
cmake --version
```

## Performance

- **Build time**: <1 second
- **Execution time**: <10ms
- **Memory usage**: <1MB

## License

This is an example project for educational purposes.

## Further Reading

- [Catch2 Documentation](https://github.com/catchorg/Catch2)
- [CMake Tutorial](https://cmake.org/cmake/help/latest/guide/tutorial/index.html)
- [C++17 Features](https://en.cppreference.com/)
