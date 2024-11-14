# Variables assigning and refrencing in shell scripting
Variables in simple terms as a name holding a value.
We have two types of variable in shell scripting;\
As an introduction, variables must lie between the following range `[a-z,A-Z,0-9]` including the under-score character `_`\
we also need to note that a variable **should never** start `[0-9]`. 
A variable should never contain special chararter, but can start with an under-score.\
The value can be anything of your choice.

this the syntax for assigning variables
> \<variable_name\>=\<variable_value\>

There should be no space before and after the equal-to sign.\
e.g `name=nkwenti` `_food=garri` `coder1=Marco` etc 

To display a variable, we need to use `$` operator and the `echo` command;
```bash
echo $<variable-name>
```
That command shoul display the variable_value.\
There are two types of variables;
- global variables: these are variables that exist only within the shell they are created.
- local variables: these are variables that exist in all new shells.

We need to note that a local variable can become a global variable using the command `expport`
```bash
export <variable_name>
```
this will make that variable accessible in all shells
to undo this you use the `unset` command
```bash
unset <variable_name>
```
The commands `env` and `printenv` can be used to display all global variables
```bash
env
```
```bash
printenv
```
## This marks the end of this second chapter
