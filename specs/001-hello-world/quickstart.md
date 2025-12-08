# Quickstart Guide: Hello World Program

**Feature**: Hello World Program  
**Date**: 2025-12-09  
**Purpose**: Get started quickly with building and testing the hello world program

## Prerequisites

- C++ compiler (g++ 7+ or clang++ 5+)
- Git (for version control)
- Basic command-line knowledge

## Quick Setup

### 1. Clone and Navigate
```bash
# Assuming you're in the project root
cd /path/to/project
```

### 2. Build with Make (Simplest)
```bash
make
```
This compiles `src/hello_world.cpp` to `hello-world` executable.

### 3. Build with CMake (Standard)
```bash
mkdir -p build
cd build
cmake ..
make
```
Executable will be at `build/hello-world`.

### 4. Run the Program
```bash
./hello-world  # or ./build/hello-world if using CMake
```
Expected output: `Hello, World!`

## Running Tests

### Unit Tests
```bash
# With CMake build
cd build
make test

# Or run tests directly
./test/unit/test_hello_world
```

### Test Coverage
```bash
# Generate coverage report (requires gcov/lcov)
make coverage
```

## Development Workflow

### Test-Driven Development (TDD)
1. Write a failing test in `tests/unit/test_hello_world.cpp`
2. Implement the minimum code to pass the test in `src/hello_world.cpp`
3. Refactor while keeping tests passing
4. Repeat

### Code Quality Checks
```bash
# Format code (clang-format required)
make format

# Lint code (cppcheck required)
make lint
```

## Troubleshooting

### Common Issues

**"Compiler not found"**: Install g++ or clang++:
```bash
# Ubuntu/Debian
sudo apt install g++

# macOS
brew install llvm
```

**"Catch2 not found"**: Catch2 is header-only and included in the project.

**"Make command not found"**: Use CMake instead or install make.

### Verification
To verify everything works:
```bash
# Build, test, and run
make clean test run

# Expected:
# 1. Build succeeds
# 2. All tests pass
# 3. Output: "Hello, World!"
```

## Next Steps

- Read the full specification in `spec.md`
- Review the implementation plan in `plan.md`
- Check the constitution for coding standards

## Constitution Compliance Checklist

- [ ] Code follows naming conventions (Principle I)
- [ ] Tests written before implementation (Principle II)  
- [ ] Program output is consistent (Principle III)
- [ ] All tests pass with >80% coverage (Testing Gate)
- [ ] Code review completed (Quality Gate)