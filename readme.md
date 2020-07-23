
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
2.  `ls` means 'lists' all files and directories in the working directory. In filesystem folders are called directories.

```
  

$ ls
  

```

3.  `cd` means change directory switches you into the directory you specify.

```
  

$ cd directoryname
  

```

4.  `cd ..` move up one directory.

```
  

$ cd ..
  

```
5.  `mkdir` means "make a directory". It creates a new directory in the working directory you are in, but can also be used chained with the name of the directory you would like to create the new directory inside, like 'mkdir folderA/folderB'.

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

3.  `ls-t`orders files and directories by the time they were last modified
```
  

$ ls-t
  

```

4. Multiple options can be used together, like `ls-alt`
```

  
$ ls-alt

  
```

### Third Section - Commands to copy, move, and remove files and directories:

  1.  `cp` command copies files or directories. Here, we copy the contents of **filenameA.txt** into **filenameB.txt**.
```

  
$ cp filenameA filenameB

  
```

2.  `mv` moves files. It’s similar to `cp` in its usage.
```
  

$ mv filename.fileformat directoryname
  

```

3.  `rm` removes files.
```
  

$ rm filename.fileformat
  

```

4.  `rm-r` removes directories. It is an option that modifies the behavior of the `rm` command. The `-r` stands for “recursive,” and it’s used to delete a directory and all of its child directories.
```

  
$ rm-r directoryname
  

```

### Fourth Section - Commands to redirect standard input and standard output.:

1.  `echo` The echo command accepts a string as standard input, and echoes the string back to the terminal as standard output.

```
  
  
$ echo "Hello"
Hello
  
  
```

Standard **input**, abbreviated as `stdin`, is information inputted into the terminal through the keyboard or input device.

Standard **output**, abbreviated as `stdout`, is the information outputted after a process is run.

Standard **error**, abbreviated as `stderr`, is an error message outputted by a failed process.

---

  

### How the redirect works

1.  `>` redirects standard output of a command to a file, taking the standard output of the command on the left, and redirecting it to the file on the right, overwriting previous content.
```
  

$ echo "Hello" > hello.txt
  

```
The `>` command redirects the standard output to a file.

Here, **Hello** is entered as the standard input. The standard output "Hello" is redirected by `>` to the file hello.txt.

2.  `>>` redirects standard output of a command to a file, taking the standard output of the command on the left, and appending it to the file on the right.
```
  

$ cat hello.txt >> hi.txt
  

```
You can view the output data of the file with `cat` and the filename.  

3.  `cat` The cat is short for *concatenate command* is one of the most frequently used command in command lines.
```
  

$ cat hello.txt >> hi.txt
  

```
It concatenate both files and print on the standard output.

4.  `<` redirects standard input to a command. It takes the standard input from the file on the right and inputs it into the program on the left.
```

  
$ cat < hello.txt
  

```
Here, hello.txt is the standard input for the `cat` command. The standard output appears in the terminal.

Basically cat is the command to display any file content to the terminal.

5.  `|` means a **pipe** and it takes the standard output of the command on the left, and pipes it as standard input to the command on the right.

You can think of this as “command to command” redirection.

```
  

$ cat hello.txt | wc
  

```
ere the output of cat hello.txt is the standard input of `wc`.

6.  `wc` is short for *word count* and it reads either standard input or a list of files and generates one or more of the following statistics: *newline count*, *word count*, and *byte count*.

```

  
$ cat hello.txt | wc
  

```
Here, the `wc` command outputs the number of *lines*, *words*, and *characters* in hello.txt, respectively.

**Other commands that are powerful when combined with redirection commands**

6.  `sort` takes the standard input and orders it alphabetically for the standard output.
```

  
$ sort places.txt
  

```
Here, the places in sort places.txt are listed in alphabetical order.
```
  

$ cat places.txt | sort > sorted-places.txt
  

```
Here, the command takes the standard output from cat places.txt and “pipes” it to sort. The standard output of sort is redirected to sorted-places.txt.

7.  `uniq` stands for “unique” and filters out adjacent, duplicate lines in a file. Adjacent means *directly follows the previous instance*.

```
  

$ uniq places.txt
  

```

Here uniq places.txt filters out duplicates lines, tha follows directly the previous instance inside of it.

```
  

sort places.txt | uniq > uniq-places.txt
  

```
Here by piping sort places.txt to uniq, all duplicate lines are alphabetized (and thereby made adjacent), filtered out, and then send filtered contents to uniq-places.txt

8.  `grep` stands for *global regular expression print*. It searches files for lines that match a pattern and returns the results. It is also case sensitive.

```
  

$ grep Restaurant places.txt
  

```
Here, grep searches for Restaurante in places.txt.

`grep -i` `i` enables the command to be case *insensitive*.

```
  

$ grep -i Restaurant places.txt
  

```
Here, `grep -i` searches for capital or lowercase strings that match Restaurant in places.txt.

`grep -R`  `-R` stands for “recursive”.

```
  

$ grep -R Restaurant /home/workspace/places
  

```
Here grep -R searches the /home/workspace/places directory for the string Restaurant and outputs filenames and lines with matched results.

`grep -Rl` searches all files in a directory and outputs only filenames with matched results.

`R` stands for *recursive* and `l` stands for *files with matches*.

```
  

$ grep -Rl Restaurant /home/workspace/places
  

```
Here grep `-Rl` searches the /home/workspace/places directory for the string Restaurant and outputs filenames with **matched** results.

9.  `sed` stands for *stream editor*. It accepts standard input and modifies it based on an expression, before displaying it as output data. It is similar to *find and replace*.
```

  

$ sed 's/drugstore/bakery/' places.txt

  

```
-  `s` stands for “substitution”. it is always used when using sed for substitution.
-  `drugstore` the search string, the text to find.
-  `bakery` the replacement string, the text to add in place.

In this case, `sed` searches places.txt for the word *drugstore* and replaces it with *bakery*.

---

<h4  align="center">

Made by <a  href="https://www.linkedin.com/in/viniciusrma/"  target="_blank">Vinícius Morais</a>

</h4>
