# lexical-analysis
Lexical Analysis for Pascal Compiler
Compiler’s Design Project Definition
Guadalupe De la Cruz Márquez

# 1.	General Description of the Compiler
Pascal is an imperative and procedural programming language (published in 1970 by Niklaus Wirth), as a small, efficient language intended to encourage good programming practices using structured programming and data structuring. It is named in honor of the French mathematician, philosopher and physicist Blaise Pascal. For this project I will implement both procedural and imperative styles with some restrictions that I’ll describe above.

# 2.	Description of the Stages
This project will involve the 4 compiler’s stages during the course that are described with more details above.

# a.	Lexical Analysis
In this section I will explain the formal language as input, as well as the instructions I will implement for my current compiler project. 
1.	Comments. 
i.	Multi-line comments are set like {* *} 
ii.	Single line comments are set like {}
2.	Nested structures. The syntax for a nested for-do loop statement in Pascal is as follows:
for variable1: =initial_value1 to [down to] final_value1 do
begin
   for variable2: =initial_value2 to [down to] final_value2 do
   
   begin   
      statement(s);
   end;
end;   
The syntax for a nested while-do loop statement in Pascal is as follows:
while(condition1) do

begin
   while(condition2) do
   
   begin
      statement(s);
   end;
   statement(s);
end;

The syntax for a nested repeat ... until loop Pascal is as follows:
repeat
   statement(s);
   repeat
      statement(s);
   until(condition2);
until(condition1);









# 3.	Variables and Constants. 
i.	Variables
Type & Description
Character
Typically, a single octet (one byte). This is an integer type.
grade: char = 'A';
Integer
The most natural size of integer for the machine.
age: integer = 15;
Boolean
Specifies true or false logical values. This is also an integer type.
value: boolean = true;


ii.	Constants
Constant Type & Examples
Ordinal (Integer)type constant
valid age = 21;
Set type constant
Vowels = set of (A, E, I, O, U);
Pointer types constant
P = NIL;
Character type constant
Operator = '+';

# 4.	Strings. Allow the use of strings as one token.
String
Stores an array of characters.
name: string = 'John Smith';
String type constant
president = 'Johnny Depp';

# 5.	Input and Output. 
i.	Output
program output;
var x: integer;
begin
  for x: =1 to 10 do
  writeln ('Number', x)
end.

ii.	Input
program input;

var
  c: int;
begin
  readln(c);
  read(c);
end.




program RemainOpen;

begin
  writeln('&&inp*ut');
  readOut;
end.

# 6.	Data types. This are all the data types that pascal supports, but for this implementation I’ll only use: Integer, Character & Boolean from the scheme below.



# 7.	Conditional and Loops. 
i.	while-do loop
program whileLoop;
var
   a: integer;

begin
   a: = 10;
   while a < 20 do
   
   begin
      writeln ('value of a: ', a);
      a: = a + 1;
   end;
end.

ii.	for-do loop
program forLoop;
var
   a: integer;

begin
   for a: = 10 to 20 do
   
   begin
      writeln ('value of a: ', a);
   end;
end.

iii.	repeat-until loop
program repeatUntilLoop;
var
   a: integer;

begin
   a: = 10;
   (* repeat until loop execution *)
   repeat
      writeln ('value of a: ', a);
      a: = a + 1
   until a = 20;
end.



# b.	Syntax Analysis
This is a basic description of Pascal’s syntax, here explains in summary how the different parts of the program are translated from the grammar.
 



The next diagrams are the way BNF [3] describes de same grammar flow and translation but in a more detailed way. The symbols of the Pascal vocabulary are divided into the following classes:  identifiers, numbers, strings, operators, delimiters, and comments. In the following notation, 
•	The bar | means you must have one of the two items it separates.
•	Curly brackets {} are shorthand notation for having zero or more items. 
•	Square brackets [] stands for optional meaning having zero or one item. 
•	Characters to be represented as is are in single quotes. 
. 
 


 
 





# c.	Semantic Analysis
In the sense that each kind of declaration or statement is mapped into a high-level Petri net. When a statement is aggregated from several other statements, the net is built in the usual algebraic way by combining the subnets of the constituent statements. As an example, we represent a while-statement of the form by the following net:
 

A for-statement as the form:
 
The read-command as:
 
The write command as:
 
d.	Code Generation
For this project, I decided to implement a small Pascal compiler (that will create an executable file) based on the steps above because, as a procedural & imperative language, it uses a static scope & a block structure that uses a restricted data typing to work properly.

# 3.	References
[1].	https://en.wikipedia.org/wiki/Pascal_(programming_language)
[2].	https://www.tutorialspoint.com/pascal/pascal_basic_syntax.htm
[3].	http://condor.depaul.edu/ichu/csc447/notes/wk2/pascal.html
[4].	https://www.cs.kau.se/cs/education/courses/dvgc01/lectures/Lab1Intro.pdf
[5].	 http://courses.washington.edu/css448/zander/Project/grammar.pdf
[6].	https://tidsskrift.dk/daimipb/article/view/7470/6319
