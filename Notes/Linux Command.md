## What are Shell Scripts?

A Shell script is a file that contains a series of commands. The shell reads the file like they've been entered directly from the command line then carries out each command sequentially as written in the script. 
Rember that most things that can be done on the command line can be done with scripts and vice versa. 


## Writing Shell Scripts 
### First Step 
You need a text editor to write your scripts, it could be from the terminal (Vim, Emacs, Nano) or a GUI text editor (VS Code, Sublime or Atom) whatever you're comfortable with maybe notepad but remeber that the file must contain ASCII text. 

  The first line of your scripy is important and should begin with `#!/bin/bash`. It is a special construct, called a **shebang**, given to the system indicating what program is to be used to interpret the script. In this case, /bin/bash.

### Writing Comments
To use comments in your scripts, use the `#` character before yout text. 

### Our Sample Script
```
#!/bin/bash
# My first script
echo "Hello World!"
```

### Create a file named hello_world 
You can use whatever editior you are confortabke with, I prefer nano so that's what I'm going with. :)
```console
user@shell:~$ nano hello_world
```

### Adding your commands to the file `hello_world` you just created
Copy the command from our Sample Script above into the terminal 

### Running our Script
To run your script you just createad, enter ```./hello_world``` to the command line.
```console
user@shell:~$ nano hello_world
```

### Setting Permission (Making your file executable)
Since you're working with Scripts and you plan on executing them you need to make them executable and all you have to do is give the shell permission to do so using 
the `chmod` command. 

The command: ``` chmod 755 [FILENAME]``` The `"755"` will give us read, write, and execute permission. Everybody else will get only read and execute permission.
To make the script private, (i.e., only we can read and execute), use `"700"` instead.

### Add directories to our ($PATH)
The $PATH is a list of dierctories where executable files(programs) are kept and will search only those difectories for programs whenever you call one.  
To view your current path, enter: ```echo $PATH``` in your terminal, this returns a colon sperated list of directories. We can add directories to our path with the following command, where directory is the name of the directory we want to add: ```export PATH=$PATH:directory```

A better way would be to edit our ***.bash_profile*** file to include the above command. That way, it would be done automatically every time we log in. To do this we need to create a bin directory if we do not have one already ```mkdir ~/bin```

After noving our script to the ***bin*** directory, we'll be all set. Now we just have to type our script name and our script will run. 

> PS: On some distributions, most notably Ubuntu (and other Debian-based distributions), we will need to open a new terminal session before our newly created bin directory will be recognized.
