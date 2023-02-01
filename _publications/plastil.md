---
short: 'PlaStIL'
title: 'PlaStIL: Plastic and Stable Memory-Free Class-Incremental Learning'
collection: projects
permalink: /projects/PlaStIL
thumbnail: /images/PlaStIL_thumbnail.png
date: 14-09-2022
venue: 'arXiv preprint'
authors: '<a href="https://gregoirepetit.github.io">Grégoire Petit</a>, <a href="https://scholar.google.com/citations?user=fjsa2GYAAAAJ">Adrian Popescu</a>, <a href="https://scholar.google.com/citations?user=hivcTB0AAAAJ">Eden Belouadah</a>, <a href="https://davidpicard.github.io">David Picard</a> and <a href="https://scholar.google.fr/citations?user=IZczNpUAAAAJ">Bertrand Delezoide</a> ' 
conference_short: ' 2022'
abstract: "Plasticity and stability are needed in class-incremental learning in order to learn from new data while preserving past knowledge. Due to catastrophic forgetting, finding a compromise between these two properties is particularly challenging when no memory buffer is available. Mainstream methods need to store two deep models since they integrate new classes using fine tuning with knowledge distillation from the previous incremental state. We propose a method which has similar number of parameters but distributes them differently in order to find a better balance between plasticity and stability. Following an approach already deployed by transfer-based incremental methods, we freeze the feature extractor after the initial state. Classes in the oldest incremental states are trained with this frozen extractor to ensure stability. Recent classes are predicted using partially fine-tuned models in order to introduce plasticity. Our proposed plasticity layer can be incorporated to any transfer-based method designed for memory-free incremental learning, and we apply it to two such methods. Evaluation is done with three large-scale datasets. Results show that performance gains are obtained in all tested configurations compared to existing methods. "
bibtex: "@article{petit2022plastil, <br>
    Title = {PlaStIL: Plastic and Stable Memory-Free Class-Incremental Learning}, <br>
    Author = {G. Petit, A. Popescu, E. Belouadah, D. Picard, B. Delezoide}, <br>
    Journal = {arXiv preprint}, <br>
    Year = {2022}<br>
    }"
code: "https://github.com/GregoirePetit/PlaStIL"
pdf: "https://arxiv.org/pdf/2209.06606"
project_page: "https://gregoirepetit.github.io/projects/PlaStIL"
paper_url: "https://arxiv.org/abs/2209.06606"
---

