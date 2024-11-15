# SCRIPT STRUCTURE AND EXTENSIONS

    A Script file is an ordered sequence of commands that must be executed by a corresponding command interpreter.

    There are many interpreters for the Script but the default one is after the '#!' at the first line
    known as shebang like /bin/bash

    All lines with "#" are considered as ignored after the shebang and considered as comments.

    To manipulate files, we must make sure the users groups or others have proper permissions
    We use the command 'chmod ugo -=+ rwx'

    With permissions put in current directory, it can be executed as './scriptname.sh'

    It is important to make the script writable by root user only because groups and others can destroy the script 
    by modifying it.

    The placement of the file are not too rigid. Two commands can be on the same line but executed differently. 
    This is done by simply adding a ';' at end of each command.

    We can check status by using the '$?' command.


# VARIABLES

    Storage locations that holds value eg Solution=422

    Variables can't start with a non-alphabetical variable.

    Bash script also have special variables called parameters.

    Parameters start with non-alphabetical characters like ;

   * $* All arguments passed to the script

   * $@ All arguments passed to the script if used with double quotes 

   * $# Numbers of arguments in the script 

  *  $0 Name of script file

  *  $!  PID of last executed script

   * $$ PID of current shell

  *  $? Status code of last executed command

    There is also what we call ;

  ### Positional parameters  : 
    Positional parameters are variables that refer to specific positions in a list of arguments.

    They take numbers except 0. If number is greater than 9, we use curly brackets {}

    For example ${23}

    Here communication and interaction with the user is very crutial. 

    To display output to the user, we use 'echo'. For example 'echo hello'

    To take input from the user we can use 'read'. For example 'read name' where name is the variable.

    We can take multiple inputs from the user by separatong the variables with space
    For example read name age sex

    To store commands in a variable we use `` or $()

    To know the length of a variable we use #{} eg echo ${#OS}


# ARRAYS

    An array is a variable storing many inputs.
    It is declared as 'declare -a' eg declare -a size
    
    To insert values we can do size=(1 2 3 4 5). This directly puts all the values in each index

    We can still do size[0]=1, size[1]=2. This puts values one by one

    To read an array, just write the name of variable size

    To read a value in an array we write ${size[1]} for example


# ARITHMETIC EXPRESSION

    To perform arithmetic operations we use 

```sh 
    sum=`expr $val1 + $val2` or sum=$(($val1 + $val2))
 ```

    where sum is the name of the variable that take the whole calculation, val1 and val2 are numbers and + is the operator


# CONDITIONAL EXPRESSION

    In bash, not all commands are but only those that respect a particular criteria.
    for example command A && command B here execution continues only if the one at left is correct. (status code is 0)
    If not it will display an error and stop 

    For command A || command B here execution will stop when it found a correct command (status code is not 0)

    There is also the if condition. Compares condition until one is false 

    for example 
   ```sh
    if [ condition ]; then 

        command

    fi

    We can also put else and elif to compare many conditions 

     for example 
    if [ condition ]; then 

        command

        elif [ condtion ]; then 

            command

        else command

    fi
```

# SCRIPT OUTPUT

    Even when the purpose of a script only involves file-oriented operations, it is important to display
    progress related messages in the standard output, so the user should be informed of progress work.
    To display the output, te echo command is used

    With option -e, command echo is able to display special
    characters using escaped sequences
```sh
     
     #!/bin/bash
    OS=$(uname -o)
    echo -e "Operating system:\t$OS"
    Operating system:	GNU/Linux

```
