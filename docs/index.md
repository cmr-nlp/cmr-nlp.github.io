---
layout: default
title: Intro
nav_order: 1
description: "On Continual Model Refinement in Out-of-Distribution Data Streams"
permalink: /
last_modified_date: April 5th 2022
---
 
# CMR | On Continual Model Refinement in Out-of-Distribution Data Streams
{: .fs-7 .fw-700 .text-blue-300 }

---
<span class="fs-2">
[Paper](https://arxiv.org/abs/2205.02014){: target="_blank" .btn .btn-green .mr-1 .fs-3}
[Github](https://github.com/facebookresearch/SemanticDebugger){: target="_blank" .btn .btn-purple .mr-1 .fs-3 }
[Video](https://youtu.be/DhCSL_EkpRc){: target="_blank" .btn .btn-blue .mr-1 .fs-3 }
[Slides](/content/slides.pptx){: target="_blank" .btn .btn-red .mr-1 .fs-3 }
<!-- [Poster](/content/csr_poster.pdf){: target="_blank" .btn .btn-red .mr-1 .fs-3 } -->
</span>


<!--
--- 
<span class="fs-2">
[Data](/data){: .btn .btn-green .mr-1 }
[Methods](/methods){: .btn .btn-purple .mr-1 }
[Metrics](/metrics){: .btn .btn-blue .mr-1 }
[Leaderboard](/leaderboard){: .btn .btn-red .mr-1 }
</span>
-->

---


<!-- ![DrFact](/images/poaster.png){: style="text-align:center; display:block; margin-left: auto; margin-right: auto;" width="100%"} -->

This is the project site for the paper, [_**On Continual Model Refinement in Out-of-Distribution Data Streams**_](https://yuchenlin.xyz/files/cmr.pdf), by [_Bill Yuchen Lin_](https://yuchenlin.xyz/), [Sida Wang](http://www.sidaw.xyz/), [Xi Victoria Lin](http://victorialin.net/), [Robin Jia](https://robinjia.github.io/), [Lin Xiao](https://linxiaolx.github.io/), [Xiang Ren](http://www-bcf.usc.edu/~xiangren/), and [Scott Yih](https://scottyih.org/), published in Proc. of [*ACL 2022*](https://www.2022.aclweb.org/). 
This is a joint work by Facebook AI Research (FAIR) and USC.

---

<!-- 
 <style type="text/css">
    .image-left {
      display: block;
      margin-left: auto;
      margin-right: auto;
      float: right;
    }
 
    table th:first-of-type {
        width: 10
    }
    table th:nth-of-type(2) {
        width: 10
    }
    table th:nth-of-type(3) {
        width: 50
    }
    table th:nth-of-type(4) {
        width: 30
    } 

    </style> -->




![Introduction](images/authors.png){: style="text-align:center; display:block; margin-left: auto; margin-right: auto;" width="100%"}

<!-- {: .fs-3 .fw-300 } -->
### Abstract
Real-world natural language processing (NLP) models need to be continually updated to fix the prediction errors in out-of-distribution (OOD) data streams while overcoming catastrophic forgetting. However, existing continual learning (CL) problem setups cannot cover such a realistic and complex scenario. In response to this, we propose a new CL problem formulation dubbed continual model refinement (CMR). Compared to prior CL settings, CMR is more practical and introduces unique challenges (boundary-agnostic and non-stationary distribution shift, diverse mixtures of multiple OOD data clusters, error-centric streams, etc.). We extend several existing CL approaches to the CMR setting and evaluate them extensively. For benchmarking and analysis, we propose a general sampling algorithm to obtain dynamic OOD data streams with controllable nonstationarity, as well as a suite of metrics measuring various aspects of online performance. Our experiments and detailed analysis reveal the promise and challenges of the CMR problem, supporting that studying CMR in dynamic OOD streams can benefit the longevity of deployed NLP models in production.

---

![Conclusion](images/conclusion.png){: style="text-align:center; display:block; margin-left: auto; margin-right: auto;" width="100%"}

--- 

<iframe width="100%" height="500" src="https://www.youtube.com/embed/DhCSL_EkpRc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

---

```bibtex
@inproceedings{lin-etal-2022-cmr,
    title = "On Continual Model Refinement in Out-of-Distribution Data Streams",
    author = "Lin, Bill Yuchen and Wang, Sida and Lin, Xi Victoria and Jia, Robin and Xiao, Lin and Ren, Xiang and Yih, Wen-tau",
    booktitle = "Proceedings of the 60th Annual Meeting of the Association for Computational Linguistics (ACL 2022)",
    year = "2022"
}
```