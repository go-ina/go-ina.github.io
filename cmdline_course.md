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

We also learned about the structure of the UNIX file system, including standard system directories and file permissions that protect user privacy.  
At the end of the module, a short quiz helped reinforce these concepts and provided hands-on practice with the most common UNIX commands.
## Example: Navigating the File System
pw
ls -l
cd Documents

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

---

## Week 3: Scripting, Configuration Files, and Installing Programs
In this module, we started grouping our commands into **shell scripts** — small programs that automate repetitive tasks. Instead of typing commands one by one, we wrote and executed scripts to solve more complex problems.

We explored **environment variables**, which control system behavior, and learned how to customize our setup using configuration files such as `.bashrc`.  
Commands like `echo` and `export` were used to test and define environment variables, and we practiced editing configuration files using text editors like `nano` and `vim`.

This week also introduced simple package installation and configuration management, preparing us to work more independently on the command line.

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

---

## Summary of Core Commands


### File System and Navigation
`cd`, `ls`, `pwd`, `cp`, `mv`, `rm`, `mkdir`, `touch`, `cat`, `tail`, `sudo`

### Text Editing and Output
`nano`, `vim`, `echo`

### Searching and Text Processing
`grep`, `find`, `cut`, `tr`, `sed`, `sort`

### Networking and Downloading
`wget`, `ssh`, `scp`

### Version Control
`git`


<img src="{{ '/assets/images/programming.jpg' | relative_url }}" width=800>
