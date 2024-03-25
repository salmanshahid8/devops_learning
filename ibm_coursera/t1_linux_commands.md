# Shell Commands

### Getting System Information

- `printenv SHELL` check the base shell
- `whoami` which returns the user's username
- `id` which returns the current user, and group IDs
- `id -u` returns the id number
- `id -u -n` returns the name of the user
- `uname` returns the operating system name
- `uname -s` -r os name and version
- `uname -v` os version
- `ps` displays running processes and their IDs
- `ps -e` all processes on the pc irrespective of the user. the elapsed time is also showed
- `top` displays running processes and resource usage including memory, CPU, and IO
- `top -n 3` top 3 running process, ordered by CPU usage
- `df` shows information about mounted file systems
- `df -h` size, capacity and available volume of each file system
- `df -h ~` table all the discs mounted on home directory
- `man` fetches the reference manual for any shell command
- `man id` returns the manual of id command. Square brackets show optional input argument
- `date` prints today's date
- `date "+%j day of %Y"`
- `date "+It's %A, the %j day of %Y!"`

### File Management

- `cp` copy file
- `cp -r <source> <destination>` recursively copy all the source files to destination file
- `mv` –> change file name or path
- `rm` –> remove file
- `touch` –> create empty file, update file timestamp
- `chmod` –> change or modify file permissions
- `chmod +x <file.sh>` gives executable permission to the shell file
- `wc <file>` get count of lines, words, characters in file, count last line as a character
- `wc -l <file>` show only number of lines in the file
- `wc -w <file>` show only number of words in the file
- `wc -c <file>` show only number of characters in the file
- `sort <file>` sort the words of file in alphabetical order
- `sort -r <file>` sort the words of file in reverse alphabetical order
- `uniq <file>` show the unique words in the file
- `grep` grep stands for global regular expression print, return lines in file matching pattern
- `grep <criterion> <file>` FInds the lines having the criterion satisfied, is case-sensitive
- `grep -i <criterion> <file>` FInds the lines having the criterion satisfied, not case sensitive
- `cut -d ' ' -f2 <file>` -d is delimiter, -f2 is the word comes after delimiter, shows the later part
- `paste -d ',' <file1> <file2> <filen>` -d is delimiter, default is space, here we said comma, the files will be joined together and displayed on the terminal

### Navigating and working with directories

- `ls` lists the files and directories in the current directory
- `ls <directory>` shows list of files in mentioned directory
- `ls -l` shows permissions, owner, last modified dates and the file names
- `ls -r` shows the tree structure of subdirectories and files
- `find` used to find files matching a pattern in the current directory tree
- `find . -name "file.txt"` . means search within current working directory, is case sensitive
- `find . -iname "file.txt"` . means search within current working directory, not case sensitive
- `pwd` prints the current, or ‘present working,’ directory
- `mkdir` makes a new directory
- `cd` changes the current directory to another directory
- `rmdir` removes an entire directory. should be preferred on rm -r command

### Printing file and string content

- `cat` which prints the entire contents of a file
- `more` used to print file contents one page at a time,space to move to next page ,q+enter to return to command prompt
- `head -n <N>` for printing just the first ‘N’ lines of a file
- `tail -n <N>` for printing the last ‘N’ lines of a file
- `echo`which 'echoes' an input string by printing it. It can also ‘echo’ the value of a variable
- `echo $PATH` path variable

### File compression and archiving applications

- `tar` which is used to archive a set of files
- `tar -cf <file.tar> <file>` makes a tar compressed file
- `tar -tf <file.tar>` list all the files in the archive
- `tar -xf <file.tar> <destination>` unarchive the file.tar in the destination directory
- `zip` which compresses a set of files
- `unzip` which extracts files from a compressed or zipped archive

### Networking applications

- `hostname` prints the host name
- `hostname -s` drops .local from hostname command
- `hostname -i` provides ip address of the host name
- `ping -c 5 <url>` -c=number of packets, sends 5 packets to a URL and prints the response, ctrl+c to abort
- `ifconfig` displays or configures network interfaces on the system
- `ifconfig eth0` returns info of ethernet network
- `curl` displays the contents of a file located at a URL
- `curl <URL> -o <output_file.txt>` store the output of curl command in the file
- `wget <URL>` wget for webget, can be used to download a file from a URL
