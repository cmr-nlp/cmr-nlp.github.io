---
layout: default
title: Benchmark Data
nav_order: 2
# toc_list: true
last_modified_date: April 5th 2022
permalink: /data
has_toc: true
---

# The Benchmark Data for CMR 
{: .no_toc}



## Table of contents
{: .no_toc .text-delta }

- TOC
{:toc}


---

![cmr_formulation](images/cmr_formulation.png){: style="text-align:center; display:block; margin-left: auto; margin-right: auto;" width="100%"}

---

## Download and Preprocess 

Here we use the MRQA datasets as an example to show how datasets should be processed.

1. download the data files 
```bash
cd data/mrqa/
bash download.sh
```

2. preprocess the datasets
```bash
cd ~/CMR/ # go to the root folder of CMR project, say ~/CMR/
python data/data_formatter.py
```

After thest two steps, you should see a few `mrqa_*` folders under the `data` folder, where each is for a particular data cluster.


## Generating OOD data streams

### Generate upstream model predictions.

We first use the upstream model to infer examples from other data clusters.

```bash
mkdir -p upstream_resources/qa_upstream_preds/tmp/ # under the CMR folder
bash scripts/run_mrqa_infer.sh
```

The first part of this script is to test the upstream model on the upstream training data, and the second part is to test the upstream model on other data clusters' dev data. 

### Sample data streams.

Now we generate the data streams and evaluation sets that we need for our experiments. The default configurations that are used here can be found in the code file. 

```bash
mkdir -p experiments/eval_data/qa/
python cmr/benchmark_gen/sample_submission_streams.py --task_name QA
```

The generated data streams can be visualized by running `cmr/benchmark_gen/visualize_streams.py`.



## More configurations for generating OOD data streams

![ood_data](images/ood_data.png){: style="text-align:center; display:block; margin-left: auto; margin-right: auto;" width="100%"}


TODO: here, we will introduce the details for using the `sample_submission_streams.py` for generating the OOD data streams as described in the above picture.