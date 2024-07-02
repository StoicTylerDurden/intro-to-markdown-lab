# How to create a file using the terminal

## Welcome to the terminal 
* The **terminal** is a text interface for executing text-based programs. If you're running any tooling for web development there's a near-guaranteed chance that you'll have to pop open the command line and run some commands to use your chosen tools (you'll often see such tools referred to as CLI tools — command line interface tools).


## Basic built-in terminal commands
* Navigate your computer's file system along with base-level tasks such as _create_, _copy_, _rename_, and _delete_:
    * Move around your directory structure: `cd`
    * Create directories: **`mkdir`**
    * Create files (and modify their metadata): **`touch`**
    * Copy files or directories: **`cp`**
    * Move files or directories: **`mv`**
    * Delete files or directories: **`rm`**
* Download files found at specific URLs: **`curl`**
* Search for fragments of text inside larger bodies of text: **`grep`**
* View a file's contents page by page: **`less`**, **`cat`**
* Manipulate and transform streams of text (for example changing all the instances of `<div>`s in an HTML file to `<article>`): `awk`, `tr` `sed`


### Navigation on the command line
The cd command lets you Change Directory. Technically, cd isn't a program but a built-in. This means your operating system provides it out of the box, and also that you can't accidentally delete it — thank goodness! You don't need to worry too much about whether a command is built-in or not, but bear in mind that built-ins appear on all unix-based systems.

To change the directory, you type cd into your terminal, followed by the directory you want to move to. Assuming the directory is inside your home directory, you can use cd Desktop.

![code on a laptop stuff](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Understanding_client-side_tools/Command_line/win-terminals-cd.png)

```bash
cd Desktop
```

If you want to move back up to the previous directory, you can use two dots:

```bash
cd ..
```

> Note: A very useful terminal shortcut is using the tab key to autocomplete names that you know are present, rather than having to type out the whole thing. For example, after typing the above two commands, try typing cd D and pressing tab — it should autocomplete the directory name Desktop for you, provided it is present in the current directory. Bear this in mind as you move forward.

<br> </br>
For example, if you wanted to go to a directory called `src`, located inside a directory called `project`, located on the `Desktop`, you could type these three commands to get there from your home folder:

```Bash
cd Desktop
cd project
cd src
```

But this a waste of time — instead, you can type one command, with the different items in the path separated by forward slashes, just like you do when specifying paths to images or other assets in CSS, HTML, or JavaScript code:

```bash
cd Desktop/project/src
```
<br> </br>
### Listing directory contents
Another built-in Unix command is **ls** (short for list), which lists the contents of the directory you're currently in. Note that this won't work if you're using the default Windows command prompt (**cmd**) — the equivalent there is **dir**.

Try running this now in your terminal:

```bash
ls
```
This gives you a list of the files and directories in your present working directory, but the information is really basic — you only get the name of each item present, not whether it is a file or a directory, or anything else. Fortunately, a small change to the command usage can give you a lot more information.

### Introducing command options
Most terminal commands have options — these are modifiers that you add onto the end of a command, which make it behave in a slightly different way. These usually consist of a space after the command name, followed by a dash, followed by one or more letters.

For example, give this a go and see what you get:

```bash
ls -l
``` 
<br> </br>
![code on a laptop stuff](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Understanding_client-side_tools/Command_line/mac-terminals-ls.png)

### Creating, copying, moving, removing

There are a number of other basic utility commands that you'll probably end up using quite a lot as you work with the terminal. They are pretty simple, so we won't explain them all in quite as much detail as the previous couple.

Have a play with them in a test directory you've created somewhere so that you don't accidentally delete anything important, using the example commands below for guidance:

* `mkdir` — this creates a new directory inside the current directory you are in, with the name you provide after the command name. For example, mkdir my-awesome-website will make a new directory called my-awesome-website.

* `rmdir` — removes the named directory, but only if it's empty. For example, rmdir my-awesome-website will remove the directory we created above. If you want to remove a directory that is not empty (and also remove everything it contains), then you can use rm -r instead (see below), but this is dangerous. Make sure there is nothing you might need inside the directory later on, as it will be gone forever.

* `touch` — creates a new empty file, inside the current directory. For example, touch mdn-example.md creates a new empty file called mdn-example.md.

* `mv` — moves a file from the first specified file location to the second specified file location, for example mv mdn-example.md mdn-example.txt (the locations are written as file paths). This command moves a file called mdn-example.md in the current directory to a file called mdn-example.txt in the current directory. Technically the file is being moved, but from a practical perspective, this command is actually renaming the file.

* `cp` — similar in usage to mv, cp creates a copy of the file in the first location specified, in the second location specified. For example, cp mdn-example.txt mdn-example.txt.bak creates a copy of mdn-example.txt called mdn-example.txt.bak (you can of course call it something else if you wish).
* `rm` — removes the specified file. For example, rm mdn-example.txt deletes a single file called mdn-example.txt. Note that this delete is permanent and can't be undone via the recycle bin that you might have on your desktop user interface.

### Summary
That brings us to the end of our brief tour of the terminal/command line, you can learn more details by clicking the following link.

[MDN Introduction to CMD](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Understanding_client-side_tools/Command_line)