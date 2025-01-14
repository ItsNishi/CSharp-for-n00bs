# Data Types

Value vs Reference



Data types go hand-in-hand with variables, so it's hard to cover them as separate topics.  Some concepts here may not make 100% sense until you complete the **Variables** module, so feel free to revisit this module again if you need to.

Data types in C# are referred to as "value types" and "reference types".

When a value type is declared, the data is stored in the memory location of the variable.  When a reference type is declared, the data is stored somewhere else in memory and the variable contains a pointer to it.

Reference types are always allocated in heap memory, but value types can be allocated on the heap or on the stack, depending on where they're declared.  If a value type is declared inside a method, then it's stored on the stack.  If it's declared in a class, then the data is stored on the heap.  This is because a class is a reference type, which must always be stored on the heap.  Classes and methods will be covered in detail later.

Value types include `int`, `byte`, `bool`, and `char`.  Reference types include `string`, `arrays` and `class`.



Integers and Floating Points

An integer is whole number, -2, -1, 0, 1, 2, etc.

If we want an integer to be negative, it should be declared as a "signed" integer.  Otherwise, it can be "unsigned".  Unsigned integers can be larger than signed integers because we're not wasting a "sign" bit.  We can allocate different sizes for an integer in multiples of 8 bits:  8, 16, 32 and 64 bits.

The naming of these types can be a little hard to remember - they are:

\


| **Keyword** | **Size**        |
| ----------- | --------------- |
| sbyte       | Signed 8-bit    |
| byte        | Unsigned 8-bit  |
| short       | Signed 16-bit   |
| ushort      | Unsigned 16-bit |
| int         | Signed 32-bit   |
| uint        | Unsigned 32-bit |
| long        | Signed 64-bit   |
| ulong       | Unsigned 64-bit |

\
int sInt = -20;

uint uInt = 20;

byte sByte = 256;

\


Most IDEs will know if you're trying to assign an invalid value to these types.  Since `byte` is only 8-bits (and unsigned), it cannot accommodate a value larger than 255.

A floating point is a number that can have decimal places, 8.2, 3.14, etc.

There are three types (all of which are signed):

\


| Keyword | Size     |
| ------- | -------- |
| float   | 4 bytes  |
| double  | 8 bytes  |
| decimal | 16 bytes |

\


When declaring a float or double, the letter `F` or `D` should be appended to the value.  You can declare a value that is more precise than the specified data type, but it will only "use" the range that it is able when carrying out any mathematics, etc.

\
float piFloat = 3.14159265359F;

double piDouble = 3.14159265359D;



pi as float: 3.1415927

pi as double: 3.14159265359



Booleans and Characters



A `bool` is a true or false value.&#x20;

A `char` is a single letter or number, represented by an integer.  Those "integers" are standardised in the [ASCII](https://www.lookuptables.com/text/ascii-table) and [Unicode](https://www.lookuptables.com/text/unicode-characters) tables.  Different languages allow different byte sizes for characters, from 1 to 4 bytes.  C# uses 2 bytes, which allows it to use any character in UTF-16.



A character is defined with single quotes.



bool myBool = true;

char myChar = 'A';
