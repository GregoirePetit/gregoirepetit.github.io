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

I am currently looking for a good lab to conduct a Postdoc in Continual Learning/Computer Vision. Let's design that Postdoc together!

Education
======
I am a PhD researcher in Machine Learning and Computer Vision. I conducted my research in the [CEA LIST](https://list.cea.fr) of [CEA Tech](https://www.cea-tech.fr) and in the [IMAGINE team](http://imagine.enpc.fr/) of [Ecole des Ponts Paristech](http://www.enpc.fr/) in Paris. My works are focusing on Exemplar-Free Class-Incremental Learning problems, which aims at learning new classes while keeping the knowledge of the previous ones. During my PhD studies, I was supervised by [Dr. Adrian Popescu](https://scholar.google.com/citations?user=fjsa2GYAAAAJ), [Dr. Bertrand Delezoide](https://scholar.google.fr/citations?user=IZczNpUAAAAJ) and [Prof. David Picard](https://davidpicard.github.io).
My thesis was funded by [AI4Media](https://www.ai4media.eu/), a 4-year-long project funded under the European Union’s Horizon 2020 research and innovation programme.

I graduated from [IMT Atlantique](https://www.imt-atlantique.fr/en) with a Master of Engineering in Information Technology (Telecom Bretagne) and from the [Georgia Institute of Technology](https://www.gatech.edu/) with a [Master of Science in Computer Science](https://catalog.gatech.edu/programs/computer-science-ms/), specializing in Machine Learning.

News
======
- January 2024: I will present my work on [PreTrIL](https://gregoirepetit.github.io/projects/PreTrIL) at the [WACV2024 conference](https://wacv2024.thecvf.com/) in Waikoloa, HI, USA.
- I defend my PhD on the 5th of December 2023!
- August 2023: I presented my work on [PlaStIL](https://gregoirepetit.github.io/projects/PlaStIL) at the [CoLLAs2023](https://lifelong-ml.cc/) conference in Montréal, Canada.
- January 2023: I presented my work on [FeTrIL](https://gregoirepetit.github.io/projects/FeTrIL) at the [WACV2023 conference](https://wacv2023.thecvf.com/) in Waikoloa, HI, USA.
- September 2022: I attended the [AI4Media](https://www.ai4media.eu) colloquium in Thessaloniki, Greece.
- July 2022: I participated in the [VISUM](https://visum.inesctec.pt/) summer school in Porto, Portugal.
- June 2022: I attended the [CVPR2022](https://cvpr2022.thecvf.com/) in New Orleans, LA, USA.

Publications
======
Below are listed my publications, from the latest to the oldest. You can also find my articles on [my Google Scholar profile](https://scholar.google.com/citations?user=oKWj7yQAAAAJ).

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
