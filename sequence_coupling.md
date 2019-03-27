# Sequence Coupling

This anti-pattern can be recognized by most of the time analyzing function names and their purpose.
This is particularly important for functions that need to occur in order such as a 'start' function and 'end' function. 

## Example

(found from OneRemote/Main/Main.ino (https://github.com/ChicoState/OneRemote/blob/master/Main/Main.ino))

In the case of the code we found, our setup encapsulates a number of actions that could be further encapsulated seperately for clarity.
More specifically the WIFI setup which contains 3 functions and also the Web Server which also contains 3 functions.

## Harms

It is harmful because it inhibits code useability and readability.
There is a high risk of the code not properly running without proper ordering.
Also, in future additions to code, the setup or current method could become too cluttered and complicated.

## Antidote

Find lines of code with simularities and encapsulate them into their own descriptive, seperate functions.
Find some means of making the order of the required commands clearer, either through commenting or more specific function naming.



(found from Wiki3 (http://wiki3.cosc.canterbury.ac.nz/index.php/Sequential_coupling))
