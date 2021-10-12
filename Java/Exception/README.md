# Exception

## Checked and Unchecked Exceptions

### Checked Exceptions
Must be either caught or declared in the method in which it is thrown. Otherwise, it won't compile.

Two ways of solving the compilation error:
1. Catch the exception and handle it;
2. Declare that the exception can be thrown using the `throws` keyword.

An exception is a checked exception if it inherits from `java.lang.Throwable`, but **not** from `java.lang.RuntimeException` or `java.lang.Error`.

Example: `FileNotFoundException`

### Unchecked Exceptions
Can be thrown without being caught or declared.

Examples: `ArithmeticException`, `ArrayIndexOutOfBoundsException`, `NullPointerException`.

References:
1. https://en.wikibooks.org/wiki/Java_Programming/Checked_Exceptions
2. https://en.wikibooks.org/wiki/Java_Programming/Unchecked_Exceptions