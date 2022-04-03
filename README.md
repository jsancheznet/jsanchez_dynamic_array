# jsanchez_dynamic_array
Generic dynamic array implementation in C

:information_source: this only compiles/works in C.

# How to use

```C
#include "jsanchez_dynamic_array.h"


// Create a pointer with the desired array type
my_struct *StructArray;

// Init the array, this allocates size for the array metadata and sets the array size and capacity to 0
ArrayInit(StructArray);

// Push to the end of the array, the array grows dynamically and each
// time the capacity is reached it allocates the double of the space used
// and copies everything onto the new memory pool
my_struct Foo;
ArrayPush(StructArray, Foo);

// Pops the last element of the array. The array also resized down
// when the size is 1/3 of the capacity and you pop one element.
my_struct *Foo;
ArrayPop(StructArray, &Foo);

// Get the current array size and capacity, ArrayCount is the same as
// ArraySize, i prefer ArrayCount but Size might be clearer
int Size = ArraySize(StructArray);
int Capacity = ArrayCapacity(StructArray);

// Free the memory and metadata
ArrayFree(StructArray);
```

# License

This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or
distribute this software, either in source code form or as a compiled
binary, for any purpose, commercial or non-commercial, and by any
means.

In jurisdictions that recognize copyright laws, the author or authors
of this software dedicate any and all copyright interest in the
software to the public domain. We make this dedication for the benefit
of the public at large and to the detriment of our heirs and
successors. We intend this dedication to be an overt act of
relinquishment in perpetuity of all present and future rights to this
software under copyright law.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.

For more information, please refer to <http://unlicense.org/>
