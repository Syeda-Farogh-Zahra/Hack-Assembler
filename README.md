# Hack-Assembler
Assembler for hack language, using very basic programming concepts like static arrays and dynamic arrays. The project is created in C++.
To understnd this code one must have knowlegde about how nand2tetris hack language works.
This asembler is in two parts, the does not handels symbols while the second part do.
In the first part an input file is being taken from user, and firstly all comments and whitespaces are being removed.Then an static array of size 16 is being declared and is initialized by 0. the file is being read line by line, on encountering the "@" symbol the value next to it is converted to binary by using a for loop and standard logic for decimal conversion. The A instruction is then written in the output file. If not an A instruction then it must be a C instruction. C instruction is divided into two parts. And the values are hardcored in the array, following the table of hack language instructions.

In the second part a class is made having two data members, *symbols* to store names of lables and variables and *address* to store there adresses. in the funtion predefined, a temp file is created and on encountering a predefined symbol it replaces it with it's value. in the function lables file is being read again and on encountering a label it stores it value in the address aarray and it's name in the symbol array. in the function label check, if a label is used it replaces it's name with the value stored in address array. Then in Variable function works almost same as label, it just checks if the string after @ is a number or not, if it is a number store it, else ignore it. The conversion is done in the same way as in part 1.

Program is being tested on multiple asm programs including "PONG" and it works fine.
The goal was to create it in the simplest way possible so anyone even with basic programming concepts can understand it.
