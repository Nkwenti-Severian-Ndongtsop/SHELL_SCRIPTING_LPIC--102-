  ## LOOP CONSTRUCTS
Scripts are often used as a tool to automate repetitive tasks, performing the same set of commands
until a stop criteria is verified. Bash has three loop instructions — for, until and
while — designed for slightly distinct loop constructions.
  # TYPES OF LOOPS
        There are generally 3 loops
 1:  THE FOR LOOP 
   This for works through a given list of items (eg .words,or any other space-separated text segments just to name a few)
   Before each iteration,the *for* instruction assigns the current item to a variable,which can the be used by the enclosed commands
   It is done until a no item is left 
 ```sh
 for VARNAME in LIST
do
COMMANDS
done
```
FOR EXAMPLE
```sh
#!/bin/bash
for NUM in 1 1 2 3 5 8 13
do
echo -n "$NUM is "
if [ $(( $NUM % 2 )) -ne 0 ]
then
echo "odd."
else
echo "even."
fi
done
```
 2: THE UNTIL LOOP
 An until loop in Bash scripting is used to repeatedly execute a block of code until a specified condition becomes true. It operates in the opposite manner of a while loop: the until loop continues running as long as the condition evaluates to false and stops when the condition evaluates to true[1], [2].

```sh
 #!/bin/bash
SEQ=( 1 1 2 3 5 8 13 )
IDX=0
until [ $IDX -eq ${#SEQ[*]} ]
do
    echo -n "${SEQ[$IDX]} is "
    if [ $(( ${SEQ[$IDX]} % 2 )) -ne 0 ]
    then
        echo "odd."
    else
        echo "even."
    fi    SEQ=( 1 1 2 3 5 8 13 ): Initializes an array SEQ with a sequence of numbers.
    IDX=0: Sets the starting index to 0.
    until [ $IDX -eq ${#SEQ[*]} ]: Loops until IDX reaches the length of SEQ.
    echo -n "${SEQ[$IDX]} is ": Prints the current number without a newline.
    if 
    IDX=$(( $IDX + 1 ))
done
```
3: THE WHILE LOOP
+ The while loop in Bash scripting is a fundamental construct that allows you to execute a block of commands repeatedly as long as a specified condition evaluates to true. It is particularly useful when the number of iterations is not known beforehand and depends on the condition being checked[1], [2].
```SH
while [ condition ]; do
    # commands
done
```
# EXAMPLE OF WHILE LOOP
```SH
#!/bin/bash

count=1

while [ $count -le 5 ]; do
    echo "Count is $count"
    ((count++))
done

```

