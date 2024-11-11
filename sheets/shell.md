## SHELL

**Basic Navigation & File Management:**

| Command | Description | Example |
|---|---|---|
| `pwd` | Print working directory | `pwd` |
| `cd <directory>` | Change directory | `cd /home/user/documents` |
| `ls` | List directory contents | `ls -l` (long listing) |
| `mkdir <directory>` | Create a new directory | `mkdir new_folder` |
| `touch <file>` | Create an empty file | `touch my_file.txt` |
| `cp <source> <destination>` | Copy files or directories | `cp file.txt new_file.txt` |
| `mv <source> <destination>` | Move or rename files or directories | `mv file.txt /tmp/` |
| `rm <file>` | Remove files | `rm -r my_directory` (remove directory recursively) |

**File Content & Manipulation:**

| Command | Description | Example |
|---|---|---|
| `cat <file>` | Display file contents | `cat my_file.txt` |
| `less <file>` | View file contents with paging | `less long_file.txt` |
| `head <file>` | Display the first few lines of a file | `head -n 5 my_file.txt` |
| `tail <file>` | Display the last few lines of a file | `tail -f my_file.txt` (follow file changes) |
| `grep <pattern> <file>` | Search for a pattern in a file | `grep "error" log.txt` |
| `wc <file>` | Count words, lines, and characters | `wc -l my_file.txt` (count lines) |
| `sort <file>` | Sort lines of a file | `sort -r my_file.txt` (reverse sort) |
| `uniq <file>` | Remove duplicate lines from a sorted file | `uniq my_file.txt` |

**System Information & Control:**

| Command | Description | Example |
|---|---|---|
| `whoami` | Display the current user | `whoami` |
| `date` | Display the current date and time | `date` |
| `cal` | Display a calendar | `cal` |
| `df` | Display disk space usage | `df -h` (human-readable format) |
| `du` | Display directory size | `du -sh my_directory` |
| `free` | Display memory usage | `free -h` |
| `top` | Display system processes | `top` |
| `uname` | Display system information | `uname -a` |

**Network Operations:**

| Command | Description | Example |
|---|---|---|
| `ping <host>` | Test network connectivity to a host | `ping google.com` |
| `ssh <user>@<host>` | Securely connect to a remote host | `ssh user@server.com` |
| `wget <url>` | Download a file from the internet | `wget https://example.com/file.zip` |
| `curl <url>` | Transfer data from or to a server | `curl -O https://example.com/file.zip` |
| `ifconfig` | Display network interface configuration | `ifconfig` |
| `netstat` | Display network connections and listening ports | `netstat -tulnp` |

**Advanced Techniques:**

| Command | Description | Example |
|---|---|---|
| `|` (pipe) | Redirect output of one command to another | `ls -l | grep "txt"` |
| `>` (redirect) | Redirect output to a file | `ls -l > file_list.txt` |
| `>>` (append) | Append output to a file | `date >> log.txt` |
| `<` (input) | Redirect input from a file | `sort < file_list.txt` |
| `$()` (command substitution) | Execute a command and substitute its output | `echo "Today is $(date)"` |
| `&&` (and) | Execute a command only if the previous command succeeded | `mkdir new_dir && cd new_dir` |
| `||` (or) | Execute a command only if the previous command failed | `rm file.txt || echo "File not found"` |
| `*` (wildcard) | Match any characters | `ls *.txt` |
| `?` (wildcard) | Match a single character | `ls file?.txt` |
| `[ ]` (character class) | Match any character within the brackets | `ls [abc].txt` |

**Shell Scripting:**

  * Create a file with `.sh` extension.
  * Add a shebang line: `#!/bin/bash`
  * Write shell commands in the file.
  * Make the script executable: `chmod +x my_script.sh`
  * Run the script: `./my_script.sh`

**Tips & Tricks:**

  * Use Tab completion to quickly complete commands and file names.
  * Use the Up arrow key to recall previous commands.
  * Use `Ctrl+C` to interrupt a running command.
  * Use `Ctrl+R` to search through command history.
  * Use `man <command>` to view the manual page for a command.

**Resources:**

  * **Bash Guide for Beginners:** [https://tldp.org/LDP/Bash-Beginners-Guide/html/](https://www.google.com/url?sa=E&source=gmail&q=https://tldp.org/LDP/Bash-Beginners-Guide/html/)
  * **Advanced Bash-Scripting Guide:** [http://tldp.org/LDP/abs/html/](https://www.google.com/url?sa=E&source=gmail&q=http://tldp.org/LDP/abs/html/)
  * **Explain Shell:** [https://explainshell.com/](https://www.google.com/url?sa=E&source=gmail&q=https://explainshell.com/)