+++
title = "HPC closing session"
slug = "hpc4"
+++

1. Are there any questions on the materials you just watched?
1. Let's go together through the challenges, do some exercises, and debug problems.

Click on a triangle to expand a question:

{{< question num=17 >}}
Submit a serial job that runs `hostname` command.

Try playing with `sq`, `squeue`, `scancel` commands.
{{< /question >}}

{{< question num=18 >}}
Submit a serial job based on `pi.c`.

Try `sstat` on a currently running job. Try `seff` and `sacct` on a completed job.
{{< /question >}}

{{< question num=19 >}}
Using a serial job, time optimized (`-O2`) vs. unoptimized code. Type your findings into the chat.
{{< /question >}}

{{< question num=20 >}}
Using a serial job, time `pi.c` vs. `pi.py` for the same number of terms (cannot be too large or too small -- why?).

Python pros -- can you speed up `pi.py`?
{{< /question >}}

{{< question num=21 >}}
Submit an array job for different values of `n` (number of terms) with `pi.c`. How can you have different executable for
each job inside the array?
{{< /question >}}

{{< question num=22 >}}
Submit a shared-memory job based on `sharedPi.c`. Did you get any speedup? Type your answer into the chat.
{{< /question >}}

{{< question num=23 >}}
Submit an MPI job based on `distributedPi.c`.

Try scaling 1 → 2 → 4 → 8 cores. Did you get any speedup? Type your answer into the chat.
{{< /question >}}

{{< question num=24 >}}
Test the serial code inside an interactive job. Please quit the job when done, as we have very few compute cores on the
training cluster.

Note: we have seen the training cluster become unstable when using too many interactive resources. Strictly speaking,
this should not happen, however there is a small chance it might. We do have a backup.
{{< /question >}}

{{< question num=25 >}}
Test the shared-memory code inside an interactive job. Please quit when done, as we have very few compute cores on the training cluster.
{{< /question >}}

{{< question num=26 >}}
Test the MPI code inside an interactive job. Please quit when done, as we have very few compute cores on the training cluster.
{{< /question >}}

{{< question num=27 >}}
Share a file in your `~/projects` directory (make it readable) with all other users in `def-sponsor00` group.
{{< /question >}}

{{< question num=28 >}}
Are there questions on any of the topics that we covered today? You can type your question into the chat, ask via audio
(unmute), or raise your hand in Zoom.
{{< /question >}}
