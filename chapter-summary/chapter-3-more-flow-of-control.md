# Chapter 3 More Flow of Control

1. `>` and `==` evaluated before `&&` \(pg 146\)

   `&&` before `||` \(pg 147\)

2. `enum` type, a list of constants of type `int`

   ```cpp
   enum Direction { NORTH = 0, SOUTH = 1, EAST = 2, WEST = 3};
   enum Direction { NORTH, SOUTH, EAST, WEST}; // equivalent as auto assign from 0
   ```

3. `enum class` avoiding `enum` to act like `int`

   ```cpp
   enum class Direction
   {
       NORTH,
       SOUTH,
       EAST,
       WEST
   } d1; // another way to declare a Direction variable
   d1 = Direction::WEST;
   cout << "Direction 1 is west: " << (d1 == Direction::EAST) << endl; //can't cout d1 directly as it's Direction type
   ```

4. `else if` \(pg 156\) is just normal `else` and `if` indented differently, cuz c++ is _indentation insensitive_ :\)
5.  `switch` only works for `bool`, `enum` with `int` type, or a `char` \(pg164\) without `break;`, execute all blocks below the current case block
6.  `num++` vs `++num` \(pg 174\)

```cpp
   ++num //the incrementeing is done before the expression is returned

   int count = 0;
   while (count++ < 10)
   {
       statment; //here count = 1,...,10
   } //now count is 10

   count = 0;
   while (++count < 10)
   {
       statment; //here count = 1,...,9
   }
```

note the difference compared to `n++` which is down after the statement in for-loop

