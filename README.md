# zerotomastery-devops-bootcamp-learn-linux

# Table of Contents

- [zerotomastery-devops-bootcamp-learn-linux](#zerotomastery-devops-bootcamp-learn-linux)
- [Table of Contents](#table-of-contents)
  - [1.Course Outline](#1course-outline)
  - [2.Setting Up the Environment](#2setting-up-the-environment)
  - [3.The Linux Terminal in Depth](#3the-linux-terminal-in-depth)
    - [1.Getting Help, Man Pages (man, type, help, apropos)](#1getting-help-man-pages-man-type-help-apropos)
    - [2.Linux Command Structure](#2linux-command-structure)

## 1.Course Outline

## 2.Setting Up the Environment

## 3.The Linux Terminal in Depth

### 1.Getting Help, Man Pages (man, type, help, apropos)

**man, type, help, and apropos** are all commands used in Unix-like operating systems to help users understand and use other commands. Here's a comparison:

- man: This command is short for "manual". It provides detailed manual pages for other commands. For example, man ls will provide a detailed manual for the ls command. It's a comprehensive source of information, but can be overwhelming for beginners.

- type: This command is used to describe how its argument would be interpreted if used as a command. It can tell you whether a command is built-in, an alias, a file, a function, etc. For example, type ls might output "ls is aliased to ls --color=auto", indicating that ls is an alias.

- help: This command is used to get a short description of a built-in command. It's less comprehensive than man, but can be easier to understand for beginners. For example, help cd will provide a short description of the cd command.

- apropos: This command is used to search the man page descriptions for instances of a keyword. It's useful when you know what you want to do, but you don't know the command. For example, apropos copy will list all commands that have the word "copy" in their description.

### 2.Linux Command Structure

command [options] [arguments]

- command: This is the action you want to perform. It could be a built-in command or a program installed in your system. Examples include ls, cd, grep, etc.

- [options]: These are modifiers that change the behavior of the command. They are usually prefixed with a - or --. For example, in the command ls -l, -l is an option that tells ls to display the output in a long listing format.

- [arguments]: These are the targets of the command. It could be a file, a directory, a string, or any other object the command may act upon. For example, in the command cd Documents, Documents is the argument, which is the directory cd will navigate to.

