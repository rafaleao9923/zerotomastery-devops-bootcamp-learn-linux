# <p style="text-align: center;">zerotomastery-devops-bootcamp-learn-linux</p>

# Table of Contents

- [zerotomastery-devops-bootcamp-learn-linux](#zerotomastery-devops-bootcamp-learn-linux)
- [Table of Contents](#table-of-contents)
  - [Course Outline](#course-outline)
  - [Setting Up the Environment](#setting-up-the-environment)
    - [1. Linux Distributions](#1-linux-distributions)
  - [The Linux Terminal in Depth](#the-linux-terminal-in-depth)
    - [1.Getting Help, Man Pages (man, type, help, apropos)](#1getting-help-man-pages-man-type-help-apropos)
    - [2.Linux Command Structure](#2linux-command-structure)
    - [3. Terminal - Keyboard Shortcuts](#3-terminal---keyboard-shortcuts)
      - [Navigation Shortcuts:](#navigation-shortcuts)
      - [Text Manipulation Shortcuts:](#text-manipulation-shortcuts)
      - [Command History Shortcuts:](#command-history-shortcuts)
      - [Terminal Multiplexer (tmux) Shortcuts (if tmux is installed):](#terminal-multiplexer-tmux-shortcuts-if-tmux-is-installed)
      - [Copy-Paste Shortcuts (when using a terminal emulator that supports them):](#copy-paste-shortcuts-when-using-a-terminal-emulator-that-supports-them)
    - [4.Mastering the Terminal - the Bash History](#4mastering-the-terminal---the-bash-history)
      - [Basics:](#basics)
      - [Commands for Interacting with the History:](#commands-for-interacting-with-the-history)
      - [Customizing the History:](#customizing-the-history)
      - [Tips and Tricks:](#tips-and-tricks)
    - [5.Mastering the Terminal - The TAB Key](#5mastering-the-terminal---the-tab-key)
      - [1. **Auto-Completion:**](#1-auto-completion)
      - [2. **Auto-Completion for Commands:**](#2-auto-completion-for-commands)
      - [3. **Auto-Completion for File and Directory Paths:**](#3-auto-completion-for-file-and-directory-paths)
      - [4. **Auto-Completion for Filenames with Spaces:**](#4-auto-completion-for-filenames-with-spaces)
      - [5. **Listing Available Options:**](#5-listing-available-options)
      - [6. **Auto-Completion for Command Options:**](#6-auto-completion-for-command-options)
      - [7. **Auto-Completion for Variable Names:**](#7-auto-completion-for-variable-names)
      - [8. **Auto-Completion for Environment Variables:**](#8-auto-completion-for-environment-variables)
      - [9. **Command Substitution:**](#9-command-substitution)
      - [10. **File and Directory Listing:**](#10-file-and-directory-listing)
      - [Tips:](#tips)

## <p style="text-align: center;">Course Outline</p>

## <p style="text-align: center;">Setting Up the Environment</p>

### 1. Linux Distributions

Linux distributions, often referred to as "distros," are variations of the Linux operating system that include the Linux kernel, system libraries, system utilities, and application software. Each distribution is a complete package that can be installed on a computer, server, or embedded device. There are hundreds of Linux distributions, each catering to specific needs and preferences. Here's an overview of some popular Linux distributions, along with their characteristics:

1. **Ubuntu:**
   - **Description:** Ubuntu is one of the most popular and user-friendly Linux distributions. It is based on Debian and follows a regular release cycle. There are different flavors of Ubuntu, including Ubuntu Desktop, Ubuntu Server, and specialized variants like Ubuntu Studio and Ubuntu MATE.
   - **Target Users:** General desktop users, developers, and server administrators.

2. **Debian:**
   - **Description:** Debian is known for its stability and commitment to free and open-source software. It serves as the foundation for many other distributions, including Ubuntu.
   - **Target Users:** General-purpose users, server administrators, and those who prioritize stability.

3. **Fedora:**
   - **Description:** Sponsored by Red Hat, Fedora is known for being cutting-edge, with a focus on the latest software and technologies. It serves as a testing ground for features that may eventually make their way into Red Hat Enterprise Linux.
   - **Target Users:** Developers, enthusiasts, and those who want access to the latest software.

4. **CentOS:**
   - **Description:** CentOS is a free, open-source version of Red Hat Enterprise Linux (RHEL). It aims to provide a stable and secure server environment, making it a popular choice for enterprise servers.
   - **Target Users:** Server administrators and businesses seeking a free, stable alternative to RHEL.

5. **Arch Linux:**
   - **Description:** Arch Linux is a rolling release distribution known for its simplicity, customization, and the Arch User Repository (AUR), which allows users to easily install and manage software.
   - **Target Users:** Enthusiasts, experienced users, and those who want a minimalistic, do-it-yourself approach.

6. **Manjaro:**
   - **Description:** Based on Arch Linux, Manjaro is designed to be user-friendly and accessible. It provides the power of Arch Linux with an easier installation process and pre-configured desktop environments.
   - **Target Users:** Users who appreciate Arch Linux's principles but prefer an easier installation process.

7. **openSUSE:**
   - **Description:** openSUSE is known for its YaST configuration tool, which simplifies system administration tasks. It offers both a rolling release (Tumbleweed) and a stable release (Leap) version.
   - **Target Users:** General users, developers, and system administrators.

8. **Gentoo:**
   - **Description:** Gentoo is a source-based distribution where users compile software from source code, allowing for highly optimized and customized installations. It is known for its flexibility and performance.
   - **Target Users:** Enthusiasts, experienced users, and those who prioritize performance and customization.

9. **Slackware:**
   - **Description:** One of the oldest Linux distributions, Slackware follows a simplicity and minimalism approach. It is known for its stability and lack of automated configuration tools.
   - **Target Users:** Experienced users, purists, and those who prefer manual configuration.

10. **Kali Linux:**
    - **Description:** Kali Linux is designed for penetration testing, ethical hacking, and network security assessments. It includes a wide range of security tools and is used by security professionals.
    - **Target Users:** Security professionals, ethical hackers, and penetration testers.

## <p style="text-align: center;">The Linux Terminal in Depth</p>

### 1.Getting Help, Man Pages (man, type, help, apropos)

**man, type, help, and apropos** are all commands used in Unix-like operating systems to help users understand and use other commands. Here's a comparison:

- man: This command is short for "manual". It provides detailed manual pages for other commands. For example, man ls will provide a detailed manual for the ls command. It's a comprehensive source of information, but can be overwhelming for beginners.

- type: This command is used to describe how its argument would be interpreted if used as a command. It can tell you whether a command is built-in, an alias, a file, a function, etc. For example, type ls might output "ls is aliased to ls --color=auto", indicating that ls is an alias.

- help: This command is used to get a short description of a built-in command. It's less comprehensive than man, but can be easier to understand for beginners. For example, help cd will provide a short description of the cd command.

- apropos: This command is used to search the man page descriptions for instances of a keyword. It's useful when you know what you want to do, but you don't know the command. For example, apropos copy will list all commands that have the word "copy" in their description.

### 2.Linux Command Structure

In Linux, commands are the instructions given to the operating system to perform specific tasks. The typical structure of a Linux command is as follows:

```
command [options] [arguments]
```

Let's break down each component:

1. **Command:**
   - This is the actual executable or script that performs a specific operation. For example, `ls`, `cp`, `mkdir`, etc.

2. **Options:**
   - Options modify the behavior of the command. They are preceded by a hyphen (`-`) or a double hyphen (`--`). Options are often single characters or short words. For example:
     - Single character: `-l` (list in long format)
     - Full word: `--help` (display help information)

3. **Arguments:**
   - Arguments are the targets or inputs for the command. They can be file names, directories, or other data that the command needs to operate on. For example:
     - File name: `file.txt`
     - Directory: `~/Documents`

Here's a simple example using the `ls` command:

```bash
ls -l /home/user/Documents
```

- `ls` is the command.
- `-l` is an option that tells `ls` to list in long format.
- `/home/user/Documents` is an argument specifying the directory for which to list the contents.

Some commands may not require options or arguments, and some may accept multiple options or arguments.

Additionally, there are a few special characters and symbols used in Linux commands:

- **Wildcards:**
  - `*` (asterisk): Represents any number of characters.
  - `?` (question mark): Represents a single character.
  - `[ ]` (square brackets): Represents a range of characters.

  Example using wildcards with the `ls` command:

  ```bash
  ls *.txt
  ```

  This command lists all files with a `.txt` extension in the current directory.

- **Redirection:**
  - `>` (greater than): Redirects standard output to a file, overwriting its contents.
  - `>>` (double greater than): Redirects standard output to a file, appending to its contents.
  - `<` (less than): Takes input from a file and provides it as standard input to a command.

  Example using redirection with the `echo` command:

  ```bash
  echo "Hello, World!" > output.txt
  ```

  This command writes the text "Hello, World!" to a file named `output.txt`.

- **Pipes:**
  - `|` (pipe): Sends the output of one command as the input to another command.

  Example using pipes with the `ls` and `grep` commands:

  ```bash
  ls -l | grep "file"
  ```

  This command lists files in long format and filters the output to display only lines containing the word "file."

Understanding the structure of Linux commands and becoming familiar with commonly used commands and their options is essential for effective command-line usage. The `man` command (manual pages) provides detailed information about individual commands and their usage. For example:

```bash
man ls
```

This command displays the manual page for the `ls` command, providing detailed information on its options and usage.

### 3. Terminal - Keyboard Shortcuts

#### Navigation Shortcuts:

- **Ctrl + A:** Move to the beginning of the line.
- **Ctrl + E:** Move to the end of the line.
- **Ctrl + U:** Delete from the cursor to the beginning of the line.
- **Ctrl + K:** Delete from the cursor to the end of the line.
- **Ctrl + W:** Delete the word before the cursor.
- **Ctrl + L:** Clear the terminal screen.
- **Ctrl + R:** Search command history (reverse search).
- **Ctrl + S:** Stop output to the screen (used to pause terminal output).
- **Ctrl + C:** Terminate the current command.
- **Ctrl + D:** Log out of the current session (or end input for some commands).
- **Ctrl + Z:** Suspend the current process (move it to the background).

#### Text Manipulation Shortcuts:

- **Ctrl + Y:** Paste the most recently cut text.
- **Alt + D:** Delete the word after the cursor.
- **Alt + Backspace:** Delete the word before the cursor.

#### Command History Shortcuts:

- **Up Arrow or Ctrl + P:** Move to the previous command in history.
- **Down Arrow or Ctrl + N:** Move to the next command in history.
- **Ctrl + R:** Search backward through the command history.
- **Ctrl + G:** Escape from history searching mode.
- **!!:** Repeat the last command.
- **!n:** Repeat the nth command in history.

#### Terminal Multiplexer (tmux) Shortcuts (if tmux is installed):

- **Ctrl + B, %:** Split the terminal vertically.
- **Ctrl + B, ":** Split the terminal horizontally.
- **Ctrl + B, Arrow keys:** Navigate between panes.
- **Ctrl + B, c:** Create a new window.
- **Ctrl + B, n:** Move to the next window.
- **Ctrl + B, p:** Move to the previous window.
- **Ctrl + B, d:** Detach from the current session.

#### Copy-Paste Shortcuts (when using a terminal emulator that supports them):

- **Ctrl + Shift + C:** Copy selected text.
- **Ctrl + Shift + V:** Paste copied text.

### 4.Mastering the Terminal - the Bash History

- The Bash history is a useful feature in the Bash shell that keeps a record of the commands you've entered during your session. 
- It allows you to review, reuse, and manage your command history efficiently. 

#### Basics:

1. **Command History Size:**
   - The number of commands stored in the history can be set using the `HISTSIZE` environment variable. For example:
     ```bash
     export HISTSIZE=1000
     ```

2. **History File:**
   - The history is usually saved to a file called `.bash_history` in the user's home directory.

#### Commands for Interacting with the History:

1. **`history` Command:**
   - Displays the command history along with line numbers.
     ```bash
     history
     ```

2. **`!!` (Double Bang):**
   - Repeats the last command.
     ```bash
     !!
     ```

3. **`!n` (History Expansion):**
   - Repeats the nth command from the history.
     ```bash
     !42
     ```

4. **`!-n` (Relative History):**
   - Repeats the command that appeared n commands ago.
     ```bash
     !-2
     ```

5. **`!string` (Search and Execute):**
   - Repeats the most recent command starting with "string."
     ```bash
     !ls
     ```

6. **`Ctrl + R` (Reverse Search):**
   - Initiates a reverse search in the history. Start typing a command, and it will find the most recent match.
     ```bash
     # Type Ctrl + R, then start typing
     ```

7. **`history -c` (Clear History):**
   - Clears the entire command history.
     ```bash
     history -c
     ```

8. **`history -d n` (Delete Entry):**
   - Deletes the entry at position n from the history.
     ```bash
     history -d 42
     ```

#### Customizing the History:

1. **`HISTCONTROL` Variable:**
   - Controls how commands are saved to the history. Common values include `ignorespace` (commands starting with a space are not saved) and `ignoredups` (ignores duplicate commands).

2. **`HISTFILE` Variable:**
   - Specifies the location of the history file. You can change it to use a different file.
     ```bash
     export HISTFILE=~/.my_custom_history
     ```

3. **`HISTTIMEFORMAT` Variable:**
   - If set, adds a timestamp to each history entry.
     ```bash
     export HISTTIMEFORMAT="%F %T "
     ```

#### Tips and Tricks:

1. **Persistent History Across Sessions:**
   - To ensure that history is saved and loaded between sessions, add the following to your `.bashrc` or `.bash_profile`:
     ```bash
     shopt -s histappend
     PROMPT_COMMAND="history -a"
     ```

2. **Ignore Commands from History:**
   - To prevent specific commands from being added to the history, precede them with a space.
     ```bash
     # This command won't be saved to history
      ls -l
     ```

3. **Execute a Command Without Saving to History:**
   - Use the `HISTCONTROL` variable with the value `ignorespace` or precede the command with a space.
     ```bash
     # This command won't be saved to history
      ls -l
     ```

### 5.Mastering the Terminal - The TAB Key

The `TAB` key is a powerful tool in the Linux terminal, providing various functionalities to ease command-line usage. Here's an in-depth look at the uses of the `TAB` key in the terminal:

#### 1. **Auto-Completion:**
   - One of the primary functions of the `TAB` key is auto-completion. When you start typing a command, file, or directory name and press `TAB`, the terminal will attempt to complete the entry based on the available options.
     ```bash
     ls Do<TAB>
     # Result: ls Documents/
     ```

#### 2. **Auto-Completion for Commands:**
   - Pressing `TAB` after typing a partial command will attempt to complete it, helping you avoid typing the full command.
     ```bash
     su<TAB>
     # Result: sudo
     ```

#### 3. **Auto-Completion for File and Directory Paths:**
   - Auto-completion works for file and directory paths, making it easier to navigate the filesystem.
     ```bash
     cd /ho<TAB>
     # Result: cd /home/
     ```

#### 4. **Auto-Completion for Filenames with Spaces:**
   - If a filename contains spaces, the `TAB` key will automatically escape the spaces, allowing you to continue typing.
     ```bash
     cat My\ Docu<TAB>
     # Result: cat My\ Documents/
     ```

#### 5. **Listing Available Options:**
   - Pressing `TAB` twice after a partial entry will display a list of available options, helping you choose from the available matches.
     ```bash
     ls D<TAB><TAB>
     # Result: Display list of options starting with D
     ```

#### 6. **Auto-Completion for Command Options:**
   - When typing command options, pressing `TAB` will auto-complete the option if there is a unique match.
     ```bash
     ls -l --h<TAB>
     # Result: ls -l --help
     ```

#### 7. **Auto-Completion for Variable Names:**
   - In some shells, pressing `TAB` can auto-complete variable names.
     ```bash
     $MY_VA<TAB>
     # Result: $MY_VARIABLE
     ```

#### 8. **Auto-Completion for Environment Variables:**
   - Environment variables can be auto-completed by pressing `TAB` after the `$` symbol.
     ```bash
     echo $HOM<TAB>
     # Result: echo $HOME
     ```

#### 9. **Command Substitution:**
   - When using command substitution with `$(...)`, pressing `TAB` can auto-complete the command within the substitution.
     ```bash
     ls -l $(echo /u<TAB>)
     # Result: ls -l $(echo /usr/)
     ```

#### 10. **File and Directory Listing:**
   - Pressing `TAB` after a command that expects a file or directory as an argument will list available options.
     ```bash
     cat /etc/p<TAB>
     # Result: cat /etc/passwd
     ```

#### Tips:
- **Double-Tap TAB:**
  - Double-tapping `TAB` will show a list of available options if there are multiple matches.
  
- **Cycle Through Options:**
  - If there are multiple matches, pressing `TAB` multiple times will cycle through the available options.

- **Case Sensitivity:**
  - `TAB` key completion is case-sensitive. Be aware of the case when using it.

- **Customization:**
  - The behavior of `TAB` completion can be customized using shell options and configuration files, such as `.bashrc` or `.bash_profile`.