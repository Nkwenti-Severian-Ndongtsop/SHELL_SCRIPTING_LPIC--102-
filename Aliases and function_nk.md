# Functions and Aliases
### Aliases
An alias ia a subtitute name for another command(s). It is very easy to create an alias.\
to create an aliase we use the following formst;
> alias <alias_name>=command(s)\

> unalias <aliase_name>

 ### Creating Functions
 Function can simply be a collection of commands and logic statements.\
 We can have two syntax in creating a function;
Under function we have two ways of defining functions
- using the keyword `function`\
using this keyword you simply add the function_name next to it, then the commands in curly brackets `{}`

> function <function_name> {
>
> command1
> 
> command2
> 
> command#
> 
> }

- using `()`
using this symbol`()`, you don't need the function keyword. You can just write the function name then you include`()` after the name.

> <function_name> () {
>
> command1
>
> command2
>
> command#
>
> }
### bash built-in special variables
- `$?`: used to check if the last command was successfully executed.
- `$$`:it provides the **PID** of the current shell.\
- `$!`: it povide the PID of the last running background job.\
- `$#`: it is used to access the number of arguments passed to a function.\
- `$@,$*`: they hold all the arguments passed in function.\
- `$_`: it holds the last parameter.

#### Variables in functions
This is simply writing a shell script and including a variable in it.
```bash
test () {
name="Mr MArco"
echo "The god of code is $name "
}
```

#### positional paramaters in functions
This is just about passing parameters in your function directly.
```bash
function test {
echo "$1, you look good"
}

test Mr Marco
```
we could also have;
```bash
function test {
echo "$1, you look good"
}
```
with this one, you will include the parameter when execution the function.

