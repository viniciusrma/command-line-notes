# ⛓Command Line ⛓

Welcome! This is a **resume about command line**. Hope you enjoy it!

From the command line, you can navigate through files and folders on your computer, just as you would with Finder on Mac OS or Windows Explorer on Windows.

The command line is a text interface for the computer’s operating system. To access the command line, we use the terminal.

- In the terminal, first you see **'$'.** 
This is called a **shell prompt**. It appears when the terminal is ready to accept a command.

A **filesystem** organizes a computer’s files and directories into a **tree structure**.

It **starts** with the **root directory**. Each parent directory can contain more child directories and files.

From the command line, you can navigate through files and folders on your computer. Right above there's good examples of commands that every programmer is going to use.  

## First Section - The most basic commands

1.  `pwd` stands for “print working directory”. Outputs the name of the current working directory.
```

$ pwd

```
2. `ls` means 'lists' all files and directories in the working directory. In filesystem folders are called directories.
```

$ ls

``` 
3. `cd` means change directory switches you into the directory you specify.
```

$ cd directoryname

``` 
4.  `cd ..` move up one directory.
```

$ cd ..

``` 
5.  `mkdir` means "make a directory". It creates a new directory in the working directory you are in,  but can also be used chained with the name of the directory you would like to create the new directory inside, like 'mkdir folderA/folderB'.
```

$ mkdir directoryname
$ mkdir directoryA/directoryB

``` 
6. 'touch' ``creates a new file inside the working directory you are in - but can also be used chained with the name of the directory you would like to create an file inside, like 'touch folderA/file.txt'.

```

$ touch filename
$ touch folderX/file.fileformat

``` 
## Second Section - Options to modify the behavior of commands:

1.  `ls-a` lists all contents of a directory, including hidden files and directories.
```

$ ls-a 

``` 
2.  `ls-l` lists all contents in long format, or table format.
```

$ ls-l 

``` 
3. `ls-t`orders files and directories by the time they were last modified
```

$ ls-t 

``` 
4. Multiple options can be used together, like `ls-alt`
```

$ ls-alt 

``` 
### Third Section - Commands to copy, move, and remove files and directories:

1. `cp` command copies files or directories. Here, we copy the contents of **filenameA.txt** into **filenameB.txt**.
```

$ cp filenameA filenameB

``` 
2. `mv`  moves files. It’s similar to `cp` in its usage.
```

$ mv filename.fileformat directoryname 

``` 
3. `rm`  removes files.
```

$ rm filename.fileformat

``` 
4. `rm-r` removes directories. It is an option that modifies the behavior of the `rm` command. The `-r` stands for “recursive,” and it’s used to delete a directory and all of its child directories.
```

$ rm-r directoryname

``` 
---
<h4  align="center">
Made by <a  href="https://www.linkedin.com/in/viniciusrma/"  target="_blank">Vinícius Morais</a>
</h4>