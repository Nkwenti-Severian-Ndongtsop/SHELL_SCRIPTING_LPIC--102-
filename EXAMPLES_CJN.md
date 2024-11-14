# FOR AN "AND STATEMENT"
```SH
#! /bin/bash

age=50

if [[ "$age" -gt 18 && "$age" -lt 30 ]]
then
 echo "valid age"
 else
 echo "age not valid"
fi
```
# FOR AN " OR STATEMENT"
```SH
#! /bin/bash

age=98

if [ "$age" -gt 18 ] || [ "$age" -lt 30 ]
then
 echo "valid age"
 else
 echo "age not valid"
fi
```
 # A TASK LIST
```SH
 #!/bin/bash

# Function to add a task
add_task() {
    echo "$1" >> tasks.txt
    echo "Task added successfully."
}

# Function to remove a task
remove_task() {
    sed -i "/$1/d" tasks.txt
    echo "Task removed successfully."
}

# Function to view tasks
view_tasks() {
    cat tasks.txt
}

# Main program
while true; do
    echo "1. Add task"
    echo "2. Remove task"
    echo "3. View tasks"
    echo "4. Exit"
    read -p "Enter your choice:  " choice

    case $choice in
        1)
            read -p "Enter task:  " task
            add_task "$task"
            ;;
        2)
            read -p "Enter task to remove:  " task
            remove_task "$task"
            ;;
        3)
            view_tasks
            ;;
        4)
            exit 0
            ;;
        *)
            echo "Invalid choice."
            ;;
    esac
done
```
