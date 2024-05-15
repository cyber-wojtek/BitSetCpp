# Bitset class for C++

This project aims to be an efficient, optimized C++ BitSet header class designed to provide high-performance operations for manipulating fixed and dynamic size sequences of bits.

## Table of Contents
- [Key Features](#key-features)
- [How To Use](#how-to-use)
- [Documentation/Examples](#documentation-examples)
- [Download](#download)
- [License](#license)


## Key Features
- **Efficient and Optimized Operations:** Performance is prioritized, providing heavily optimized read and write operations. It's designed to handle bit manipulation tasks as efficiently as possible.
- **Comprehensive Functionality:** Supports a wide range of operations, including iteration, bitwise operations (AND, OR, XOR, NOT), comparison, conversion to and from strings, and more.
- **Iterators:** Iterator types (`iterator`, `const_iterator`, `reverse_iterator`, `const_reverse_iterator`) are provided for easy traversal and manipulation of bits within the bitset.
- **Flexible Constructors:** Offers multiple constructors for initializing bitsets from other bitset instances and C and C++ style strings.
- **Fixed and Dynamic Size Support:** Both a fixed and dynamic size version of the bitset class is available.
- **Main Classes:**
  - `bitset<BlockType, Size>`: Represents a fixed-size BitSet with a specified block type and size.
  - `dynamic_bitset<BlockType>`: Represents a dynamic-size BitSet with a specified block type.
  
## How To Use
To use the this library in your project, follow these steps:
1. **Download:** Download the newest available release package from the [releases page](https://github.com/cyber-wojtek/BitSetCpp/releases).
2. **Integration:** Add the downloaded header file (`bitset.hpp` or similar) to your project.
3. **Include:** Include the header file in your source files where you need to use the bitset functionality.
4. **Usage:** Start using the `bitset` or `dynamic_bitset` class in your code by creating instances, performing operations, and utilizing its features as needed.

Here's a basic example of how to use this library:

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

## Documentation/Examples <a name="documentation-examples"></a>
Full documentation of the library and more examples can be found [here](#)

## Download
You can download this library from the [GitHub releases page](https://github.com/cyber-wojtek/BitSetCpp/releases).

## License
This library is distributed under the MIT License with an attribution clause. See the `LICENSE` file for more information about the licensing terms.
