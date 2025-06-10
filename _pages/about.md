---
permalink: /
title: "About me"
excerpt: "Grégoire Petit"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% include base_path %}

My desire to conduct research stems from a deep fascination with the transformative power of Machine Learning and its potential to solve complex, real-world problems. I am particularly drawn to conducting research in the field of medical AI, where the integration of diverse data modalities offers an exciting frontier for innovation.

Education
======
I am a PhD researcher in Machine Learning and Computer Vision. I conducted my research in the [CEA LIST](https://list.cea.fr) of [CEA Tech](https://www.cea-tech.fr) and in the [IMAGINE team](http://imagine.enpc.fr/) of [Ecole des Ponts Paristech](http://www.enpc.fr/) in Paris. My works are focusing on Exemplar-Free Class-Incremental Learning problems, which aims at learning new classes while keeping the knowledge of the previous ones. During my PhD studies, I was supervised by [Dr. Adrian Popescu](https://scholar.google.com/citations?user=fjsa2GYAAAAJ), [Dr. Bertrand Delezoide](https://scholar.google.fr/citations?user=IZczNpUAAAAJ) and [Prof. David Picard](https://davidpicard.github.io).
My thesis was funded by [AI4Media](https://www.ai4media.eu/), a 4-year-long project funded under the European Union’s Horizon 2020 research and innovation programme.

I graduated from [IMT Atlantique](https://www.imt-atlantique.fr/en) with a Master of Engineering in Information Technology (Telecom Bretagne) and from the [Georgia Institute of Technology](https://www.gatech.edu/) with a [Master of Science in Computer Science](https://catalog.gatech.edu/programs/computer-science-ms/), specializing in Machine Learning.

Then, I conducted a postdoc at the [Medical University of Innsbruck](https://www.i-med.ac.at/) in Austria, in the Digital Cardiology group, where I conducted research on the application of Machine Learning to medical imaging. I successfully published my work on [EchoDFKD](https://gregoirepetit.github.io/projects/EchoDFKD) at the [WACV2025 conference](https://wacv2025.thecvf.com/) in Tucson, AZ, USA.

Currently, I am conducting a postdoc at the [LIP6](https://www.lip6.fr/) in Paris, France, in the [LFI team](https://lfi.lip6.fr/) where I am working on the application of Machine Learning and Computer Vision to the analysis of nanoparticle images, in collaboration with the [PHENIX](https://www.phenix.cnrs.fr/) laboratory.

News
======
- 2025: I am conducting a postdoc at the [LIP6](https://www.lip6.fr/) in Paris, France, in the [LFI team](https://lfi.lip6.fr/).
- March 2025: I presented my work on [EchoDFKD](https://gregoirepetit.github.io/projects/EchoDFKD) at the [WACV2025 conference](https://wacv2025.thecvf.com/) in Tucson, AZ, USA.
![EchoDFKD](https://gregoirepetit.github.io/images/EchoDFKD_thumbnail.gif)
- 2024: I am conducting a postdoc at the [Medical University of Innsbruck](https://www.i-med.ac.at/) in Austria, in the Digital Cardiology group.
- January 2024: I presented my work on [PreTrIL](https://gregoirepetit.github.io/projects/PreTrIL) at the [WACV2024 conference](https://wacv2024.thecvf.com/) in Waikoloa, HI, USA.
- I defended my [PhD](https://gregoirepetit.github.io/thesis/).  on the 5th of December 2023!
- August 2023: I presented my work on [PlaStIL](https://gregoirepetit.github.io/projects/PlaStIL) at the [CoLLAs2023](https://lifelong-ml.cc/) conference in Montréal, Canada.
- January 2023: I presented my work on [FeTrIL](https://gregoirepetit.github.io/projects/FeTrIL) at the [WACV2023 conference](https://wacv2023.thecvf.com/) in Waikoloa, HI, USA.
- September 2022: I attended the [AI4Media](https://www.ai4media.eu) colloquium in Thessaloniki, Greece.
- July 2022: I participated in the [VISUM](https://visum.inesctec.pt/) summer school in Porto, Portugal.
- June 2022: I attended the [CVPR2022](https://cvpr2022.thecvf.com/) in New Orleans, LA, USA.

Publications
======
Below are listed my publications, from the latest to the oldest. You can also find my articles on [my Google Scholar profile](https://scholar.google.com/citations?user=oKWj7yQAAAAJ).

{% for post in site.publications reversed %}
  {% include archive-single-short.html %}
{% endfor %}
