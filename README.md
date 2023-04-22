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
