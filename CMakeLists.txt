cmake_minimum_required(VERSION 3.10)
project(HelloWorld)

# Set C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# Set output directory
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

# Add main executable
add_executable(hello-world src/hello_world.cpp)

# Enable testing
enable_testing()

# Add unit tests
add_executable(test_hello_world tests/unit/test_hello_world.cpp)
target_include_directories(test_hello_world PRIVATE ${CMAKE_SOURCE_DIR}/tests)
add_test(NAME HelloWorldTest COMMAND test_hello_world)

# Add integration tests
add_executable(test_execution tests/integration/test_execution.cpp)
target_include_directories(test_execution PRIVATE ${CMAKE_SOURCE_DIR}/tests)
add_test(NAME ExecutionTest COMMAND test_execution)

# Add custom test target
add_custom_target(test_run
    COMMAND ${CMAKE_CTEST_COMMAND} --output-on-failure
    DEPENDS test_hello_world test_execution
)
