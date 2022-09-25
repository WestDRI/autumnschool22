+++
title = "Bash closing session"
slug = "bash4"
+++

1. Are there any questions on the materials you just watched?
1. Let's go together through the challenges, do some exercises, and debug problems.

Click on a triangle to expand a question:

{{< question num=33 >}}
File permissions (no need to type any answer)
{{< /question >}}

{{< question num=34 >}}
In the `molecules` directory (download link mentioned <a href="../bash/bash-04-tar-gzip" target="_blank">here</a>),
create a shell script called `scan.sh` containing the following:
```sh
#!/bin/bash
head -n $2 $1
tail -n $3 $1
```
While you are in that current directory, you type the following command (with space between two 1s):
```sh
./scan.sh  '*.pdb'  1  1
```
What output would you expect to see?
{{< /question >}}

{{< question num=35 >}}
```txt
The Tao that is seen
Is not the true Tao, until
You bring fresh toner.
With searching comes loss
and the presence of absence:
"My Thesis" not found.
Yesterday it worked.
Today it is not working.
Software is like that.
```
From the above text, contained in the file `haiku.txt`, which command would result in the following output:
```txt
and the presence of absence
```
{{< /question >}}

{{< question num=36 >}}
The `-v` flag to `grep` inverts pattern matching, so that only lines that do not match the pattern are printed. Given
that, which of the following commands will find all files in `/data` whose names end in `ose.dat` (e.g., `sucrose.dat`
or `maltose.dat`), but whose names do not contain the word `temp`?
{{< /question >}}

{{< question num=37 >}}
Write a one-line command that will search for a string in all files in the current directory and all its subdirectories,
and will hide errors (e.g. due to permissions).
{{< /question >}}

{{< question num=38 >}}
Play with command substitution using both `$(...)` and ``` `...` ``` syntax. (no need to type any answer)
{{< /question >}}

{{< question num=39a >}}
Write a script that takes an English-language file and print the list of its 100 most common words, along with the word
count. Hint: use the workflow from the text manipulation video. Finally, convert this script into a bash function. (no
need to type any answer)
{{< /question >}}

{{< question num=39b >}}
Write a function `countFiles()` to count files in all directories passed to it as arguments (need to loop through all
arguments). At the beginning add the check:
```sh
    if [ $# -eq 0 ]; then
        echo "No arguments given. Usage: countfiles dir1 dir2 ..."
        return 1
    fi
```
{{< /question >}}

{{< question num=40 >}}
Write a function `archive()` to replace directories with their gzipped archives.
```sh
$ ls -F
chapter1/  chapter2/  notes/
$ archive chapter* notes/
$ ls
chapter1.tar.gz  chapter2.tar.gz  notes.tar.gz
```
(no need to type any answer)
{{< /question >}}

{{< question num=41a >}}
Write a one-line command that finds 5 largest files in the current directory and prints only their names and file sizes
in the human-readable format (indicating bytes, kB, MB, GB, ...) in the decreasing file-size order. Hint: use `find`,
`xargs`, and `awk`.
{{< /question >}}

{{< question num=41b >}}
Let's discuss incorporating scripts from other languages into bash, as suggested in 
<a href="../bash/bash-08-scripts-functions/#scripts-in-other-languages" target="_blank">this Python example</a>.
{{< /question >}}

{{< question num=42 >}}
Let's study together these commands:
```sh
$ source ~/projects/def-sponsor00/shared/fzf/.fzf.bash
$ kill -9 `/bin/ps aux | fzf | awk '{print $2}'`
```
{{< /question >}}

{{< question num=43 >}}
Are there questions on any of the topics that we covered today? You can type your question into the chat or ask via
audio (unmute), or raise your hand in Zoom.
{{< /question >}}
