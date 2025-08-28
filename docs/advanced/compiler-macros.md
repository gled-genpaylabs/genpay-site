# Compiler Macros
**Compiler Macros** are a helpful tool from the compiler, which allow you to get the compiler's help with operating on data.

**List of Genpay macros:**
- **`print!(LITERAL_FORMAT, ...) void`** - Prints formatted input without a new line to standard output.

Example: `print!("2 + 2{}", 2 + 2)`

----
- **`println!(LITERAL_FORMAT, ...) void`** - Prints formatted input with a new line to standard output.

Example: `println!("Hello, {}!", "World")`

----
- **`format!(LITERAL_FORMAT, ...) *char`** - Returns a formatted string from provided input.

Example: `format!("Number: {}", 5)`

----
- **`panic!(LITERAL_FORMAT, ...) void`** - Calls the compiler's runtime panic with formatted input.

Example: `panic!("Oops! Looks {}", "bad")`

----
- **`sizeof!(EXPRESSION / BASIC_TYPE) usize`** - Returns the size (in bytes) of the provided expression or basic type.

Example: `sizeof!(i32)`

----
- **`cast!(EXPRESSION, TYPE) TYPE`** - Casts an expression to the targeted type.

> [!NOTE] Allowed Types Casts
> - `integer type -> integer type`
> - `integer type -> float type`
> - `integer type -> char`
> - `integer type -> bool`
> - `integer type -> pointer type`
> ----
> - `float type -> float type`
> - `float type -> integer type`
> ----
> - `char -> integer type`
> - `bool -> integer type`
> - `pointer type -> integer type`
> - `pointer type -> pointer type`

Example: `cast!(10, f64)`
