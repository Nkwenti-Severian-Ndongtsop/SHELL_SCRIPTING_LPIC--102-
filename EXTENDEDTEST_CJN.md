# Extended Tests
A test command can evaluate expressions using two different sysntaxes usually placed in a square bracket where any command is given implicitly
```sh
if [[ -f "$filename" ]]; then
  echo "File exists."
else
  echo "File does not exist."
fi
```
## SOME SPECIAL ARGUMENTS
* -a "$VAR"
    Evaluate if the path in VAR exists in the filesystem and it is a file.
* -b "$VAR"
    Evaluate if the path in VAR is a special block file.
* -c "$VAR"
  Evaluate if the path in VAR is a special character file.
* -d "$VAR"
  Evaluate if the path in VAR is a directory.
* -e "$VAR"
  Evaluate if the path in VAR exists in the filesystem.
* -f "$VAR"
  Evaluate if the path in VAR exists and it is a regular file.
* -g "$VAR"
  Evaluate if the path in VAR has the SGID permission.
* -h "$VAR"
  Evaluate if the path in VAR is a symbolic link.
  #  SOME NUMERICAL ARGUMENTS
*  $NUM1 -lt $NUM2
Evaluate if NUM1 is less than NUM2.
* $NUM1 -gt $NUM2
Evaluate if NUM1 is greater than NUM2.
 * $NUM1 -le $NUM2
Evaluate if NUM1 is less or equal to NUM2.
* $NUM1 -ge $NUM2
Evaluate if NUM1 is greater or equal to NUM2.
* $NUM1 -eq $NUM2
Evaluate if NUM1 is equal to NUM2.
* $NUM1 -ne $NUM2
Evaluate if NUM1 is not equal to NUM2.
   ## TEXT VARIABLES
    It is recommended to use the double quotes around a tested variable because, if the variable
    happens to be empty, it could cause a syntax error for the test command. The test options
    require an operand argument and an unquoted empty variable would cause an error due to a
    missing required argument. There are also tests for arbitrary text variables, described as follows:
* -z "$TXT"
Evaluate if variable TXT is empty (zero size).
* -n "$TXT" or test "$TXT"
Evaluate if variable TXT is not empty.
* "$TXT1" = "$TXT2" or "$TXT1" == "$TXT2"
Evaluate if TXT1 and TXT2 are equal.
* "$TXT1" != "$TXT2"
Evaluate if TXT1 and TXT2 are not equal.
* "$TXT1" < "$TXT2"
Evaluate if TXT1 comes before TXT2, in alphabetical order.
* "$TXT1" > "$TXT2"
Evaluate if TXT1 comes after TXT2, in alphabetical order.

# THE CASE STATEMENT
```SH
#!/bin/bash

echo "Enter a fruit (apple, banana, orange):"
read fruit

case $fruit in
  apple)
    echo "You chose an apple!"
    ;;
  banana)
    echo "You chose a banana!"
    ;;
  orange)
    echo "You chose an orange!"
    ;;
  *)
    echo "Unknown fruit!"
    ;;
esac

```


In this script:

  *  The user is prompted to enter a fruit.
   * The script checks the input against several defined patterns (apple, banana, and orange).
    * If the input matches one of the patterns, the corresponding message is printed.
   * The wildcard pattern * is used to catch any input that does not match known options, displaying a default message.
