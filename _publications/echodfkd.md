---
short: 'EchoDFKD'
title: 'EchoDFKD: Data-Free Knowledge Distillation for Cardiac Ultrasound Segmentation using Synthetic Data'
collection: projects
permalink: /projects/EchoDFKD
thumbnail: /images/EchoDFKD_thumbnail.gif
date: 03-03-2025
venue: 'Winter Conference on Applications of Computer Vision (WACV)'
authors: '<a href="https://gregoirepetit.github.io">Grégoire Petit</a>, Nathan Palluau, <a href=https://scholar.google.fr/citations?user=BY-ZbOsAAAAJ>Axel Bauer</a>, <a href="https://aiscm.i-med.ac.at/members/dlaska-clemens/">Clemens Dlaska</a>'
conference_short: 'WACV 2025'
abstract: "Exemplar-free class-incremental learning is very challenging due to the negative effect of catastrophic forgetting.
 The application of machine learning to medical ultrasound videos of the heart i.e. echocardiography has recently gained traction with the availability of large public datasets. Traditional supervised tasks such as ejection fraction regression are now making way for approaches focusing more on the latent structure of data distributions as well as generative methods. We propose a model trained exclusively by knowledge distillation either on real or synthetical data involving retrieving masks suggested by a teacher model. We achieve state-of-the-art (SOTA) values on the task of identifying end-diastolic and end-systolic frames. By training the model only on synthetic data it reaches segmentation capabilities close to the performance when trained on real data with a significantly reduced number of weights. A comparison with the 5 main existing methods shows that our method outperforms the others in most cases. We also present a new evaluation method that does not require human annotation and instead relies on a large auxiliary model. We show that this method produces scores consistent with those obtained from human annotations. Relying on the integrated knowledge from a vast amount of records this method overcomes certain inherent limitations of human annotator labeling."
bibtex: "@InProceedings{Petit_2025_WACV, <br>
    author    = {Petit, Grégoire and Palluau, Nathan and Bauer, Axel and Dlaska, Clemens}, <br>
    title     = {EchoDFKD: Data-Free Knowledge Distillation for Cardiac Ultrasound Segmentation using Synthetic Data}, <br>
    booktitle = {Proceedings of the IEEE/CVF Winter Conference on Applications of Computer Vision (WACV)}, <br>
    month     = {March}, <br>
    year      = {2025}, <br>
}"
code: "https://github.com/GregoirePetit/EchoDFKD"
pdf: "https://arxiv.org/pdf/2409.07566"
project_page: "https://gregoirepetit.github.io/projects/EchoDFKD"
paper_url: "https://openaccess.thecvf.com/content/WACV2025/papers/Petit_EchoDFKD_Data-Free_Knowledge_Distillation_for_Cardiac_Ultrasound_Segmentation_using_Synthetic_WACV_2025_paper.pdf"
---
In Deep Learning applied to computer vision, one critical task is segmentation, which is essential for accurately interpreting and analyzing visual data. However, segmentation as an annotation task is often resource-intensive and time-consuming, particularly in the medical domain. Knowledge distillation (KD) typically aims to transfer knowledge, such as the ability to segment data, from a large, complex model (often referred to as the teacher model) to a smaller, more efficient model (the student model). This process involves training the student model to replicate the outputs of the teacher model on certain tasks. By doing so, the student model inherits the teacher's capabilities relevant to this task, requiring fewer computational resources. Beyond model compression, KD has demonstrated its versatility in various applications, such as adversarial robustness, ensemble fusion, continual learning, partial or missing labels, multi-task learning, and cross-modal learning.

It often happens that the medical data used to optimize a model is not accessible while the model itself is shared. In particular, regarding computer vision applied to echocardiography, several recent models are shared with the public while the corresponding datasets are not.
It's a safe bet that many laboratories are reluctant even to share their models because of the risk of reconstruction attacks. Knowledge distillation offers protection against attacks on sensitive biometric data that attempt to reconstruct training examples from models, making it a robust solution in medical applications. Owners of a sensitive dataset could, therefore, share only the outputs of their models on several examples or a fusion of outputs from restricted models instead of sharing their model directly. Furthermore, KD is an efficient way of transferring knowledge from one modality to another and thus managing the situation common in medicine, where the different modalities of an example are not always the same from one dataset to another (some datasets might include, for instance, other views or patient metadata). Finally, it is effective for model compression when the student model is lightweight, reducing noise and forcing the student model to focus on the knowledge of interest while removing, for instance, labeler-specific style.

Compared with KD methods based on real data, Data-Free Knowledge Distillation (DFKD) methods enable knowledge to be distilled on a potentially infinite number of artificial examples, making it possible to achieve a near-perfect imitation of the teacher model, at least in the domain well represented by the generative model. In addition, it is possible to focus on a particular section of the possible examples space, e.g., by conditioning on a particular part of a patient's health data (such as age, resting heart rate, etc.), thus generating a very large number of examples under these conditions to ensure efficient distillation of one or more teachers to a specialized student. Moreover, DFKD methods are not necessarily incompatible with KD methods based on real data since synthetic data can be used in addition to real data, in pre-training, in composite batches, or even in the form of data augmentation when examples are created from real examples.

In the present work, we introduce EchoDFKD, the first DFKD model for echocardiography. We use this paradigm by relying on the EchoNet-Synthetic dataset. This dataset was generated following the example of EchoNet-Dynamic, whose test set we use to demonstrate the suitability of our approaches for subsequent tasks on real data.

We first provide the performance of our models using traditional methods based on human labels to provide a fair comparison with models achieving state-of-the-art (SOTA) performance and show that the very lightweight convolutional long short-term memory (ConvLSTM) architecture, as some previous results using this architecture (but with more weights) had suggested, are relevant for  apical-4-chamber echocardiograms. Furthermore, we establish a line on the Pareto (score, weight) frontier, which demonstrates that, although the need to process frames one by one requires relatively large numbers of floating point operations (FLOPs), it is possible to achieve competitive performance levels utilizing a significantly lower number of FLOPs.

To take our model-centric approach to its full extent, we propose removing humans from the process altogether by proposing evaluation methods by other models. This demonstrates that starting from initial models that have been developed involving human knowledge, it is then possible to successfully tackle machine learning tasks by letting these models interact with each other. In the context of unannotated medical data availability, this offers the advantage of enabling rigorous evaluation of masks provided by another agent on this data and fair comparison with other mask proposals. Indeed, while model-based evaluation is highly error-prone, these errors are less likely to be systematic or style-specific. 

The detailled description of the method is available in the [paper](https://openaccess.thecvf.com/content/WACV2025/papers/Petit_EchoDFKD_Data-Free_Knowledge_Distillation_for_Cardiac_Ultrasound_Segmentation_using_Synthetic_WACV_2025_paper.pdf)

The code is available on [Github](https://github.com/GregoirePetit/EchoDFKD)

You can find the poster of the paper [here](https://gregoirepetit.github.io/files/EchoDFKD_poster.pdf), and the presentation video below.

If you found this work useful for your research, please cite it as follows:

```BibTeX
@InProceedings{Petit_2025_WACV,
    author    = {Petit, Gr\'egoire and Palluau, Nathan and Bauer, Axel and Dlaska, Clemens},
    title     = {EchoDFKD: Data-Free Knowledge Distillation for Cardiac Ultrasound Segmentation using Synthetic Data},
    booktitle = {Proceedings of the IEEE/CVF Winter Conference on Applications of Computer Vision (WACV)},
    month     = {March},
    year      = {2025},
}
```