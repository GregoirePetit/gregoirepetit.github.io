---
short: 'FeTrIL'
title: 'FeTrIL: Feature Translation for Exemplar-Free Class-Incremental Learning'
collection: projects
permalink: /projects/FeTrIL
thumbnail: /images/FeTrIL_thumbnail.png
date: 04-01-2023
venue: 'Winter Conference on Applications of Computer Vision (WACV)'
authors: '<a href="https://gregoirepetit.github.io">Grégoire Petit</a>*, <a href="https://scholar.google.com/citations?user=fjsa2GYAAAAJ">Adrian Popescu</a>, <a href="https://www.wayup.com/profile/Hugo-Schindler-788dbd9307/">Hugo Schindler</a>, <a href="https://davidpicard.github.io">David Picard</a> and <a href="https://scholar.google.fr/citations?user=IZczNpUAAAAJ">Bertrand Delezoide</a> ' 
conference_short: 'WACV 2023'
abstract: "Exemplar-free class-incremental learning is very challenging due to the negative effect of catastrophic forgetting.
A balance between stability and plasticity of the incremental process is needed in order to obtain good accuracy for past as well as new classes. Existing exemplar-free class-incremental methods focus either on successive fine tuning of the model, thus favoring plasticity, or on using a feature extractor fixed after the initial incremental state, thus favoring stability. We introduce a method which combines a fixed feature extractor and a pseudo-features generator to improve the stability-plasticity balance. The generator uses a simple yet effective geometric translation of new class features to create representations of past classes, made of pseudo-features. The translation of features only requires the storage of the centroid representations of past classes to produce their pseudo-features. Actual features of new classes and pseudo-features of past classes are fed into a linear classifier which is trained incrementally to discriminate between all classes.  The incremental process is much faster with the proposed method compared to mainstream ones which update the entire deep model. Experiments are performed with three challenging datasets, and different incremental settings. A comparison with ten existing methods shows that our method outperforms the others in most cases."
bibtex: "@InProceedings{Petit_2023_WACV, <br>
    author    = {Petit, Grégoire and Popescu, Adrian and Schindler, Hugo and Picard, David and Delezoide, Bertrand}, <br>
    title     = {FeTrIL: Feature Translation for Exemplar-Free Class-Incremental Learning}, <br>
    booktitle = {Proceedings of the IEEE/CVF Winter Conference on Applications of Computer Vision (WACV)}, <br>
    month     = {January}, <br>
    year      = {2023}, <br>
    pages     = {3911-3920} <br>
}"
code: "https://github.com/GregoirePetit/FeTrIL"
pdf: "https://arxiv.org/pdf/2211.13131"
project_page: "https://gregoirepetit.github.io/projects/FeTrIL"
paper_url: "https://openaccess.thecvf.com/content/WACV2023/html/Petit_FeTrIL_Feature_Translation_for_Exemplar-Free_Class-Incremental_Learning_WACV_2023_paper.html"
---

Deep learning has dramatically improved the quality of automatic visual recognition, both in terms of accuracy and scale. Current models discriminate between thousands of classes with an accuracy often close to that of human recognition, assuming that sufficient training examples are provided. Unlike humans, algorithms reach optimal performance only if trained with all data at once whenever new classes are learned. This is an important limitation because data often occur in sequences and their storage is costly. Also, iterative retraining to integrate new data is computationally costly and difficult in time- or computation-constrained applications Incremental learning was introduced to reduce the memory and computational costs of machine learning algorithms. The main problem faced by class-incremental learning (CIL) methods is catastrophic forgetting, the tendency of neural nets to underfit past classes when ingesting new data. Many recent solutions, based on deep nets, use replay from a bounded memory of the past to reduce forgetting. However, replay-based methods make a strong assumption because past data are often unavailable. Also, the footprint of the image memory can be problematic for memory-constrained devices. Exemplar-free class-incremental learning (EFCIL) methods recently gained momentum. Most of them use distillation to preserve past knowledge, and generally favor plasticity. New classes are well predicted since models are learned with all new data and only a representation of past data. A few EFCIL methods are inspired by transfer learning. They learn a feature extractor in the initial state, and use it as such later to train new classifiers. In this case, stability is favored over plasticity since the model is frozen.

We introduce FeTrIL, a new EFCIL method which combines a frozen feature extractor and a pseudo-feature generator to improve incremental performance. New classes are represented by their image features obtained from the feature extractor. Past classes are represented by pseudo-features which are derived from features of new classes by using a geometric translation process. This translation moves features toward a region of the features space which is relevant for past classes. The proposed pseudo-feature generation is adapted for EFCIL since it is simple, fast and only requires the storage of the centroids for past classes. We run experiments with a standard EFCIL setting, which consists of a larger initial state, followed by smaller states which include the same number of classes. Results show that the proposed approach has better behavior compared to ten existing methods, including very recent ones.

The detailled description of the method is available in the [paper](https://openaccess.thecvf.com/content/WACV2023/html/Petit_FeTrIL_Feature_Translation_for_Exemplar-Free_Class-Incremental_Learning_WACV_2023_paper.html)

The code is available on [Github](https://github.com/GregoirePetit/FeTrIL)

You can find the poster of the paper [here](https://gregoirepetit.github.io/files/FeTrIL_poster.pdf), and the presentation video below.

[![FeTrIL presentation](https://img.youtube.com/vi/sI-4a1BBoW8/0.jpg)](https://youtu.be/sI-4a1BBoW8 "Presentation of FeTrIL")

If you found this work useful for your research, please cite it as follows:

```BibTeX
@InProceedings{Petit_2023_WACV,
    author    = {Petit, Gr\'egoire and Popescu, Adrian and Schindler, Hugo and Picard, David and Delezoide, Bertrand},
    title     = {FeTrIL: Feature Translation for Exemplar-Free Class-Incremental Learning},
    booktitle = {Proceedings of the IEEE/CVF Winter Conference on Applications of Computer Vision (WACV)},
    month     = {January},
    year      = {2023},
    pages     = {3911-3920}
}
```