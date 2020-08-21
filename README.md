## Table of contents
* [Description and Links](#S-CODE-TO-BF)
* [Commands and Syntax](#Commands)
* [Examples](#Examples)

# S-CODE-TO-BF
make writing Brainfuck code a lot simpler! (Uses 8bit cells and cell wrapping where [-]- would set the cell to 255)  

I am currently working on a Project in Scratch ( https://scratch.mit.edu/ ) that translates/compiles S-CODE (simple(-ish) programming language I created inside of Scratch, based around making BF CODE) into a valid and (relatively) short Brainfuck Code.
## Links
#### Here is the Project:
```
https://scratch.mit.edu/projects/418348452/
```
#### Here is an Intepreter I made that runs BF-CODE:
```
https://scratch.mit.edu/projects/364982727/
```


## Commands
#### Here is the updating command list:
```
https://scratch.mit.edu/discuss/post/4340209/
```
#### Lets go over the basics
* [Variables](#Variables)
* [Lists](#Lists)
* [I/O](#Input/Output)
* [Loops](#Loops)
* [Do if](#Do-if)
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
lint Test (amount of elements)
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
  

   
   
### Input/Output

  
  
   
### Loops

  
  
   
### Do if

  
  
   
### Low Level Commands

  
  
   
### Other

  
  
   

## Examples
test bla bla bla

