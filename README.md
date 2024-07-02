# MyCalculator
background:
You will create a program called "mycal" that can solve math/logic problems. You will start with basic operators and then keep on adding features that are harder and harder to implement. Don't worry with doing unit testing. We will do a code review after you have solved all the problems.

Problems:
0. create a program called "mycal". When you call it from the terminal it will print out “hello I am a calculator”.

1. modify "mycal" so that when called from the terminal it will let you enter a string. After you press enter it will print the string back to you and ask for another string. Make it repeat this forever until the program is stopped with Ctrl+C

2. modify “mycal" so if you pass the string that starts with “add” and then followed by two numbers such as “add 6 10” it will print out the answer (“16”) on the next line. If you pass in something that doesn’t start with “add” make it print the string “sorry I don’t understand the input”

3. modify “mycal” so if a string starts with “sub” it will subtract the next two numbers. for example “sub 6 10” will print out “-4”. Also do “mul” for multipling two numbers, “div” for dividing two numbers.

4. modify “mycal” so it can also do the operators “and”, “or” and “xor”. for example “and 6 10” will do a bitwise “and” and print out the result 2. “or 6 10” will do a bitwise “or” and print out 14. “xor 6 10” will do a bitwise “exclusive or” and print out 12.

# stop here and I will review the code before continuing.

5. modify “mycal” so it can store numbers. If you type “assign x 6” it will store 5 into “x”. then if you type something like “add x 10” it will print out 16. Only needs to support single letter variable names for now. So if you then type “assign abC 10” you could then run “add x abC” afterwards and it will print out 16.

6. modify “mycal” so you can set variables from the return result by using the format “x result”. For example if you type:
add 6 10
# prints: 16
assign x result
# now x is equal to 16
add x + 10
# prints: 26

if it’s not clear the “# prints: blah” statements are what “mycal” will print to the screen. no the user input.


6. modify “mycal” so it can do loops. Will need to add two more commands which are “loop” and “repeat”. “loop” doesn’t do anything by itself but when the “repeat” command is reached it will redo all the previous calculations between the “loop” and “repeat”. For example if you run the commands:
assign x 6
assign y 10
loop
mul x y
# prints: 60
assign z result
sub z y
# prints: 50
x 10
repeat
# prints: mul x y
# prints: 100
# prints: assign z result
# prints: sub z y
# prints: 90
