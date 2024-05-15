# CppBitSet

CppBitSet is an efficient, optimized C++ BitSet header class designed to provide high-performance operations for manipulating fixed-size sequences of bits.

## Table of Contents
- [Key Features](#key-features)
- [How To Use](#how-to-use)
- [Concepts](#concepts)
- [Download](#download)
- [License](#license)


## Key Features
- **Efficient and Optimized Operations:** CppBitSet prioritizes performance, providing heavily optimized read and write operations. It's designed to handle bit manipulation tasks with minimal overhead.
- **Comprehensive Functionality:** Supports a wide range of operations, including iteration, bitwise operations (AND, OR, XOR, NOT), comparison, conversion to and from strings, and more.
- **Iterators:** Iterator types (`iterator`, `const_iterator`, `reverse_iterator`, `const_reverse_iterator`) are provided for easy traversal and manipulation of bits within the bitset.
- **Flexible Constructors:** Offers multiple constructors for initializing bitsets from bool values, block values, other bitset instances, C-style strings, pointers to strings, and `std::basic_string` instances.
- **Dynamic-Size Version:** A dynamic-size version of the bitset class is also available, offering flexibility in handling variable-sized bit sequences.
- **Main Classes:**
  - `bitset<BlockType, Size>`: Represents a fixed-size BitSet with a specified block type and size.
  - `dynamic_bitset<BlockType>`: Represents a dynamic-size BitSet with a specified block type.
  
## How To Use
To use the CppBitSet library in your project, follow these steps:
1. **Download:** Download the newest available release package from the [releases page](https://github.com/cyber-wojtek/BitSetCpp/releases).
2. **Integration:** Add the downloaded header file (`BitSet.hpp` or similar) to your project.
3. **Include:** Include the header file in your source files where you need to use the bitset functionality.
4. **Usage:** Start using the `bitset` class in your code by creating instances, performing operations, and utilizing its features as needed.


Here's a basic example of how to use CppBitSet:

```cpp
#include "woj/bitset.hpp"
#include <iostream>

int main() {
    // Create a bitset with a fixed size of 10 bits, initialized with all zeros
    woj::bitset<uint16_t, 10> myBitSet;

    // Set bits using dedicated set() function
    myBitSet.set(1);  // Set the bit at index 1 to true

    // Bit indexing is supported as well
    myBitSet[3] = true;  // Set the bit at index 3 to true
    myBitSet[5] = true;  // Set the bit at index 5 to true

    // Print the bitset
    std::cout << "Bitset: " << myBitSet << '\n';

    // Perform bitwise operations, comparisons, etc.
    // ...

    return 0;
}

```

## Concepts
The library utilizes C++20 concepts for type checking and template constraints. Here are the key concepts used:
- `unsigned_integer`: Checks if a type is an unsigned integer.
- `char_type`: Checks if a type is a character type.

## Download
You can download the CppBitSet library from the [GitHub releases page](https://github.com/cyber-wojtek/BitSetCpp/releases). Choose the appropriate release package for your project and download it to get started.

## License
CppBitSet is distributed under the MIT License with an attribution clause. See the `LICENSE` file included with the library for more information about the licensing terms.
