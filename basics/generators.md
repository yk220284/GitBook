# Generators

### Simple Example

Creating a simple generator that returns crc\(cyclic redundancy check\) calculations of a list of integers

```python
from zlib import crc32
import numpy as np

# creating a generator using yield key word
def create_generator(integers):
    for integer in integers:
        yield crc32(np.int64(integer))
```

Iterate through the generator 

```python
g = create_generator([1,3,4])

# using a loop
for x in g:
    print(x)
    
# or one by one using next()
next(g)
```



### Other Examples

Another form of common generators is using `()` 

```python
g1 = (i**2 for i in range(5))
```



