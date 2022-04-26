---
layout: default
title: Evaluation
nav_order: 4
# toc_list: true
last_modified_date: April 5th 2022
permalink: /evaluation
mathjax: true
has_toc: true
---

# Evaluation Protocol & Analysis
{: .no_toc}




## Table of contents
{: .no_toc .text-delta }

- TOC
{:toc}


## Experiments 

There are multiple scripts for running experiments with different CMR methods in `experiments/run_scripts`. 
We leave their documentation on our project website.
Here we take the `run_simplecl.sh` and `slurm_simple.sh` as examples for running the Continual-Finetuning baseline method shown in our paper. For running other CMR methods, the filename should be self-explanatory and we will show the detailed instructions on our website.

For running a particular setup of CMR experiments, 
we can execute the below command:
```bash
bash experiments/run_scripts/run_simplecl.sh ${seed} ${lr} ${ep} ${l2w} ${ns_config} ${task} val/test ${stream_id}
```

### Wrapper

Here, the arguments, such as `seed`, `lr`, are usually specified in a wrapper script, which in this example is the `slurm_simple.sh`.
The wrapper script has two major modes: validation (`val`) and testing (`test`). 
The validation mode is to explore the best hps and the testing mode is to evaluate the final hps of a CMR method with multiple rounds of experiments (via setting different seeds and using different streams).

### Job scheduling 
Note that we include a slurm-related command for those who use [slurm] for scheduling jobs on their servers. If you don't use slurm, you could remove the following part (i.e., `tmux ...`) or replace it with your own job-scheduling method for running the job `[xxx]`:

`tmux new-session -d -s ${session_name} "srun --job-name ${session_name} --gpus-per-node=1 --partition=devlab --time=120 --cpus-per-task 4 --pty [xxx]"`




 

### None Refinement (reference)
TODO: introduce `experiments/run_scripts/run_nonecl.sh`.

This is a reference method that does nothing for CMR.


### Offline Refinement (reference)

TODO: introduce `experiments/run_scripts/run_offline.sh`
This is a reference method that refine the model by using the overall error data to fine-tune the baseline method offline, i.e., not an online learning method.
