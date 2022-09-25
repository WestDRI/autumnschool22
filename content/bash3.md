+++
title = "Bash Day 2 morning session"
slug = "bash3"
+++

1. Let's continue with the questions we did not finish on Tuesday.

<!-- here paste the answered questions from Tuesday -->

{{< question num=18 >}}
Using Unix pipes, write a one-line command to show the name of the longest .pdb file (by the number of lines). Paste
your answer into the chat.
{{< /question >}}

{{< question num=19 >}}
Combine `ls` and `head` and/or `tail` into a one-line command to show three largest files (by the number of bytes) in a
given directory. Paste your answer into the chat.
{{< /question >}}

{{< question num=20 >}}
Write a loop that concatenates all .pdb files in `data-shell/molecules` subdirectory into one file called
`allmolecules.txt`, prepending each fragment with the name of the corresponding .pdb file, and separating different
files with an empty line. Run the loop, make sure it works, bring it up with the "*up arrow*" key and paste into the
chat.
{{< /question >}}

{{< question num=21 >}}
Use Ctrl-C to kill an infinite (or very long) loop. (no need to type any answer)
{{< /question >}}

{{< question num=22 >}}
Play with variables and their values. Change the prompt, e.g. `PS1="\u@\h \w> "`. (no need to type any answer)
{{< /question >}}

{{< question num=23 >}}
What will the command `echo directoryName/*` do? Try answering without running it. How is this output different from `ls
directoryName` and `ls directoryName/*`?
{{< /question >}}

{{< question num=24 >}}
What will the loop `for i in hello 1 2 * bye; do echo $i; done` print? Try answering without running the loop.
{{< /question >}}

{{< question num=25 >}}
Pasting variables into strings:
```sh
var="sun"
echo $varshine
echo ${var}shine
echo "$var"shine
```
(no need to type any answer)
{{< /question >}}

{{< question num=26 >}}
Create a loop that writes into 10 files `chapter01.md`, `chapter02.md`, ..., `chapter10.md`. Each file should contain
chapter-specific lines, e.g. `chapter05.md` will contain exactly these lines:
```sh
## Chapter 05
This is the beginning of Chapter 05.
Content will go here.
This is the end of Chapter 05.
```
(no need to type any answer)
{{< /question >}}

{{< question num=27 >}}
Redirection `1>` and `2>` and `/dev/null` (no need to type any answer)
{{< /question >}}

{{< question num=28 >}}
`;` vs. `&&` separators, e.g. `mkdirr tmp; cd tmp` (no need to type any answer)
{{< /question >}}

{{< question num=29 >}}
Variable manipulation:
```sh
myvar="hello"
echo $myvar
echo ${myvar:offset}
echo ${myvar:offset:length}
echo ${myvar:2:3}    # 3 characters starting from character 2
echo ${myvar/l/L}    # replace the first match of a pattern
echo ${myvar//l/L}   # replace all matches of a pattern
```
(no need to type any answer)
{{< /question >}}

{{< question num=30 >}}
Using knowledge from the previous question, write a loop to replace spaces to underscores in all file names in the
current directory.
```sh
touch hello "first phrase" "second phrase" "good morning, everyone"
ls -l
ls *\ *
```
{{< /question >}}

{{< question num=31 >}}
Why `mv *.txt *.bak` does not work? Write a loop to rename all .txt files to .bak files. There are several solutions for
changing a file extension inside a loop you know by now.
{{< /question >}}

{{< question num=32 >}}
Are there questions on any of the topics that we covered today? You can type your question into the chat, ask via audio
(unmute), or raise your hand in Zoom.
{{< /question >}}

2. Review the program for this morning: you have **1h4m** of videos to read/watch until 11:30am Pacific.

By mid-day you should be able to:

- write a multi-line bash script and a bash function
- process command-line arguments in this script / function
- search inside files with `grep`
- search the filesystem with `find`
- perform basic text manipulation with `sed`, `tr`, `awk`

Some of the hands-on exercises we will do in the mid-day Zoom session:

- Write a function archive() to replace directories with their gzipped archives.
- Write a one-line command that will search for a string in all files in the current directory and all
  its subdirectories, and will hide errors (e.g. due to permissions).
- Write a one-line command that finds 5 largest files in the current directory and prints only their
  names and file sizes in the human-readable format (indicating bytes, kB, MB, GB, ...) in the decreasing
  file-size order. Hint: use `find`, `xargs`, and `awk`.
