# Shell Scripting

### Shebang

- `#!interpreter [optional-arg]` it is calles shebang. The interpreter is the path to an executable program, optional-arg is a string
- `#!/bin/sh` shell executable from bin directory
- `#!/bin/bash` bash shell executable from bin directory
- `#!/usr/bin/env python3` bash shell executable from bin directory
- `echo '#!/bin/bash' >> <file.sh>` appends the `#!/bin/bash` in the file
- In terminal , `./<file.sh>` runs the executable file after running the `chmod +x <file.sh>` command

### Filters, Pipes and Variables

- Filters can be chained together in a pipe. Pipe stands for pipeline
- `|` is the pipe command. e.g. `ls | sort -r` inserts the output of `ls` as input of `sort -r` and show the directory contents in reverse alphabetical order
- shell variables are limited to the scope of shell
- `set` command can be sued to list all shell variables
- `set | head -4` list top 4 shell variables
- to set a variable value, `var_name=value` with no spaces around `=`
- to delete a shell variable, use `unser var_name`
- to print the variable use `echo $var_1 $var_2`, where `$` calls the variable
- environment variable have extented scope. To make a shell variable an environment variable, use `export var_name`
- To check if the `var_name` is made environement variable, use `env | grep "<part_of_string_variable>"` in terminal

### Features of Bash Shell

#### Metacharacters

- `#` precedes a comment
- `;` separate two commands on same line e.g. `echo "Hi" ; whoami`
- `*` filename expansion wildcard. Looks for all the files with the given suffix
- `?` single character wildcard in filename expansion

#### Quoting

- `\` expace unique character interpretation e.g. output of `echo "\$1 each"` will be `$1 each`, whereas `$` is read as a character instead of a builtin feature
- The differenece between single-quotes and double-quotes is that the single-quotes interpret the command literally e.g. the output of `echo '$1 each'` is `$1 each`, whearas, the double quotes evaluates metacharacters e.g. the output of `echo "$1 each"` is `each`

#### I/O redirection

- `>` redirects output to the file
- `>>` append output to the file
- `2>` redirects standard error to the file
- `2>>` append standard error to the file
- `<` redirects file contents to standard input

#### Command substitution

- Replace the command by its output by using `$(command)` e.g. `here=$(pwd)` and doing `echo $here` to display it

#### Bach versus concurrent modes

- in batch mode, the commands run sequentially using `command1 ; command2`
- in concurrent mode, the commands run in parallel using `command1 & command2`. The `command1` operates in the background and passes control to `command2` in the foreground.

