# minishell
The goal of this project is to create a simple shell. Will be your own little bash or zsh. You are going to learn a lot about processes and file descriptors.
<p align="center">
  <img src="https://res.cloudinary.com/leetask/image/upload/v1639473388/perso/minishell_keoad5.png" width="100%" />
</p>


### Available options

Minishell runs executables from an absolute, relative or environment PATH (``/bin/ls`` or ``ls``), including arguments or options. ``'``, ``\`` and ``"`` work the same as bash, except for multiline commands.

You can separate commands with ``;``, as well as use redirections ``>`` ``>>`` ``<`` and pipes ``|``.

Environment variables are handled, like ``$HOME``, including the return code ``$?``.

Finally, you can use ``Ctrl-C`` to interrupt and ``Ctrl-\`` to quit a program, as well as ``Ctrl-D`` to throw an EOF, same as in bash.

A few of the functions are "built-in", meaning we don't call the executable, we re-coded them directly. It's the case for ``echo``, ``pwd``, ``cd``, ``env``, ``export``, ``unset`` and ``exit``.
### Allowed Functions
- **malloc**
- **free**
- **write**
- **open**
- **read**
- **close**
- **fork** = [Creates a child process.](https://man7.org/linux/man-pages/man2/fork.2.html)
- **wait, waitpid**  = [Stops the parent process until the child process exit.](https://man7.org/linux/man-pages/man2/waitid.2.html)
- **wait3, wait4** = [Are similar to waitpid, but additionally return resource usage information about the child.](https://man7.org/linux/man-pages/man2/wait3.2.html)
- **signal** = [Sets a function to handle a signal.](https://man7.org/linux/man-pages/man2/signal.2.html)
- **kill** = [Sends a signal to a process or a group of processes.](https://man7.org/linux/man-pages/man2/kill.2.html)
- **exit** = [Terminates a process immediately, special handle for child processes.](https://www.tutorialspoint.com/c_standard_library/c_function_exit.htm)
- **getcwd** = [Saves the pathname of your current working directory in a string.](https://man7.org/linux/man-pages/man2/getcwd.2.html)
- **chdir** = [Changes your current working directory.](https://man7.org/linux/man-pages/man2/chdir.2.html)
- **stat, lstat, fstat** = [Returns information about a file.](https://man7.org/linux/man-pages/man2/stat.2.html)
- **execve** = [Executes a program referred by a variable.](https://man7.org/linux/man-pages/man2/execve.2.html)
- **dup** = [Creates a copy of a file descriptor using the lowest numbereded unused descriptor.](https://man7.org/linux/man-pages/man2/dup.2.html)
- **dup2** = [Creates a copy of a file descriptor using the descriptor number given by the user.](https://man7.org/linux/man-pages/man2/dup.2.html)
- **pipe** = [It's used to create inter-process communication.](https://man7.org/linux/man-pages/man2/pipe.2.html)
- **opendir** = [Opens a directory stream.](https://pubs.opengroup.org/onlinepubs/009695399/functions/opendir.html)
- **readdir** = [Returns a pointer to a dirent structure representing the next directory entry in the directory stream.](https://www.man7.org/linux/man-pages/man3/readdir.3.html)
- **closedir** = [Closes the directory stream.](https://linux.die.net/man/3/closedir)
- **strerror** = [Returns an error message.](https://www.tutorialspoint.com/c_standard_library/c_function_strerror.htm)
- **errno** = [Number of last error, its a variable.](https://www.youtube.com/watch?v=IZiUT-ipnj0&ab_channel=JacobSorber)

## How To Use
> Deployment
```shell
git clone https://github.com/mbani01/minishell.git
make && ./minishell
```

[Back To The Top](#minishell)

### Credit

This two-person project was done with [mamoussa](https://github.com/mamoussa405).

I was responsible for the lexing, parsing, argument checking, and environment variables.

Mamoussa took care of the execution, built-in functions, signal handling ,redirection and piping .

