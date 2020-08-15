# Chapter 5 Functions for All Subtasks

1. _Call-by-Reference-Parameters_: they pass in the variable at _memory location_

   ```cpp
   void swapValues(int& variable1, int& variable2)
   {
       int temp;
       temp = variable1;
       variable1 = variable2;
       variable2 = temp;
   } //note using void as no return
   ```

2. _Formal parameters_ vs _arguments_
3. writing comments:

   _Precondition_: what is assumed to be true when the function is called

   _Postcondtion_: the effect of the function call

4. `assert` macros from `<cassert>` is used when requiring a boolean expression to be `true`.

   e.g. when we want certain user input.

   ```cpp
   #define NDEBUG // for disabling all assert macros
   #include <cassert>
   ```

