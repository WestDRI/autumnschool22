+++
title = "Notes for the GPU session"
slug = "gpunotes"
+++

We will use a Python notebook from inside a RAPIDS NGC Apptainer container. Building this container from
scratch takes anywhere from 40 mins (in `/localscratch`) to several hours (in `/scratch`). Today we will skip
this part, as we have already built this container for you -- you can find it at
`/scratch/razoumov/rapids.sif` on Cedar.

<!-- In my test it took 4h38m in `/scratch` and 42m in `/localscratch.` -->

> **Note**: Just for your information, here is how we recommend to build this container in `/localscratch`
> in the future:
> 1. Log in to Cedar cluster and `cd ~/scratch`
> 2. Create a job submission script `distributed.sh` filling in your Slurm allocation in the blank field:
> ```sh
> #!/bin/bash
> #SBATCH --time=0:90:0
> #SBATCH --mem-per-cpu=7200
> #SBATCH --account=...
> WORKDIR=$(pwd)
> cd $SLURM_TMPDIR
> module load apptainer
> export APPTAINER_TMPDIR=$SLURM_TMPDIR   # otherwise temporary files will go into /scratch/$USER (slower)
> apptainer build rapids.sif docker://nvcr.io/nvidia/rapidsai/rapidsai:cuda11.5-runtime-centos7-py3.9
> /bin/mv -f rapids.sif $WORKDIR
> ```
> 3. Submit this job with `sbatch distributed.sh` and wait for it to finish.

<!-- chmod og+X /scratch/razoumov -->
<!-- chmod og+r /scratch/razoumov/{rapids.sif,notebook-*.ipynb} -->

Today, we will be using this image. Log in to *cedar.computecanada.ca* with your guest account and copy the
container and the notebooks into your `/scratch` directory. Next, start an interactive GPU job:

```sh
cd ~/scratch
cp /scratch/razoumov/rapids.sif .
cp /scratch/razoumov/notebook-1-cupy-intro.ipynb .
cp /scratch/razoumov/notebook-2-rapids-intro.ipynb .
cp /scratch/razoumov/notebook-3-numba-intro.ipynb .
module load apptainer
salloc --time=3:00:0 --mem-per-cpu=3600  --gpus-per-node=1 --account=def-training-wa_gpu --reservation=westdri-wr_gpu
```

Wait for the job to get started, and then -- inside the job -- start a shell inside the container. Please pay
attention to the change in the prompt in the lines below, i.e. don't blankly copy the prompt into your command
line:

```sh
apptainer shell --nv -B /home -B /project -B /scratch rapids.sif

Apptainer> source /opt/conda/etc/profile.d/conda.sh
Apptainer> conda activate rapids

(rapids) Apptainer> jupyter-lab --ip $(hostname -f) --no-browser
```

When the JupyterLab server starts, it will produce something like:

```txt
To access the server, open this file in a browser:
    file:///home/.../.local/share/jupyter/runtime/jpserver-...-open.html
Or copy and paste one of these URLs:
    http://node_name.int.cedar.computecanada.ca:8888/lab?token=896fb...c28e1
 or http://127.0.0.1:8888/lab?token=896fb...c28e1
```

Take note of (1) the node name, (2) the token and possibly (3) the port if it is different from 8888.

On your computer, open a new local terminal, whether in Mac or Linux or inside MobaXTerm in Windows. In that
window, paste the following command, substituting {{< colour "#714285" "username" >}}&nbsp; by your username,
{{< colour "#714285" "node_name" >}}&nbsp; by its corresponding value, and the remote 
{{< colour "#714285" "port" >}}&nbsp; (the second `8888`) by the actual port (if different from `8888`)
-- this will start SSH port
forwarding from the local port 8888 to the remote port 8888 on the compute node:

```sh
ssh username@cedar.computecanada.ca -L 8888:node_name.int.cedar.computecanada.ca:8888
```

Finally, in the browser on your computer, go to http://localhost:8888/?token=896fb...c28e1, pasting in the
full {{< colour "#714285" "token" >}}. This will start JupyterLab. Inside it, start a Python 3 notebook.

More details in our documentation:

- {{<a "https://docs.alliancecan.ca/wiki/RAPIDS#Working_on_clusters_with_a_Singularity_image" "Starting RAPIDS with a Singularity image">}}
- {{<a "https://docs.alliancecan.ca/wiki/Advanced_Jupyter_configuration#Connecting_to_JupyterLab" "Connecting to JupyterLab">}}








<!-- ```sh -->
<!-- sshuttle -dns -Nr $USERNAME@cedar.computecanada.ca -->
<!-- ``` -->

<!-- or -->

<!-- ssh <username>@cedar.computecanada.ca -L 8888:<node>:8888 -->

<!-- Copy the Jupyter URL into your web browser. -->

<!-- http://localhost:8888/lab?token=38d90a7494bb4c9cd358bd7ee46a45e72591605d61551858 -->
