+++
title = "HPC mid-day session"
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

{{< question num=14 >}}
Julia parallelism was not mentioned in the videos. Let's quickly talk about it (slide 29).
{{< /question >}}

{{< question num=14b >}}
Suggest a computational problem to parallelize. Which of the parallel tools mentioned in the videos would you use, and
why?

If you are not sure about the right tool, suggest a problem, and we can brainstorm the approach together.
{{< /question >}}


{{< question num=15 >}}
If you use Python or R in your work, try running a Python or R script in the terminal.

If this script depends on packages, try installing them in your own directory with `virtualenv`. Probably, only a few of
you should do this on the training cluster at the same time.
{{< /question >}}

{{< question num=16 >}}
Any remaining questions? Type your question into the chat, ask via audio (unmute), or raise your hand in Zoom.
{{< /question >}}

3. Review the program for this afternoon: you have **1h15m** of videos to watch until 2:30pm Pacific.

By the end of this workshop you should be familiar with:

- how jobs are scheduled in Slurm
- submitting ...
  - serial, shared-memory, distributed-memory and hybrid jobs
  - array jobs
  - interactive jobs, and switching between interactive and batch jobs for the same task
- how to estimate memory requirements of a completed Slurm job

Some of the hands-on exercises we will do in the late afternoon Zoom session:

- Using a serial job, time optimized (-O2) vs. unoptimized C code.
- Using a serial job, time a C code vs. a Python code.
- Submit an array job for different number of terms in the summation of \pi.
- Try scaling an MPI job with 1 -> 2 -> 4 -> 8 cores and measuring the speedup.
- Test a code inside an interactive job.






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
