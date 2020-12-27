# DOPE: Dartmouth Oversimplified Programming Enviroment
This is my attempt to ressurect DOPE: BASIC's direct predecessor. There are some caveats to this which are explained in the included index.html file. That file also has a working example of the interpreter using xTerm.js.

# Using the Interpreter
dope.js is the core of this operation, it contains the full interpreter for the DOPE language. Creating a new interpreter takes few options, and looks something like:

```
        var dope = new DOPE({
            onOutput: function(line){
              console.log(line);
            }
        });
```
Curently `onOutput` is the only option, which provides a function to handle printing outputs of a DOPE program.

Important functions include...

`DOPE.run(buffer)` -- Run a DOPE program, where `buffer` is a string blob of the program to interpret.

`DOPE.runLine(number, line)` -- Run a single line of DOPE, where `number` is line's number and `line` is the code to run. 
