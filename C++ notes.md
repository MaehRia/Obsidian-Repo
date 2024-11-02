
# size_t VS int

Size_t is always unsigned type. An **unsigned type** in C++ is a data type that can only represent non-negative values (zero and positive numbers).


### 1. Definition and purpose

- **`size_t`**:
    - **Type**: An **unsigned integer type** defined in `<cstddef>` or included indirectly through common headers like `<vector>`, `<iostream>`, etc.
    - **Purpose**: Used to represent the size or count of objects in memory and is returned by functions like `.size()`. It ensures that the value is non-negative and large enough to handle the size of any object in memory.
    - **Range**: Always non-negative (no negative values), and its maximum value depends on the system architecture (e.g., 32-bit or 64-bit).
- **`int`**:
    - **Type**: A **signed integer type** that can represent both negative and positive numbers.
    - **Purpose**: Used for general counting and arithmetic operations where negative values might be meaningful or required.
    - **Range**: The range varies, typically from `-2,147,483,648` to `2,147,483,647` on 32-bit systems.

### 2. Comparison of Ranges

- **`size_t`**:
    - Has a range from `0` to a maximum positive value (e.g., `4,294,967,295` on a 32-bit system or `18,446,744,073,709,551,615` on a 64-bit system).
    - It's safe to use `size_t` for indexing and sizes because it can represent large, positive numbers without the risk of negative values.
- **`int`**:
    - Can hold both negative and positive values. Its range is limited compared to `size_t` because half of its range is used for negative numbers.

### 3. Use cases

**`size_t`**:

- Best used when working with **sizes and indices**, such as iterating over elements of a container or when a function expects a size-related value (e.g., `.size()` of a vector). Example: 
 ```cpp
std::vector<int> numbers = {1, 2, 3, 4, 5};
for (size_t i = 0; i < numbers.size(); ++i) {
    std::cout << numbers[i] << " ";
}
```

**`int`**:

- More appropriate for **general-purpose calculations** where negative numbers might be involved or when the potential size of numbers won't exceed the limits of `int`.

### 4.  Potential Pitfalls

**Mixing `size_t` and `int`**:

- Be careful when comparing or mixing `size_t` and `int`. Since `size_t` is unsigned, operations that mix `int` and `size_t` can produce unexpected results if not handled properly, especially in comparisons.