+++
title = "HPC opening session"
slug = "hpc1"
+++

1. Instructor / helpers / course introduction.
1. Distribute the usernames and passwords.
1. Let's try to log in to the training cluster.
1. Download [today's materials](http://bit.ly/introhpc2) (ZIP file with slides and codes inside).
1. Review the program for this morning: you have **1h49m** of videos to watch, before 11:30am Pacific. We have many
   parallel programming frameworks videos: select the tools you are most interested in.

By mid-day you should be familiar with:

- Compute Canada / the Alliance cluster hardware
  - cluster intended purpose and specs
  - filesystems
  - allocation policies
- how to ...
  - ssh into a cluster
  - edit remote files
  - transfer files between your computer and an HPC cluster
  - use software modules
  - compile serial, shared-memory and distributed-memory codes
  - write and use makefiles
  - install Python or R packages/libraries in your own directories on the cluster
- basic parallel programming ideas in OpenMP, MPI, Chapel, Julia (slides only), Python Dask

Some of the hands-on exercises we will do in the mid-day Zoom session:

- Edit a remote file in nano or vi or emacs.
- Try to understand what the default GNU compiler module does: run `module show` on it, print `PATH` variable, locate
  the GNU C compiler.
- Check if your favourite research software is installed on the cluster.
- Write a makefile from scratch.
- Try left+right or upper+lower split panes in tmux on the cluster.
