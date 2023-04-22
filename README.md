# Git Tutorial

Hello World repository for Git tutorial
This is an example repository for the Git tutoial on <https://www.w3schools.com>

This repository is built step by step in the tutorial.

## 0. Configuration

```bash
$ git config --global user.email "you@example.com"
$ git config --global user.name "Your Name"
```

## 1. Create a new Git in empty repository

```bash
$ git init
```

## 2. Check status

```bash
$ git status

# Short status flags are:
#       ?? - Untracked files
#       A  - Files added to stage
#       M  - Modified files
#       D  - Deleted files
$ git status --short
```

## 2. Move files from local to staging environment

```bash
$ git add .
$ git add --all
$ git add -A
$ git add <file_1> 
$ git add <file_1> <file_2> ... <file_n>
```

## 3. Move files from staging environment to commit

```bash
$ git commit -m "Message to commit"

# Skip step git add . by use flag -a
$ git commit -a -m "Message to commit"
```

## 4. Check commit log

```bash
$ git log
```

## 5. Check git help

```bash
# See all the available options for the specific command
$ git <command> -help

# See all possible commands
git help --all
```

## 6. Git branch

* Without Git:
    - Make copies of all the relevant files to avoid impacting the live version
    - Start working with the design and find that code depend on code in other files, that also need to be changed!
    - Make copies of the dependant files as well. Making sure that every file dependency references the correct file name
    - EMERGENCY! There is an unrelated error somewhere else in the project that needs to be fixed ASAP!
    - Save all your files, making a note of the names of the copies you were working on
    - Work on the unrelated error and update the code to fix it
    - Go back to the design, and finish the work there
    - Copy the code or rename the files, so the updated design is on the live version
    - (2 weeks later, you realize that the unrelated error was not fixed in the new design version because you copied the files before the fix)

* With Git:
    - With a new branch called new-design, edit the code directly without impacting the main branch
    - EMERGENCY! There is an unrelated error somewhere else in the project that needs to be fixed ASAP!
    - Create a new branch from the main project called small-error-fix
    - Fix the unrelated error and merge the small-error-fix branch with the main branch
    - You go back to the new-design branch, and finish the work there
    - Merge the new-design branch with main (getting alerted to the small error fix that you were missing)

```bash
# Method 1: Use 2 command lines
$ git branch <New branch name>
$ git checkout <New branch name>

# Method 2: Combine 1 command line
$ git checkout -b <New branch name>
```

## 7. Git merge
Merge branch 2 into branch 1

```bash
$ git checkout <branch_1>
$ git merge <branch_2>
```

## 8. Git delete branch

```bash
$ git branch -d <branch_want_to_delete>
```