## What are Shell Scripts?

A Shell script is a file that contains a series of commands. The shell reads the file like they've been entered directly from the command line then carries out each command sequentially as written in the script. 
Rember that most things that can be done on the command line can be done with scripts and vice versa. 


## Writing Shell Scripts 
### First Step 
You need a text editor to write your scripts, it could be from the terminal (Vim, Emacs, Nano) or a GUI text editor (VS Code, Sublime or Atom) whatever you're comfortable with maybe notepad but remeber that the file must contain ASCII text. 

  The first line of your scripy is important and should begin with `#!/bin/bash`. It is a special construct, called a **shebang**, given to the system indicating what program is to be used to interpret the script. In this case, /bin/bash.

### Writing Comments
To use comments in your scripts, use the `#` character before yout text. 

### Setting Permission (Making your file executable)
Since you're working with Scripts and you plan on executing them you need to make them executable and all you have to do is give the shell permission to do so using 
the `chmod` command. 

The command: ``` chmod 755 [FILENAME]``` The `"755"` will give us read, write, and execute permission. Everybody else will get only read and execute permission.
To make the script private, (i.e., only we can read and execute), use `"700"` instead.
