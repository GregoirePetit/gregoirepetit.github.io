---
short: 'AdvisIL'
title: 'AdvisIL: A Class-Incremental Learning Advisor'
collection: projects
permalink: /projects/AdvisIL
thumbnail: /images/advisIL_thumbnail.png
date: 03-01-2023
venue: 'Winter Conference on Applications of Computer Vision (WACV)'
authors: '<a href="https://evajf.github.io/">Eva Feillet</a>, <a href="https://gregoirepetit.github.io">Grégoire Petit</a>, <a href="https://scholar.google.com/citations?user=fjsa2GYAAAAJ">Adrian Popescu</a>, Marina Reyboz and <a href="https://hudelotc.github.io/">Céline Hudelot</a> ' 
conference_short: 'WACV 2023'
abstract: "Recent class-incremental learning methods combine deep neural architectures and learning algorithms to handle streaming data under memory and computational constraints. The performance of existing methods varies depending on the characteristics of the incremental process. To date, there is no other approach than to test all pairs of learning algorithms and neural architectures on the training data available at the start of the learning process to select a suited algorithm-architecture combination. To tackle this problem, in this article, we introduce AdvisIL, a method which takes as input the main characteristics of the incremental process (memory budget for the deep model, initial number of classes, size of incremental steps) and recommends an adapted pair of learning algorithm and neural architecture. The recommendation is based on a similarity between the user-provided settings and a large set of pre-computed experiments. AdvisIL makes class-incremental learning easier, since users do not need to run cumbersome experiments to design their system. We evaluate our method on four datasets under six incremental settings and three deep model sizes. We compare six algorithms and three deep neural architectures. Results show that AdvisIL has better overall performance than any of the individual combinations of a learning algorithm and a neural architecture. AdvisIL's code is available at https://github.com/EvaJF/AdvisIL."
bibtex: "@InProceedings{Feillet_2023_WACV, <br>
    author    = {Feillet, Eva and Petit, Grégoire and Popescu, Adrian and Reyboz, Marina and Hudelot, Céline}, <br>
    title     = {AdvisIL - A Class-Incremental Learning Advisor}, <br>
    booktitle = {Proceedings of the IEEE/CVF Winter Conference on Applications of Computer Vision (WACV)}, <br>
    month     = {January}, <br>
    year      = {2023}, <br>
    pages     = {2400-2409} <br>
}"
code: "https://github.com/EvaJF/AdvisIL"
pdf: "https://openaccess.thecvf.com/content/WACV2023/papers/Feillet_AdvisIL_-_A_Class-Incremental_Learning_Advisor_WACV_2023_paper.pdf"
project_page: "https://gregoirepetit.github.io/projects/AdvisIL"
paper_url: "https://openaccess.thecvf.com/content/WACV2023/html/Feillet_AdvisIL_-_A_Class-Incremental_Learning_Advisor_WACV_2023_paper.html"
---

