## Editing the Scripts We Already Have

During our shell session, the system is holding a number of facts about the world in its memory. This information is called the environment. The environment contains such things as our path, our user name, and much more. We can examine a complete list of what is in the environment with the `set` command.

Two types of commands are often contained in the environment. They are aliases and shell functions.

### How is the Environment Established?

When you log on to out system, the bash program starts and reads a series of configuration scripts called `startup files` which define the default environment used by all users which is followed by startup files in our home directory that define our personal environment, the exact sequence depends on the type of shell session being started. There are two kinds: 
* A login shell session 
* A non-login shell session.

#### Login Shell Session
A login shell sesssion is one where you are required to provide a user name and password. 

#### Non-login Shell Session 
A non-login shell session typically occurs when we launch a terminal session in the GUI.

Login shells read one or more of the following files at startup

* ***`/etc/profile`*** - A global configuration script that applies to all users.
* ***`~/.bash_profile`*** - A user's personal startup file. Can be used to extend or override settings in the global configuration script.
* ***`~/.bash_login`*** - If `~/.bash_profile` is not found, bash attempts to read this script.
* ***`~/.profile`*** - If neither ~/.bash_profile nor ~/.bash_login is found, bash attempts to read this file. This is the default in Debian-based distributions, such as Ubuntu.


Non-Login shells read one or more of the following files at startup

* ***`/etc/bash.bashrc`*** - A global configuration script that applies to all users.
* ***`~/.bashrc	***`*** - A user's personal startup file. Can be used to extend or override settings in the global configuration script.
They also inherit the environment from their parent process, usually a login shell
Remember,since most of the file names listed above start with a period (meaning that they are hidden), you will need to use the `-a` option when using ls.
The ~/.bashrc file is probably the most important startup file from the ordinary user’s point of view, since it is almost always read.


