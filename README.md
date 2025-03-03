# BasicShell
 A simple Linux shell with limited functionality.
 It finds an executable in the PATH, then loads
 it  and executes it (using execv). Since it uses
 "." (dot) as a separator, it cannot handle file
 names like "minishell.h"

## Documentation

### Compiling
In order to compile the code and run it, follow
the following instructions:  
1. Move into the build directory with `cd build`
3. Build file with `cmake ..`
4. Set ulimit with `ulimit -u 500`
5. Run the program with `make run`

### Commands
Below is a list of valid commands. Text in \<angle
brackets> can be chosen by the user.  
```rust
C <file1> <file2>       // Copy <file1> to <file2>, creates <file2> if needed
D <file>                // Delete <file>
E <comment>             // Echo <comment>
H                       // Help menu, displays documentation
L                       // Lists the contents of the current directory
M <file>                // Make; creates <file> via text editor
P <file>                // Prints contents of <file> to screen
Q                       // Quit shell program
W                       // Wipe; clears the screen
X <program>             // Executes <program>
```
If a command is issued outside of this list, it
will be passed to `execvp()` and executed normally.
