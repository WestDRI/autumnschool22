+++
title = "HPC Day 1 mid-day session"
slug = "hpc2"
+++

1. Are there any questions on the materials you just watched?
1. Let's go together through the challenges, do some exercises, and debug problems.

Click on a triangle to expand a question:

{{< question num=1 >}}
Let's log in to the training cluster. Try to access `/home`, `/scratch`, `/project` on the training cluster. Note that
these only emulate the real production filesystems and have no speed benefits on the training cluster.
{{< /question >}}

{{< question num=2 >}}
Edit a remote file in `nano` or `vi` or `emacs`. Use `cat` or `more` to view its content in the terminal.
{{< /question >}}

{{< question num=3 >}}
Load the default GNU compiler with `module` command. Which version is it? Try to understand what the module does: run
`module show` on it, `echo $PATH`, `which gcc`.
{{< /question >}}

{{< question num=4 >}}
Load the default Intel compiler. Which version is it? Does it work on the training cluster?
{{< /question >}}

{{< question num=5 >}}
Can you spot the third compiler family when you do `module avail`?
{{< /question >}}

{{< question num=6 >}}
What other modules does `scipy-stack/2022a` load?
{{< /question >}}

{{< question num=7 >}}
How many versions of python3 do we have? What about python2?
{{< /question >}}

{{< question num=8 >}}
Think of a software package that you use. Check if it is installed on the cluster, and share your findings.
{{< /question >}}

{{< question num=9 >}}
Transfer a file to/from the cluster (we did this already in bash class) using either command line or GUI. Type "done"
into the chat when done.
{{< /question >}}

{{< question num=10 >}}
Can you explain (1-2 sentences) how HPC can help us solve problems? Why a desktop/workstation not sufficient? Maybe, you
can give an example from your field?
{{< /question >}}

{{< question num=11 >}}
Try left+right or upper+lower split panes in `tmux`. Edit a file in one and run bash commands in the other. Trying
disconnecting and then reconnecting to the same session.
{{< /question >}}

{{< question num=12 >}}
In `introHPC/codes`, compile `{pi,sharedPi,distributedPi}.c` files. Try running a short serial code on the login node
(not longer than a few seconds: modify the number of terms in the summation).
{{< /question >}}

{{< question num=13a >}}
Write a makefile to replace these compilations commands with `make {serial,openmp,mpi}`.
{{< /question >}}

{{< question num=13b >}}
Add target `all`.

Add target `clean`. Try implementing `clean` for *all* executable files in the current directory, no matter what they
are called.
{{< /question >}}







<!-- {{< solution >}} -->
<!-- ```sh -->
<!-- function countfiles() { -->
<!--     if [ $# -eq 0 ]; then -->
<!--         echo "No arguments given. Usage: countfiles dir1 dir2 ..." -->
<!--         return 1 -->
<!--     fi -->
<!--     for dir in $@; do -->
<!--         echo in $dir we found $(find $dir -type f | wc -l) files -->
<!--     done -->
<!-- } -->
<!-- ``` -->
<!-- {{< /solution >}} -->
