# SHELL_SCRIPTING_LPIC
  ## customizing and using the shell variables
  #### key points
   - set environment variables
   - write bash functions for frequently used commands 
   - maintain skeleton directories for new users account
   - set command search path with the proper directory
The shell is the most powerful tool in a linux system and provides an interface for managing the linux operating.\
It takes input from the user as commands and gives output on the terminal.\

Starting with shells we have **Interractive/Non-interactive shells** and **Login/Non-Login Shells**
**Log-in shells:** is the initial shell that starts when a user logs in to the system, through the terminal or SSH connection.\ 
This log-in uses **~/.profile**, **~/.bashrc**, etc. This is indicated using **(-)**
**Non log-in shells:** these are shells that are started without a log-in process, like starting a shell from another shell or a program.\ 
It executes the **~/.bashrc**. This does not have **(-)**. 
The command to check wether you are on a log-in shell or a non log-in shell is
```bash
echo $0
```
**Interactive shells:** these are shells that respond accordingly to commands inputted by the user. Executes the .bashrc, .profile script
Non-interactive shell: this shell does not allow the user to input command and returns  no output to the user. The screen command 

the next thing are start-up scripts; 
/etc/profile : this script runs to set-up all environment variables such as PS1.
When log-in into a user the .profile and /etc/profile runs 
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
Next thing to talk about is **start-up scripts** for the shell.
> /etc/profile       *

> /etc/profile.d/*   *

> ~/.bash_profile

> ~/.bash_login

> /etc/bash.bashrc   *

> ~/.profile

> ~/.bash_logout

> ~/.bashrc
