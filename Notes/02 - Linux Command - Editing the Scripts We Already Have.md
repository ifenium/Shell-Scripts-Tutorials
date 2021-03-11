## Editing the Scripts We Already Have

During our shell session, the system is holding a number of facts about the world in its memory. This information is called the environment. The environment contains such things as our path, our user name, and much more. We can examine a complete list of what is in the environment with the `set` command.

Two types of commands are often contained in the environment. They are aliases and shell functions.

### How is the Environment Established?

When you log on to out system, the bash program starts and reads a series of configuration scripts called `startup files` which define the default environment used by all users which is followed by startup files in our home directory that define our personal environment
