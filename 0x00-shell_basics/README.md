# 0x00. Shell, Navigation

This will be your first introduction to an Unix terminal.
All projects will be tested on 'Ubuntu 20.04'

## Resources

* [Linux Navigation](http://linuxcommand.org/lc3_lts0020.php)
* [Linux - Looking around](http://linuxcommand.org/lc3_lts0030.php)
* [Linux - Manipulating files](http://linuxcommand.org/lc3_lts0050.php)

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
