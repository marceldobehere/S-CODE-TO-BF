## Table of contents
* [Description and Links](#S-CODE-TO-BF)
* [Features](#Features)
* [Commands and Syntax](#Commands)
* [Examples](#Examples)

# S-CODE-TO-BF
make writing Brainfuck code a lot simpler! (Uses 8bit cells and cell wrapping where [-]- would set the cell to 255)  

I am currently working on a Project in Scratch ( https://scratch.mit.edu/ ) that translates/compiles S-CODE (simple(-ish) programming language I created inside of Scratch, based around making BF CODE) into a valid and (relatively) short Brainfuck Code. 
  
## Features
Here are some Features it has:  

* Variables
* Lists
* I/O functions
* Loops 
* Do 
* Functions
* Low Level Commands
* Math
* Programs can be im/ex ported and written in another text editor (save it as a .txt and don't use " because scratch lists don't like that character)

## Links
#### Here is the Project:
```
https://scratch.mit.edu/projects/418348452/
```
#### Here is an Intepreter I made that runs BF-CODE:
```
https://scratch.mit.edu/projects/364982727/
```
#### Here is an OS (a GUI) I made with S-CODE:
```
https://github.com/marceldobehere/BF-OS
```


## Commands
#### Here is the updating command list:
```
https://scratch.mit.edu/discuss/post/4340209/
```



#### Lets go over the basics
* [Variables](#Variables)
* [Lists](#Lists)
* [I/O](#Input-and-Output)
* [Loops](#Loops)
* [Do if](#Do-if)
* [Functions](#Functions)
* [Low Level stuff](#Low-Level-Commands)
* [Other](#Other)




### Variables

Let's start with some basic Variables.  
  
To set up a Variable for later use, just use int.  

```
int Test
```
To set a Variable to a value, use set.  
```
set Test 100
```
To set a Variable to another Variable, use copy.  
```
copy Test Test2
```
To do Math with two Variables, use math.  
Note: The output will get set to the first Variable.  
```
( Supported Operations are Addition(+) Subtraction(-) Multiplication(*) Floor Division(/) )  
math Test * Test2
```
  
  
   
### Lists
Next up are Lists.  
  
To set up a List for later use, just use lint.  

```
intl Test (amount of elements)
```
To set an Element to a value, use lset.  
```
lset Test 1 5
```
This sets the first Element of the List to 5.  
  
To set an Element to a Variable, use vlset.  
```
vlset Test 1 var
```
This sets the first Element of the List to (var).  
  
   
Now we want to set the X'th Element of a List to a Variable.  
Just use vvlset.  
```
vvlset Test var1 var2
```
This sets the (var1) Element of the List to (var2).  
  
   
Now we want to set a Variable to some Element of a List!  
Just use lsetvar.  
```
lsetvar Test 1 var
```
This sets var to the first Element of the List .  
  
  
And now again with the X'th Element.  
Can you guess it?  
Its lsetvvar.  
```
lsetvvar Test var1 var2
```
This sets var2 to the (var2) Element of the List.  
  

   
   
### Input and Output
We have a few ways of Input and Output with S-CODE.  
#### Input
For input, we have input.
```
input var
```
This will prompt input and set var to the ASCII value of the input

#### Output
For Output we have a few Options:  
output.
```
ouput A
```
This will output A.  
  
  
output#.
```
ouput# 10
```
This will output 10 (a new line)  
  
  
For new lines we can also just use nl.
```
nl
```
  
  
Do you want to display Long Text?  
No Problemo! Just use phrase.
```
phrase Hello, World!
```
Can you guess what it will do?  
  
  
Now let's output a Variable!  
```
outvar var
```
This will output the Variable var. (Just like ouput# but with a Variable)  
  
  
Many People faced the HORROR of displaying the Value of a variable in Decimal.  
But with S-CODE it's as simple as outvardec.
```
outvardec var
```
This will output the decimal value of the Variable var.   
   
   
   
### Loops
Now let's get to the Loops!  
  
   
Loops look like this:  
```
loop var1 (= > < ≠) var2
...
if var1 (= > < ≠) var2 loop
```
the *loop* command starts a loop when a condition is given. (Like var1 > var2)  
Every Loop has to have 1 *if ...* command at the end of it where it will loop if a condition is met (Like var1 ≠ var2)  
Note: Loops, if and Do commands only work with variables (for now) so set a variable beforehand!  

  
  
   
### Do if
The Do if command works like the loop command but only once (no looping)
```
do if var1 (= > < ≠) var 2
...
stopdo
```
you can guess what how it works by now...  

  
  
   
### Functions
Functions are like Do if but without the if.  
Add them with this code:
```
function name
...
endfunc
```
Call a function with func.  
```
func test
```
Note: Functions use global variables like everything else and functions CANNOT have other Functions inside!!! (it could cause an endless loop of compiling)  

  
  
  
  
### Low Level Commands
Low Level Commands are for manipulating Cells or/and the Pointer directly.  
We have raw.  
This allows you to paste your own BF Code inside of the S-CODE.  
```
raw >>>+>-[>+<-]
```
Note: When using the raw command, you should always use goto beforehand AND the pointer HAS TO BE EXACTLY WHERE IT WAS BEFORE THE RAW CODE!!!!  
  
  
Then we have cellcopy.  
This allows you to copy one Cell to another.  
```
cellcopy 20 35
```
This copies the Cell 20 to the Cell 35.  
    
  
Then celllchange.  
It changes a cell by some amount
```
( You can only use + or - )
celllchange 10 + 2
```
This changed the Cell 10 by 2.   



And last but not least vcellchange.  
```
vcellchange 10 + var
```
This changed the Cell 10 by (var).  
  
  
And of Course goto.  
```
goto 10
```
It sets the Pointer to 10.  
  
  
   
### Other
Here are some Commands that don't fit in the other Categories:

#.  
```
# Your Comment goes here
 ``` 
It's for commenting.  
   

## Examples

Here are some Example Programs I made for you!  




### Hello, World!
 ``` 
phrase Hello, World!
 ``` 
 
 ### Number Comparator
 ``` 
int a
int b
phrase input number one: 
input a
outvar a
nl
phrase input number two: 
input b
outvar b

loop a = b
nl
outvar a
phrase =
outvar b
if a = b loop

loop a > b
nl
outvar a
phrase >
outvar b
if a > b loop

loop a < b
nl
outvar a
phrase <
outvar b
if a < b loop
 ```  
 ### get decimal ASCII of input
 ``` 
int a
phrase Enter a character
loop a = a
input a
nl
outvar a
phrase : 
outvardec a
if a = a loop
 ``` 
 
