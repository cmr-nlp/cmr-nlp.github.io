---
layout: default
title: CMR Methods
nav_order: 3
has_children: false
has_toc: false
permalink: /methods
---

# Methods for CMR
{: .no_toc}



## Table of contents
{: .no_toc .text-delta }

- TOC
{:toc}


---

![cmr_method](images/cmr_method.png){: style="text-align:center; display:block; margin-left: auto; margin-right: auto;" width="100%"}

## Base Language Models

## The overall pipeline 

TODO: introduce the `OnlineDebuggingMethod` class in ``cmr/debug_algs/commons.py`.
TODO: introduce how to run the experiments via `cmr/debug_algs/run_lifelong_finetune.py`.

## Continual Fine-Tuning 

TODO: introduce the `ContinualFinetuning` class in `cmr/debug_algs/cl_simple_alg.py`.

## Regularization Methods 

### Online L2Reg
TODO: introduce how and where to check the L2reg computation in CF.
### Online EWC
TODO: introduce `OnlineEWC` class in `cmr/debug_algs/cl_online_ewc_alg.py`


## Replay Methods 

TODO: introduce the unified `MemoryBasedCL` class in `cmr/debug_algs/cl_mbcl_alg.py`.

### Experience Replay (ER)
TODO: 


### Conditional Replay (MIR & MaxLoss)
TODO: 
