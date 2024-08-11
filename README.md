# CPP Template

### Overview

The make file command compiles main.cpp with strict error-checking and debugging options enabled. If the compilation is successful, it immediately runs the resulting executable (a.out). The various flags ensure that your code adheres to best practices, catches potential issues, and makes it easier to debug.

The command is made using the instructions mentioned in the Introduction chapter of [learncpp](www.learncpp.com).

### Usage

After writing the code, use the `make` command in the terminal to compile and run your code.

### Breakdown

`g++`: The GNU C++ compiler. It's used to compile C++ source code into an executable.

`main.cpp`: The source file you're compiling. This file contains the C++ code you want to compile.

`-ggdb`: This flag generates debugging information that is compatible with the GNU Debugger (GDB). It makes it easier to debug the program by including details like variable names and line numbers.

`-pedantic-errors`: Enforces strict adherence to the C++ standard. Any code that is not strictly compliant with the standard will generate an error rather than a warning. This helps in writing portable and standards-compliant code.

`-Werror`: Treats all warnings as errors. This means that if the compiler encounters any warning during compilation, it will stop and treat it as a compilation error, forcing you to fix it.

`-Wall`: Enables most of the common warnings about potentially problematic code, such as uninitialized variables or unreachable code.

`-Weffc++`: Enables warnings suggested by Scott Meyers in his book Effective C++. It checks for common best practices and programming idioms in C++.

`-Wextra`: Enables additional warning flags that are not covered by -Wall. This can help catch even more potential issues.

`-Wconversion`: Warns about implicit type conversions that might alter a value. For example, converting a double to an int could lead to loss of precision, and this flag will warn you about such conversions.

`-Wsign-conversion`: Warns when a value is implicitly converted between signed and unsigned types. This can help catch issues where the sign of a number might inadvertently change due to a type conversion.

`&& ./a.out`: The && operator ensures that the compiled program (a.out) only runs if the compilation was successful (i.e., no errors occurred). ./a.out is the command to run the compiled program.
