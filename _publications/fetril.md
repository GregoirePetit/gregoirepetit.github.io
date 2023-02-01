---
short: 'FeTrIL'
title: 'FeTrIL: Feature Translation for Exemplar-Free Class-Incremental Learning'
collection: projects
permalink: /projects/FeTrIL
thumbnail: /images/FeTrIL_thumbnail.png
date: 04-01-2023
venue: 'Winter Conference on Applications of Computer Vision (WACV)'
authors: '<a href="https://gregoirepetit.github.io">Grégoire Petit</a>, <a href="https://scholar.google.com/citations?user=fjsa2GYAAAAJ">Adrian Popescu</a>, <a href="https://www.wayup.com/profile/Hugo-Schindler-788dbd9307/">Hugo Schindler</a>, <a href="https://davidpicard.github.io">David Picard</a> and <a href="https://scholar.google.fr/citations?user=IZczNpUAAAAJ">Bertrand Delezoide</a> ' 
conference_short: 'WACV 2023'
abstract: "Exemplar-free class-incremental learning is very challenging due to the negative effect of catastrophic forgetting.
A balance between stability and plasticity of the incremental process is needed in order to obtain good accuracy for past as well as new classes. Existing exemplar-free class-incremental methods focus either on successive fine tuning of the model, thus favoring plasticity, or on using a feature extractor fixed after the initial incremental state, thus favoring stability. We introduce a method which combines a fixed feature extractor and a pseudo-features generator to improve the stability-plasticity balance. The generator uses a simple yet effective geometric translation of new class features to create representations of past classes, made of pseudo-features. The translation of features only requires the storage of the centroid representations of past classes to produce their pseudo-features. Actual features of new classes and pseudo-features of past classes are fed into a linear classifier which is trained incrementally to discriminate between all classes.  The incremental process is much faster with the proposed method compared to mainstream ones which update the entire deep model. Experiments are performed with three challenging datasets, and different incremental settings. A comparison with ten existing methods shows that our method outperforms the others in most cases."
bibtex: "@InProceedings{Petit_2023_WACV,
    author    = {Petit, Grégoire and Popescu, Adrian and Schindler, Hugo and Picard, David and Delezoide, Bertrand},
    title     = {FeTrIL: Feature Translation for Exemplar-Free Class-Incremental Learning},
    booktitle = {Proceedings of the IEEE/CVF Winter Conference on Applications of Computer Vision (WACV)},
    month     = {January},
    year      = {2023},
    pages     = {3911-3920}
}"
code: "https://github.com/GregoirePetit/FeTrIL"
pdf: "https://arxiv.org/pdf/2211.13131"
project_page: "https://gregoirepetit.github.io/projects/FeTrIL"
---

