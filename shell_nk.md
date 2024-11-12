# SHELL_SCRIPTING_LPIC
  ## customizing and using the shell variables
  #### key points
   - set environment variables
   - write bash functions for frequently used commands 
   - maintain skeleton directories for new users account
   - set command search path with the proper directory

Starting with shells we have **Interractive/Non-interactive shells** and **Login/Non-Login Shells**
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
