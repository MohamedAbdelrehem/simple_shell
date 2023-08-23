## Repository Description

Welcome to our collaborative repository! We are **Mohamed Abdelrehem** and **Mustafa Nasser**, and this repository is where we simulate a basic **Unix Shell** with its respective commands. Our implementation uses the POSIX API to recreate the functionalities of the first Ken Thompson's Shell. This project was developed as a part of the **0x16. C - Simple Shell** project at [ALX Africa](https://www.alxafrica.com/ "ALX Africa").

We've utilized a variety of system calls including **read**, **write**, **open**, **execve**, **exit**, **fflush**, **fork**, **free**, **malloc**, **getline**, **isatty**, **perror**, **strtok**, **wait**, and **waitpid**.

Our simple shell provides a user-friendly interface, displaying the prompt *Hell_Shell>>* and executing user-inputted commands in separate child processes.

## Acknowledgments

We want to express our gratitude to the ALX Community for their support and guidance throughout this project. We also extend our thanks to anyone whose code we've referenced.

## General Guidelines

- Compatible editors: `vi`, `vim`, `emacs`
- All files will be compiled on Ubuntu 14.04 LTS
- Programs and functions will be compiled with `gcc 4.8.4` using flags such as `-Wall`, `-Werror`, `-Wextra`, and `-pedantic`
- Every file should end with a new line
- The presence of a mandatory `README.md` file at the root of the project folder
- Code should adhere to the `Betty` style guidelines, which will be checked using [betty-style.pl](https://github.com/holbertonschool/Betty/blob/master/betty-style.pl) and [betty-doc.pl](https://github.com/holbertonschool/Betty/blob/master/betty-doc.pl)
- Our shell must not have memory leaks
- No more than 5 functions per file
- All header files should include include guards

## Requirements:

* Operating System: [Ubuntu 14.04 LTS](http://releases.ubuntu.com/14.04/)

* Compiler: [GCC 4.8.4](https://gcc.gnu.org/gcc-4.8/)

## Features:

Our shell offers a range of features, making it a versatile tool for users:

* The prompt *Hell_Shell>>* is displayed, awaiting user input for commands. Each command line ends with a new line character (activated by pressing *ENTER*).
* After executing a command, the prompt is displayed again.
* Entering *exit* will terminate *Hell Shell* and return a status code of 0.
* Typing *exit [status]* will end *Hell Shell* and return the inputted status, where *status* ranges from 0 to 255.
* The program can be exited using *Ctrl+D* (end of file).
* The shell effectively handles command lines containing arguments and pathways.
* The program does not quit upon entering ^C (Ctrl+C).
* Typing *env* prompts the program to display the current environment.
* Our shell executes common shell commands like *ls*, *grep*, *find*, *pwd*, *rm*, *cp*, *mv*, *exit*, *env*, *history*, etc., along with their arguments.
* In case an executable is not found, an error message is displayed and the prompt reappears.
* Our shell supports commentaries using the *#* symbol.
* Wildcard characters such as ls \*.dat in parameters (or commands) are NOT supported.
* Pipes (*|*), shell logical operators (*&&* or *||*), and command separators (*;*) are NOT supported.

### Allowed Functions: 
- `access` (man 2 access)
- `chdir` (man 2 chdir)
- `close` (man 2 close)
- `closedir` (man 3 closedir)
- `execve` (man 2 execve)
- `exit` (man 3 exit)
- `_exit` (man 2 _exit)
- `fflush` (man 3 fflush)
- `fork` (man 2 fork)
- `free` (man 3 free)
- `getcwd` (man 3 getcwd)
- `getline` (man 3 getline)
- `getpid` (man 2 getpid)
- `isatty` (man 3 isatty)
- `kill` (man 2 kill)
- `malloc` (man 3 malloc)
- `open` (man 2 open)
- `opendir` (man 3 opendir)
- `perror` (man 3 perror)
- `read` (man 2 read)
- `readdir` (man 3 readdir)
- `signal` (man 2 signal)
- `stat` (__xstat) (man 2 stat)
- `lstat` (__lxstat) (man 2 lstat)
- `fstat` (__fxstat) (man 2 fstat)
- `strtok` (man 3 strtok)
- `wait` (man 2 wait)
- `waitpid` (man 2 waitpid)
- `wait3` (man 2 wait3)
- `wait4` (man 2 wait4)
- `write` (man 2 write)

## Compiling, Debugging, and Running

- All programs and functions will be compiled with `gcc 4.8.4` using flags like `-Wall`, `-Wextra`, `-Werror`, and `-pedantic`

- To **compile** functions, use the following command:

```shell
gcc -Wall -Wextra -Werror -pedantic -Wno-format -g *.c -o Hell_Shell
```

- For **debugging** the shell, utilize valgrind:

```shell
valgrind --leak-check=full ./Hell_Shell
```

- To **run** the shell, execute:

```shell
./Hell_Shell
```

- For an in-depth manual on our shell, type:

```shell
man ./man_1_simple_shell
```

## Examples

Here are a few examples showcasing the usage of our Hell Shell:

- Running *ls* command:

```shell
Hell_Shell>> ls
AUTHORS  Hell_Shell  README.md auxiliar_functions.c  create_child.c  dir  execute.c  free_mem.c  generateAUTHORS  man_1_simple_shell  shell.h shell_init.c  tokening.c
```

- Providing the full path for the *ls* command:

```shell
Hell_Shell>> /bin/ls
AUTHORS  Hell_Shell  README.md	auxiliar_functions.c  create_child.c  dir  execute.c  free_mem.c  generateAUTHORS  man_1_simple_shell  shell.h shell_init.c  tokening.c
```

- Running *ls* with additional flags:

```shell
Hell_Shell>> ls -lat
total 88
drwxrwxr-x 4 vagrant vagrant  4096 Apr 16 17:04 .
-rw-rw-r-- 1 vagrant vagrant  5502 Apr 16 17:04 README.md
...
```

- Checking the current working

 directory with *pwd*:

```shell
Hell_Shell>> pwd
/home/vagrant/HOLBERTON/simple_shell
```

- Using the *echo* command:

```shell
Hell_Shell>> echo Hello World
Hello World
```

- Exiting the shell using *Ctrl+D* and *Ctrl+C*:

```shell
Hell_Shell>> ^C
Hell_Shell>> 
vagrant@vagrant-ubuntu-trusty-64:~/HOLBERTON/simple_shell$ 
```
