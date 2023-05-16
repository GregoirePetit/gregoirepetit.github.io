---
short: 'PlaStIL'
title: 'PlaStIL: Plastic and Stable Memory-Free Class-Incremental Learning'
collection: projects
permalink: /projects/PlaStIL
thumbnail: /images/PlaStIL_thumbnail.png
date: 22-08-2023
venue: 'Second Conference on Lifelong Learning Agents'
authors: '<a href="https://gregoirepetit.github.io">Grégoire Petit</a>*, <a href="https://scholar.google.com/citations?user=fjsa2GYAAAAJ">Adrian Popescu</a>, <a href="https://scholar.google.com/citations?user=hivcTB0AAAAJ">Eden Belouadah</a>, <a href="https://davidpicard.github.io">David Picard</a> and <a href="https://scholar.google.fr/citations?user=IZczNpUAAAAJ">Bertrand Delezoide</a> ' 
conference_short: 'CoLLAs 2023'
abstract: "Plasticity and stability are needed in class-incremental learning in order to learn from new data while preserving past knowledge. Due to catastrophic forgetting, finding a compromise between these two properties is particularly challenging when no memory buffer is available. Mainstream methods need to store two deep models since they integrate new classes using fine tuning with knowledge distillation from the previous incremental state. We propose a method which has similar number of parameters but distributes them differently in order to find a better balance between plasticity and stability. Following an approach already deployed by transfer-based incremental methods, we freeze the feature extractor after the initial state. Classes in the oldest incremental states are trained with this frozen extractor to ensure stability. Recent classes are predicted using partially fine-tuned models in order to introduce plasticity. Our proposed plasticity layer can be incorporated to any transfer-based method designed for memory-free incremental learning, and we apply it to two such methods. Evaluation is done with three large-scale datasets. Results show that performance gains are obtained in all tested configurations compared to existing methods. "
bibtex: "@article{petit2023plastil, <br>
    Title = {PlaStIL: Plastic and Stable Memory-Free Class-Incremental Learning}, <br>
    Author = {G. Petit, A. Popescu, E. Belouadah, D. Picard, B. Delezoide}, <br>
    Journal = {Second Conference on Lifelong Learning Agents}, <br>
    Year = {2022}<br>
    }"
code: "https://github.com/GregoirePetit/PlaStIL"
pdf: "https://arxiv.org/pdf/2209.06606"
project_page: "https://gregoirepetit.github.io/projects/PlaStIL"
paper_url: "https://arxiv.org/abs/2209.06606"
---

Class-incremental learning (CIL) enables the adaptation of artificial agents to dynamic environments in which data occur sequentially.
CIL is particularly useful when the training process is performed under memory and/or computational constraints. However, it is really susceptible to catastrophic forgetting, which refers to the tendency to forget past information when learning new data. Most recent CIL methods use fine-tuning with knowledge distillation from the previous model to preserve past information.
Knowledge distillation has been progressively refined to improve CIL performance.
An alternative approach to CIL is inspired by transfer learning. These methods use a feature extractor which is frozen after the initial CIL state. They become competitive in exemplar-free CIL, a difficult setting due to a strong effect of catastrophic forgetting.
The main challenge is to find a good plasticity-stability balance because fine-tuning methods favor plasticity, while transfer-based methods only address stability.

In this work, we tackle exemplar-free CIL (EFCIL) by combining the two types of approaches described above.
Building on the strong performance of transfer-based methods, we introduce a plasticity component by partially fine-tuning models for recent classes.

![PlaStIL comparisons](https://github.com/GregoirePetit/gregoirepetit.github.io/blob/main/images/plastil_graphs.png)

The results from the figure show that PlaStIL gives a better global accuracy compared to [DeeSIL](https://arxiv.org/abs/1808.06396) and [LUCIR](https://openaccess.thecvf.com/content_CVPR_2019/html/Hou_Learning_a_Unified_Classifier_Incrementally_via_Rebalancing_CVPR_2019_paper.html), two representative methods focused on stability and plasticity, respectively.
Accuracy is presented separately for past and new classes for existing methods to examine the plasticity-stability balance offered by each method.
[LUCIR](https://openaccess.thecvf.com/content_CVPR_2019/html/Hou_Learning_a_Unified_Classifier_Incrementally_via_Rebalancing_CVPR_2019_paper.html) has optimal plasticity (best accuracy of new classes), while [DeeSIL](https://arxiv.org/abs/1808.06396) has optimal stability (best accuracy for past classes).
However, the performance of both methods is strongly degraded on the complementary dimensions.
PlaStIL is close to [LUCIR](https://openaccess.thecvf.com/content_CVPR_2019/html/Hou_Learning_a_Unified_Classifier_Incrementally_via_Rebalancing_CVPR_2019_paper.html) in terms of plasticity and to [DeeSIL](https://arxiv.org/abs/1808.06396) in terms of stability.
Consequently, it ensures a better balance between these two properties of EFCIL.

PlaStIL is inspired by transfer learning but adds a partial fine-tuning component to boost plasticity.
It is applicable to any transfer-based method and we exemplify it with [DeepSLDA](https://github.com/tyler-hayes/Deep_SLDA) and [DeeSIL](https://arxiv.org/abs/1808.06396).
We introduce a hybrid classification layer which combines classification weights learned with the initial model for past classes and with the fine-tuned models for recent classes.
We evaluate the proposed approach on three datasets which contain 1000 classes each.
The number of incremental states is varied to assess the robustness of the tested methods.
Results show that performance gains are obtained by adding the proposed plasticity component to transfer-based methods.
Equally interesting, important performance improvements are obtained over distillation-based methods, which are the mainstream methods deployed to tackle CIL.

