This is the new training for Alx
These answers were suggested

Amarachi Enwerem
 14:26
for the 0x02-shell_redirections tasks

cd alx-system_engineering-devops
mkdir 0x02-shell_redirections
cd 0x02-shell_redirections
echo 'Shell I/O redirections' > README.md

TASK 0
vi 0-hello_world
{click "i" to enter insert mode}
#!/bin/bash
echo "Hello, World"
{click esc to re-enter command mode}
:wq

TASK 1
vi 1-confused_smiley
#!/bin/bash
echo "\"(Ôo)'"
:wq

TASK 2
vi 2-hellofile
#!/bin/bash
cat /etc/passwd
:wq

TASK 3
vi 3-twofiles
#!/bin/bash
cat /etc/passwd  /etc/hosts
:wq

TASK 4
vi 4-lastlines
#!/bin/bash
tail  /etc/passwd
:wq

TASK 5
vi 5-firstlines
#!/bin/bash
head -10 /etc/passwd
:wq

TASK 6
vi 6-third_line
#!/bin/bash
head --lines=3 iacta | tail --lines=1
:wq

TASK 7
vi 7-file
#!/bin/bash
echo "Best School" > \\\*\\\\\'\"Best\ School\"\\\'\\\\\*\$\\\?\\\*\\\*\\\*\\\*\\\*\:\)
:wq

TASK 8
vi 8-cwd_state
#!/bin/bash
ls -la >> ls_cwd_content
:wq

TASK 9
vi 9-duplicate_last_line
#!/bin/bash
tail --lines=1 iacta >> iacta
:wq

TASK 10
vi 10-no_more_js
#!/bin/bash
find . -type f -name '*.js' -delete
:wq

TASK 11
vi 11-directories
#!/bin/bash
find . -type d -path './*' -print | wc -l
:wq

TASK 12
vi 12-newest_files
#!/bin/bash
ls -t | head
:wq

TASK 13
vi 13-unique
#!/bin/bash
sort | uniq -u
:wq

TASK 14
vi 14-findthatword
#!/bin/bash
grep -i "root" /etc/passwd
:wq

TASK 15
vi 15-countthatword
#!/bin/bash
grep -c "bin" /etc/passwd
:wq

TASK 16
vi 16-whatsnext
#!/bin/bash
grep -iA 3 "root" /etc/passwd
:wq

TASK 17
vi 17-hidethisword
#!/bin/bash
grep -v "bin" /etc/passwd
:wq

TASK 18
vi 18-letteronly
#!/bin/bash
grep '^[A-Za-z]' /etc/ssh/sshd_config
:wq

TASK 19
vi 19-AZ
#!/bin/bash
tr Ac Ze
:wq

TASK 20
vi 20-hiago
#!/bin/bash
tr -d cC
:wq

TASK 21
vi 21-reverse
#!/bin/bash
rev
:wq

TASK 22
vi 22-users_and_homes
#!/bin/bash
cut -d':' -f1,6 /etc/passwd | sort
:wq

ADVANCED TASK 1
vi 100-empty_casks
#!/bin/bash
find . -empty -printf %f'\n'
:wq

ADVANCED TASK 2
vi 101-gifs
#!/bin/bash
find . -type f -name \*.gif -printf "%f\n" | LC_ALL=C sort -f | rev | cut -b 5- | rev
:wq

ADVANCED TASK 3
vi 102-acrostic
#!/bin/bash
cut -c 1 | paste -s -d ''
:wq

ADVANCED TASK 4
vi 103-the_biggest_fan
#!/bin/bash
tail -n +2 | cut -f -1 | sort -k 1 | uniq -c | sort -rnk 1 | head -n 11 | rev | cut -d ' ' -f -1 | rev
:wq

N.B: do not forget to run the chmod u+x command for the files
and remember you can use it for multiples files at a time. e.g
chmod u+x 0-hello_world  1-confused_smiley 2-hellofile e.t.c
