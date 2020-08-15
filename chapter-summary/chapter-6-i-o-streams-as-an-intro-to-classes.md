# Chapter 6 I/O Streams as an Intro to Classes

1. a function that is associated with an _object_ is called a _member function_ \(pg 346\).

   ```cpp
   #include <fstream>
   #include <iostream>
   #include <cstdlib>
   int main()
   {
       using namespace std;
       ifstream inStream;
       ofstream outStream; // declear two objects
       inStream.open("infile.dat");
       if (inStream.fail()) // member function for failing in openening
       {
           cout << "Input file opening failed. \n";
           exit(1);
       }

       int first, second, third;
       inStream >> first >> second >> third; // reading lines
       inStream.close();

       // outStream operations

       return 0;
   }
   ```

2. `exit` function from `<cstdlib>` and `std` namespace.

   ```cpp
   exit(1) //returns its argument to the os
   ```

3. _append_ to a file

   ```cpp
   ofstream outStream;
   outStream.open("important.txt", ios::app); // ios::app is a special constant defined in iostream
   ```

4. declare a _string_ variable

   ```cpp
   char fileName[16]; // a string variable named fileName with MAXIMUM 15 chars;
   ```

   the value of a string variable cannot be changed by an assignment.

5. _manipulator function_ from `<iomanip>`

   ```cpp
   cout << "Start" << setw(4) << 10; // set white space including 10;
   cout.setf(ios::fixed);
   cout.setf(ios::showpoint);
   cout << "$" << setprecision(2) << 10.3 << endl << "$" << 20.5 << endl; // set precision
   ```

6. set _flag_ \(pg 361\)

   ```cpp
   // someStream is a stream object like cout, outStream
   someStream.setf(ios::fixed); //floats are not written in e-notation
   someStream.setf(ios::showpoint); //a decimal point is always shown
   someStream.precision(2); //self-explainatory
   ```

7. read file _number by numebr_ separated by _whitespace_

   ```cpp
   while (inStream >> line)
    {
        cout << setw(10) << line << endl; // or other stuff
        count++;
    }
   ```

8. `get`, `put` and `putback` \(pg 376\)
9. WARN **accidentally pick up `\n`**

   `cin.get(symbol)` directly after a `cin`.

   ```cpp
   using namespace std;
   char symbol;
   int number;
   cin >> number;
   cout << number << endl;
   do
   {
   cin.get(symbol);
   } while (symbol != '\n'); // pick up extra \n
   cin.get(symbol);
   cout << symbol << endl;
   ```

10. _default arguments_ exits in c++
11. end of file `fin.eof`
12. `<cctype>` \(pg 393\) contains common character functions.

    rmk: `toupper('a')` returns `int`. so need type casting to get `A`

    ```cpp
    cout << static_cast<char>(toupper('a'));
    // or
    char c = toupper('a');
    cout << c;
    ```



