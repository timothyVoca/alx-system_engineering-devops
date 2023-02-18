# 0x00. Shell, Navigation

This will be your first introduction to an Unix terminal.
All projects will be tested on 'Ubuntu 20.04'

## Resources

*Read or Watch:*
* [Linux Navigation](http://linuxcommand.org/lc3_lts0020.php)
* [Linux - Looking around](http://linuxcommand.org/lc3_lts0030.php)
* [Linux - Manipulating files](http://linuxcommand.org/lc3_lts0050.php)

*Or in your terminsl:*
- `man pwd`
- `man ls`
- `man cd`
- `man less`
- `man touch`
- `man cp`
- `man mv`
- `man rm`
- `man mkdir`
- `man rmdir`

## Linux Navigation

You can always find the manual on a command by using `man <command>` in the terminal.

- `pwd`: print working directory.
- `cd`: change directory.
- `ls`: List files and directories.
- `cd ..`: change to the parent directory. This is a relative command.
- `cd -`: change to the pevious directory.
- `cd ./bin`: change to the bin directory within the working directory.
- `cd`: change to the root directory.

## Linux - Looking Around

Below are a few examples
- `less`: view text files.
- `file`: classify a file's content.
- `ls /bin`: list the files in the /bin folder
- `ls -l`: list files in thee working directory in long format
- `ls -l /etc /bin`: list files in the `/bin` directory and the `/etc` directory in long format.
- `ls -a`: list all files, including hidden files.
- `ls -la`: list all files in long format, including hidden files.

### A Closer look at Long format (introduction)

`ls -l` lists files in long format and it would look like this:
`drwxrwxr-x` `6 me` `me` `1024` `Oct 9 2019` `webname`

- `drwxrwxr-x` refers to the file permissions on the file (-) or directory (d). There will be more information on this [here]
- `6 me` which is next, refers to the owner (u) of the file or directory.
- `me` which is next, refers to the Group (g) with access to the file or directory.
- `1024` refers to a series of numbers that  refer to the size (in bytes) of the file ot directory.
- `Oct 9 2019` shows the last modification date and time.
- `webname` refers to the name of the file or directory.

---

- `less`: is a default program in unix that lets you view text files.

> ## What is `text`?
> computers can not directly read text files. They mostly read numbers. Hence there needs to be a means to convert text files to numbers and vice versa. One of the earliest and simplest method is the ASCII text (pronounced as "As-Key"), which is short for American Standard Code for Information Interchange.
>
> Text is a simple one-to-one mapping of characters to numbers. 50 characters of text translates to 50 bytes of data. 

## Linux - Manipulating Files

These are the commands most frequently used to mnipulate both files and directories in Linux commands.

- `cp`: copy files and directories.
- `mv`: move or rename file snd directories.
- `rm`: remove files and directories.
- `mkdir`: create directories.

An example of this is `cp -u *.html <destination>`

## Wildcards

- `*` is one example of Wildcards. It means matching any characters. So, `*.html` means match any characters with `.html`
- `?` means matches any single character.
- `[characters]` matches any character that is a member of the set characters. The characters my be one of the following types below:
	- `[:alnum:]` for Alphanumeric characters.
	- `[:alpha:]` for Alphabetic characters.
	- `[:digit:]` for Numerals.
	- `[:upper:]` for Uppercase alphabetic characters.
	- `[:lower:]` for Lowercase alphabetic characters.
- `[!characters]`matches any character that is not a member of the set characters.

You can use wildcards to make multiple selection criterias. For example:
- `*` means All filenames
- `g*` means All filenames that begin with the character "g"
- `b*.txt` means All filenames that begin with the character "b" and end with the character ".txt"
- `Data???` means Any filename that begins with the characters "Data" followed by exactly 3 more characters
- `[abc]*` means Any filename that begins with "a" or "b" or "c" followed by any other characters.
- `[[:upper:]]` meand Any filename that begins with an uppercase letter. This is an example of a character class.
- `BACKUP [[:digit:]] [[:digit:]]` means Any filename that begins with the characters "BACKUP", followed by exactly two numericals.
- `*[![:lower:]]` means filenames that does not end with a lowercase letter

## `cp`

This copies files and directories. The simplest form is:
`cp file1 file2` or
`cp file1 directory`

Examples of `cp` and its options are
- `cp file1 file2`: Copy content of file1 into file2. If file2 doesn't exist, it is created. If it exists, it is overwritten.
- `cp -i file1 file2`: Same as above but "-i" (interactive) options means if file2 exists, prompt user if it should be overwritten or not.
- `cp file1 dir1': Copy content of file1 (into a file named file1) inside of directory dir1
- 'cp -R dir1 dir2`: Copy the content of directory dir1. If directory dir2 doesn't exist, create it. Else it creates a directory named dir1 within directory dir2.

These principles are similat for `mv` and `rm`. 

## Using Commands with Wildcards

- `cp *.txt text_files` means Copy all files in the working directory with names ending with the characters ".txt" to an existing directory named test_files.
- `mv dir ../*.bak dir2` means Move the subdirectory dir1 and all the files ending in ".bak" in the current working directory's parent directory to an existing directory named dir2
- `rm *~` meand Delete all files in the current working directory that end with the character "~". Some applications create backup files using this naming scheme. You can use this tl clean them out.
