+++
title = "HPC Day 2 morning session"
slug = "hpc3"
+++

1. Let's continue with the questions we did not finish on Tuesday.

{{< question num=14 >}}
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

<!-- here paste the answered questions from Tuesday -->

2. Review the program for this morning: you have **1h15m** of videos to watch until 11:30am Pacific.

By mid-day you should be familiar with:

- how jobs are scheduled in Slurm
- submitting ...
  - serial, shared-memory, distributed-memory and hybrid jobs
  - array jobs
  - interactive jobs, and switching between interactive and batch jobs for the same task
- how to estimate memory requirements of a completed Slurm job

Some of the hands-on exercises we will do in the mid-day Zoom session:

- Using a serial job, time optimized (-O2) vs. unoptimized C code.
- Using a serial job, time a C code vs. a Python code.
- Submit an array job for different number of terms in the summation of \pi.
- Try scaling an MPI job with 1 -> 2 -> 4 -> 8 cores and measuring the speedup.
- Test a code inside an interactive job.

<!-- - Edit a remote file in nano or vi or emacs. -->
<!-- - Try to understand what the default GNU compiler module does: run `module show` on it, print `PATH` -->
<!--   variable, locate the GNU C compiler. -->
<!-- - Check if your favourite research software is installed on the cluster. -->
<!-- - Write a makefile from scratch. -->
<!-- - Try left+right or upper+lower split panes in tmux on the cluster. -->
