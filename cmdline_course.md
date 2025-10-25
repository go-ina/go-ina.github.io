---
layout: default
title: Command-line Course
permalink: /cmdline_course.html
---

# Command-Line Course

## Introduction
The command-line course introduces the fundamental tools and principles of UNIX-based systems. Throughout the course, you will learn how to work efficiently in a terminal environment, gaining essential skills for manipulating files, automating tasks, and processing text. The goal is to help you become comfortable working directly from the command line so that you can understand and control the inner workings of your system.

Over several weeks, you’ll progress from basic navigation and file operations to writing scripts, processing structured data, and using professional tools such as Git and SSH. Each module builds upon the previous one, helping you gradually develop confidence and fluency in using the command line for practical, real-world tasks.

---

| Week            | Focus                       | Key Outcome                   |
| --------------- | --------------------------- | ----------------------------- |
| 1               | UNIX basics & permissions   | Confident navigation & safety |
| 2               | Text processing & pipelines | Reproducible transformations  |
| 3               | Scripting & configuration   | Automate repeatable tasks     |
| 4               | SSH, Git, Jekyll/Pages      | Publish a versioned website   |


---


## Week 1: Setting Up the Environment and UNIX Basics
This week, we began by installing our command-line environments, which are the foundation for everything we will be doing throughout the course. You can use your personal computer for this — instructions were provided for Windows, macOS, and Linux.

Once the environment was set up, we explored the basic UNIX commands that let us navigate and manipulate the file system:
- Navigating the filesystem with `cd`, `ls`, and `pwd`
- Performing file operations with `cp`, `mv`, `rm`, and `mkdir`
- Creating and viewing files using `touch`, `cat`, and `tail`
- Displaying output with `echo`
- Using `sudo` for administrator-level commands


- **`cd`** – changes the current directory 
	(e.g., `cd Documents` moves into the "Documents" folder)
- **`ls`** – lists the files and folders in the current directory
- `ls -l` shows them in a detailed view (permissions, size, date, etc.)
- **`pwd`** – prints the current working directory
- **`cp`** – copies files or directories 
	(e.g., `cp file1.txt backup/`)
- **`mv`** – moves or renames files 
	(e.g., `mv old.txt new.txt`)
- **`rm`** – removes (deletes) files; with `-r`, it can delete folders recursively
- **`mkdir`** – creates a new directory 
	(e.g., `mkdir new_folder`)
- **`touch`** – creates an empty file or updates its modification time
- **`cat`** – displays the contents of a file in the terminal
- **`tail`** – shows the last lines of a file
- **`echo`** – prints text or variables to the screen 
	(e.g., `echo Hello World`)
- **`sudo`** – runs a command with administrator (superuser) privileges.

We also learned about the structure of the UNIX file system, including standard system directories and file permissions that protect user privacy.  
At the end of the module, a short quiz helped reinforce these concepts and provided hands-on practice with the most common UNIX commands.

---

## Week 2: Text Processing in UNIX
This week focused on using text processing tools in UNIX. We began by learning about character encodings — the systems that represent text in binary form. Then we explored a variety of tools for searching and processing text files.

Key commands introduced this week include:
- Searching for patterns with `grep`
- Finding files and directories with `find`
- Extracting columns or fields using `cut`
- Editing or transforming text with `sed`
- Translating or deleting characters using `tr`
- Sorting and organizing text data with `sort`
- Generating frequency lists with `freqlist`

We also learned how to combine these commands into **pipelines**, chaining them together to perform complex tasks efficiently without creating temporary files. These skills are especially useful for linguistic and text analysis, where automation and precision are essential.


- **`grep`** – searches for specific patterns or words inside files  
	(e.g. `grep "error" logfile.txt` finds all lines containing the word *error*)
- **`find`** – searches for files and directories based on name, type, or other criteria  
	(e.g. `find . -name "*.txt"` lists all `.txt` files in the current directory and subfolders)
- **`cut`** – extracts specific columns or fields from each line of text  
	(e.g. `cut -d',' -f2 data.csv` extracts the second column from a comma-separated file)
