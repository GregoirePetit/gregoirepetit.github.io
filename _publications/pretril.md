---
short: 'PreTrIL'
title: 'An Analysis of Initial Training Strategies for Exemplar-Free Class-Incremental Learning'
collection: projects
permalink: /projects/PreTrIL
thumbnail: /images/PreTrIL_thumbnail.png
date: 04-01-2024
venue: 'Winter Conference on Applications of Computer Vision (WACV)'
authors: '<a href="https://gregoirepetit.github.io">Grégoire Petit</a>*, <a href="https://msoumm.github.io/">Michael Soumm</a>, <a href="https://evajf.github.io/">Eva Feillet</a>, <a href="https://scholar.google.com/citations?user=fjsa2GYAAAAJ">Adrian Popescu</a>, <a href="https://scholar.google.fr/citations?user=IZczNpUAAAAJ">Bertrand Delezoide</a>, <a href="https://davidpicard.github.io">David Picard</a> and <a href="https://hudelotc.github.io/">Céline Hudelot</a>' 
conference_short: 'WACV 2024'
abstract: "Class-Incremental Learning (CIL) aims to build classification models from data streams. At each step of the CIL process, new classes must be integrated into the model. Due to catastrophic forgetting, CIL is particularly challenging when examples from past classes cannot be stored, the case on which we focus here. To date, most approaches are based exclusively on the target dataset of the CIL process. However, the use of models pre-trained in a self-supervised way on large amounts of data has recently gained momentum. The initial model of the CIL process may only use the first batch of the target dataset, or also use pre-trained weights obtained on an auxiliary dataset. The choice between these two initial learning strategies can significantly influence the performance of the incremental learning model, but has not yet been studied in depth. Performance is also influenced by the choice of the CIL algorithm, the neural architecture, the nature of the target task, the distribution of classes in the stream and the number of examples available for learning. We conduct a comprehensive experimental study to assess the roles of these factors. We present a statistical analysis framework that quantifies the relative contribution of each factor to incremental performance. Our main finding is that the initial training strategy is the dominant factor influencing the average incremental accuracy, but that the choice of CIL algorithm is more important in preventing forgetting. Based on this analysis, we propose practical recommendations for choosing the right initial training strategy for a given incremental learning use case. These recommendations are intended to facilitate the practical deployment of incremental learning."
bibtex: "@article{petit2023analysis, <br>
    title={An Analysis of Initial Training Strategies for Exemplar-Free Class-Incremental Learning}, <br>
    author={Petit, Gr{\'e}goire and Soumm, Michael and Feillet, Eva and Popescu, Adrian and Delezoide, Bertrand and Picard, David and Hudelot, C{\'e}line}, <br>
    journal={arXiv preprint arXiv:2308.11677}, <br>
    year={2023} <br>
}"
pdf: "https://arxiv.org/pdf/2308.11677"
project_page: "https://gregoirepetit.github.io/projects/PreTrIL"
paper_url: "https://arxiv.org/abs/2308.11677"
---
Real-world applications of machine learning (ML) often involve training models from data streams characterized by distributional changes and limited access to past data. This scenario presents a challenge for standard ML algorithms, as they assume that all training data is available at once. Continual learning addresses this challenge by building models designed to incorporate new data while preserving previous knowledge. Class-incremental learning (CIL) is a type of continual learning that handles the case where the data stream is made up of batches of classes. It is particularly challenging in the exemplar-free case (EFCIL), i.e. when storing examples of previous classes is impossible due to memory or confidentiality constraints. CIL algorithms must find a balance between knowledge retention, i.e. stability, and adaptation to new information, i.e. plasticity. Many existing EFCIL methods update the model at each incremental step using supervised fine-tuning combined with a distillation loss, and thus tend to favor plasticity over stability. Another line of work freezes the initial model and only updates the classifier. This approach has recently gained interest due to the availability of models pre-trained on large external datasets, often through self-supervision. While pre-trained models provide diverse and generic features, there are limits to their transferability, and these limits have not been studied in depth in the context of EFCIL. 

We propose a comprehensive analysis framework to disentangle the factors which influence EFCIL performance. Focus is put on the strategies to obtain the initial model of the incremental process. We consider the type of neural architecture, the training method, the depth of fine-tuning, the availability of external data, and the supervision mode for obtaining this initial model. The initial training strategies are compared using three EFCIL algorithms, representative for the state of the art, on 16 target datasets, under 2 challenging CIL scenarios. The main findings are that: (1) pre-training with external data improves accuracy, (2) self-supervision in the initial step boosts incremental learning, particularly when the pre-trained model is fine-tuned on the initial classes, and (3) EFCIL algorithms based on transfer learning have better performance than their fine-tuning-based counterparts. No combination of an EFCIL algorithm and an initial training strategy is best in all cases. Therefore, it is interesting to understand the contribution of the different factors influencing EFCIL performance. The insights brought by the proposed analysis could benefit both continual learning researchers and practitioners. The proposed framework can improve the evaluation and analysis of EFCIL methods. Continual learning practitioners can use the results of this study to better design their incremental learning systems.

The detailled description of the method is available in the [paper](https://arxiv.org/pdf/2308.11677).

If you found this work useful for your research, please cite it as follows:

```BibTeX
@article{petit2023analysis,
  title={An Analysis of Initial Training Strategies for Exemplar-Free Class-Incremental Learning},
  author={Petit, Gr{\'e}goire and Soumm, Michael and Feillet, Eva and Popescu, Adrian and Delezoide, Bertrand and Picard, David and Hudelot, C{\'e}line},
  journal={arXiv preprint arXiv:2308.11677},
  year={2023}
}
```