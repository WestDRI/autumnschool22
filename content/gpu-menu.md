+++
title = "Using GPUs with Python"
slug = "gpu-menu"
+++

{{<cor>}}Tuesday, November 22{{</cor>}}\
{{<cgr>}}9:30am–12:30pm Pacific Time{{</cgr>}}

This course will start at 9:30am Pacific Time and will run until 12:30pm Pacific Time.

<!-- Course materials will be added here shortly before the start of the course. -->

There is a single {{<a "https://forms.gle/NZhzRU5o8ti8VhVJ7" "free registration">}} for the entire autumn school.

---

In this workshop, you will get hands-on experience accelerating Python codes with NVIDIA GPUs. We will utilize
code samples in three main categories to introduce you to Python GPU accelerated computing. First, we will
explore drop-in replacements for SciPy and NumPy code through the CuPy library. Next we'll cover NVIDIA
RAPIDS, which provides GPU acceleration for end-to-end data science workloads. Finally we'll cover Numba,
which gives you the flexibility to write custom accelerated code without leaving the Python language. We'll
finish with an end-to-end example that incorporates all the tools introduced to tackle a geospatial
problem. By the end of the workshop, you'll have the skills to start accelerating your own Python codes with
NVIDIA GPUs!

By participating in this workshop, you'll learn how to:

- learn to accelerate existing Python applications on GPU,
- introduce CuPy and RAPIDS for drop-in GPU-accelerated replacements for Numpy and Scikit learn, and
- introduce Numba for writing custom GPU accelerated functions.


**Instructors**: Kris Keipert & Zoe Ryan (NVIDIA)

**Prerequisites:**

- Basic familiarity with Python,
- Familiarity with Numpy, and/or Scikit-learn is beneficial.

**Software**: All attendees will need a remote secure shell (SSH) client installed on their computer in
order to participate in the course exercises. On Windows we recommend
[the free Home Edition of MobaXterm](https://mobaxterm.mobatek.net/download.html). On Mac and Linux
computers SSH is usually pre-installed (try typing `ssh` in a terminal to make sure it is there).

On the remote system we will use Numba, CuPy, and RAPIDS.

Instructions for starting a Python notebook from inside a RAPIDS NGC Apptainer container on Cedar can be
found [here](../gpunotes).