- **`sed`** – stream editor for finding, replacing, or transforming text  
	(e.g. `sed 's/foo/bar/g' file.txt` replaces all occurrences of “foo” with “bar”)
- **`tr`** – translates or deletes characters in text streams  
	(e.g. `tr '[:lower:]' '[:upper:]' < names.txt` converts all letters to uppercase)
- **`sort`** – sorts lines of text alphabetically or numerically  
	(e.g. `sort -n scores.txt` sorts numbers in ascending order)  
- **`freqlist`** – a custom script used to generate word frequency lists from text files  
	(e.g `bin/freqlist.sh file.txt` outputs each unique word and how often it appears in 'file.txt')

## Example pipeline:

grep "error" logfile.txt | cut -d' ' -f5 | sort | uniq -c | sort -n


---

## Week 3 – Shell Scripting and Configuration

In this module, we started grouping our commands into **shell scripts** — small programs that automate repetitive tasks.  
Instead of typing the same commands again and again, we learned to save them in a file and make them executable.

We also explored **environment variables**, which control system behavior, and learned how to customize our setup using configuration files like `.bashrc` or `.profile`.

Commands like `echo` and `export` were used to test and define environment variables, and we practiced editing configuration files using text editors such as `nano` and `vim`.

This week also introduced simple package installation and configuration management, preparing us to work more independently on the command line.

---

### Common commands and concepts

- **Shell script** – a file containing a series of commands that can be run together.  
	(e.g. `myscript.sh` automates a process instead of running each command manually)  
- **`echo`** – prints text or variable values to the terminal (e.g., `echo $HOME` shows your home directory).  
- **`export`** – defines or modifies environment variables so they’re available to all processes  
	(e.g., `export PATH="$PATH:/my/bin"`)  
- **Environment variable** – a named value that influences system behavior (like `PATH`, `HOME`, `USER`).  
- **Configuration files** – special scripts that run automatically when you open a shell  
	(e.g., `.bashrc`, `.profile`)  
- **`chmod +x`** – gives a script permission to be executed.  
- **`#!/bin/bash`** – the “shebang” line at the top of a script that tells the system which interpreter to use.  

## Example shell script:

#!/bin/bash

# This script backs up a folder and saves it with today's date
SOURCE="$HOME/Documents"
DEST="$HOME/backup_$(date +%Y-%m-%d).tar.gz"

tar -czf "$DEST" "$SOURCE"
echo "Backup created at $DEST"



---

## Week 4: Using SSH, SCP, and Version Control
The final module focused on collaboration, remote access, and version control — all key parts of professional development workflows.

We learned to:
- Connect securely to remote systems using `ssh`
- Transfer files between machines with `scp`
- Manage project versions using `git`

Version control allows us to make changes without losing progress, restore previous versions, and collaborate efficiently with others.  
We practiced creating repositories, committing changes, pushing updates to GitHub, and resolving merge conflicts.  
GitHub, as the hosting platform for Git repositories, enabled us to share our work publicly and build personal project websites (like this one!) using **GitHub Pages**.

## Week 4 – Using SSH, SCP, and Version Control

The final module focused on collaboration, remote access, and version control — all key parts of professional development workflows.

We learned to:

- **Connect securely to remote systems using `ssh`**   
	(e.g. `ssh user@remote-server`)  
	→ Opens a secure terminal session on a remote machine  

- **Transfer files between machines with `scp`**  
	(e.g. `scp file.txt user@remote-server:/home/user/`)  
	→ Copies files securely over the network  

- **Manage project versions using `git`**  
	e.g.  
	git add .
	git commit -m "Update report"  
	git push origin main  


---

## Summary of Core Commands


### File System and Navigation
`cd`, `ls`, `pwd`, `cp`, `mv`, `rm`, `mkdir`, `touch`, `cat`, `tail`, `sudo`

### Text Editing and Output
`nano`, `echo`

### Searching and Text Processing
`grep`, `find`, `cut`, `tr`, `sed`, `sort`

### Networking and Downloading
`wget`, `ssh`, `scp`

### Version Control
`git`


<img src="{{ '/assets/images/programming.jpg' | relative_url }}" width=800>
