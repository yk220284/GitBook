# Chapter 4 Procedural Abstraction

1. `<iostream>`, `<cmath>`,`<cstdlib>` etc. are header files.
2. \(pg 219\)

   | Library Header | Functions |
   | :--- | :--- |
   | cmath | `sqrt`, `pow`\(args need to be `double`\), `ceil`, `floor`, `fabs`\(float abs\) |
   | cstdlib | `abs`, `labs`\(long abs\), `rand`, `srand` |
   | ctime | `time(0)` \(gives the Unix time\) |

3. _Type Casting_ for division between variables

   ```cpp
   static_cast<double>(SOME_INT)
   ```

4. Function _declaration_/prototype\(p226\)

   | Name | Position | Remarks |
   | :--- | :--- | :--- |
   | Function Declaration | Before `main` | `;` required, _formal params_ are optional |
   | Function Defn | After `main` | formal params in function heading |

5. _Overloading_: when you give two or more function defn for the same function name.

   Two functions must have different **number** of formal params or some formal params of different **type** e.g. division `/`

