# SHELL_SCRIPTING_LPIC
  ## customizing and using the shell variables
  #### key points
   - set environment variables
   - write bash functions for frequently used commands 
   - maintain skeleton directories for new users account
   - set command search path with the proper directory

The shell is the most powerful tool in a linux system and provides an interface for managing the linux operating.
It takes input from the user as commands and gives output on the terminal.

Starting with shells we have **Interractive/Non-interactive shells** and **Login/Non-Login Shells**\
**Log-in shells:** is the initial shell that starts when a user logs in to the system, through the terminal or SSH connection.
This log-in uses **~/.profile**, **~/.bashrc**, etc. This is indicated using **(-)**\
**Non log-in shells:** these are shells that are started without a log-in process, like starting a shell from another shell or a program.\ 
It executes the **~/.bashrc**. This does not have **(-)**. 
The command to check wether you are on a log-in shell or a non log-in shell is
```bash
echo $0
```
**Interactive shells:** these are shells that respond accordingly to commands inputted by the user.\
**Non-interactive shell:** these shells does not allow the user to input commands and returns  no output to the user.
e.g the screen command
```bash
screen
```
##### exmples of log-in shells
- log-in into another user
- log-in remotely using SSH
##### examples of non log-in shells
- vs-code shell
- normal shell
##### examples of interactive shells
- Bash
- Zsh
##### examples of non-interactive shells
- running a command on remote server using SSH
`echo 'echo $-; shopt login_shell'| ssh localhost`

The next thing are start-up scripts;\
**/etc/profile :** this script runs to set-up all environment variables such as PS1.
When log-in into a user the `.profile` and `/etc/profile` runs.\
**~/.bash_profile:** it is used to configure the users environment.\
it also runs both `~/.bash_login`, `~/.profile`.
**~/.bash_login:** it is used when you want to log-in.\
**~/.profile:** this is a check file. the script in it checks if a shell is running, if so, it's run the `~/.bashrc`.\
**~/.bash_logout:** this runs when you want to log-out. It ensures the clean-up of all operations. 

##### The next thing is how to execute a file\
They are two alternatives;
> source \<filename\>

> . \<filename\>

The last thing under this chapter is `SKEL`\
This directory `/etc/skel` contains template directory which are created when a new user is added.
You can display the content of this directory using 
```bash
cd /etc/skel
```
## This ends this chapter
