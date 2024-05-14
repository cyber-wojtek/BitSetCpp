# CppBitSet
Efficient, optimized C++ BitSet class, that heavily prioritizes the performance.

# How to use

## woj::bitset
```cpp
#include <woj/bitset.hpp>
#include <iostream>

int main()
{
  srand(time(nullptr));
  woj::bitset<uint32_t, 20> bitset;

  for (std::size_t i = 0; i < bitset.size(); ++i)
    bitset.set(i, rand() % 2);

  std::cout << "bitset:           " << bitset << '\n';

  woj::bitset<uint16_t, 20> bitset2(true);

  for (std::size_t i = rand() % 2; i < bitset.size(); i += 1 + rand() % 2)
    bitset2.clear(i);

  std::cout << "bitset2:          " << bitset2 << '\n';

  woj::bitset<uint64_t, 20> bitset_res = bitset & bitset2;

  std::cout << "bitset & bitset2: " << bitset_res;

  return 0;
}
```

Possible result:
```
bitset:           01111110010101001011
bitset2:          00100001000010101010
bitset & bitset2: 00100000000000001010
```

## woj::dynamic_bitset

```cpp
#include <woj/bitset.hpp>
#include <iostream>

int main()
{
  srand(time(nullptr));
  std::size_t size;

  std::cout << "Enter the size of the bitset: ";
  std::cin >> size;

  woj::dynamic_bitset<uint32_t> dynamic_bitset(size);

  for (std::size_t i = 0; i < size; ++i)
    dynamic_bitset.set(i, rand() % 2);

  std::cout << "dynamic_bitset:                   " << dynamic_bitset << '\n';

  woj::dynamic_bitset<uint32_t> dynamic_bitset2(size);

  for (std::size_t i = 0; i < size; ++i)
    dynamic_bitset2.set(i, rand() % 2);

  std::cout << "dynamic_bitset2:                  " << dynamic_bitset2 << '\n';

  woj::dynamic_bitset<uint64_t> dynamic_bitset_res = dynamic_bitset | dynamic_bitset2;

  std::cout << "dynamic_bitset | dynamic_bitset2: " << dynamic_bitset_res;

	return 0;
}
```
Possible input:
```
Enter the size of the bitset: 20
```

Possible result:
```
dynamic_bitset:                   10101001100111100001
dynamic_bitset2:                  11110000100000011110
dynamic_bitset | dynamic_bitset2: 11111001100111111111
```
