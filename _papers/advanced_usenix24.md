---
layout: paper
permalink: /papers/usenix24/
title: "Quantifying Privacy Risks of Prompts in Visual Prompt Learning"
authors: 
  - name: "Yixin Wu"
    affiliation: "CISPA Helmholtz Center for Information Security"
  - name: "Rui Wen"
    affiliation: "CISPA Helmholtz Center for Information Security"
  - name: "Michael Backes"
    affiliation: "CISPA Helmholtz Center for Information Security"
  - name: "Pascal Berrang"
    affiliation: "University of Birmingham"
  - name: "Mathias Humbert"
    affiliation: "University of Lausanne"
  - name: "Yun Shen"
    affiliation: "NetApp"
  - name: "Yang Zhang"
    affiliation: "CISPA Helmholtz Center for Information Security"
conference: "USENIX Security Symposium 2024"

content_blocks:
  - title: "Background"
    text: "Prompt learning is an emerging paradigm that enables large-scale pre-trained models to be applied to various downstream tasks. It optimizes tunable parameters, i.e., prompts, while freezing the parameters of the pre-trained models. Then, during inference, these prompts are added to query samples to make predictions."
    image: "/assets/img/publication_preview/usenix24_background.jpeg"
    image_caption: "Overview of visual prompt learning (VPL). We learn an input prompt via back-propagation at the input transformation stage. We apply hard-coded mapping to map the pre-trained model’s outputs into the target labels at the output transformation stage."
  - title: "Overview"
    text: "We perform the first comprehensive privacy assessment of prompts learned by visual prompt learning through the lens of property inference and membership inference attacks. Our empirical evaluation shows that the prompts are vulnerable to both attacks. We also demonstrate that the adversary can mount a successful property inference attack with limited cost. Moreover, we show that membership inference attacks against prompts can be successful with relaxed adversarial assumptions. We further make some initial investigations on the defenses and observe that our method can mitigate the membership inference attacks with a decent utility-defense trade-off but fails to defend against property inference attacks."
    image: "/assets/img/publication_preview/usenix24.jpeg"
    image_caption: "Overview of prompt usage and inference attacks. The prompt is a pixel patch. The prompted image is an original image with an added prompt. Property inference infers sensitive properties of the target prompt's training dataset that the PaaS provider does not intend to disclose. Membership inference infers whether a given sample was in the target prompt's training dataset."
  - title: "Contributions"
    text: |
      This work differs significantly from previous research on privacy risks. While prior studies primarily investigate the privacy risks of machine learning (ML) models, we focus on the privacy risks of prompts at the input level. Both ML models and prompts are essentially sets of parameters; however, prompts contain far fewer parameters than typical models (e.g., < 0.1%). In this manner, the information in the training dataset is heavily compressed during prompt learning.

      This work presents an interesting conclusion: even though prompt learning heavily compresses training dataset information, it remains vulnerable to privacy attacks, leading to the leakage of privacy-sensitive information. Based on this conclusion, there are many potential directions for follow-up work. For example, investigating the privacy leakage of various adaptation paradigms. Given the large scale of modern pre-trained models, we often do not fine-tune the entire model. Instead, we freeze certain layers and optimize only a few. Considering our findings, we hypothesize that even when fine-tuning only a small number of parameters, models may still be vulnerable to privacy attacks. Moreover, we could explore other ML techniques related to compressed training information, such as model distillation, which might also lead to privacy leakage.

      This work also has a real-world impact, particularly in light of existing and emerging privacy regulations such as the GDPR and the EU AI Act. Our findings suggest that tunable prompts could pose unforeseen privacy risks that may need to be addressed under these regulations. As AI legislation continues to evolve, it becomes increasingly important to develop privacy-preserving techniques tailored to prompt learning and other efficient adaptation paradigms.

paper: "https://www.usenix.org/system/files/usenixsecurity24-wu-yixin.pdf"
code: "https://github.com/yxoh/prompt_leak_usenix2024/"
video: "https://www.youtube.com/watch?v=fqCQlK8LPzc&t=261s"
slides: "https://www.usenix.org/system/files/usenixsecurity24_slides-wu-yixin.pdf"
citation: |
  @inproceedings{WWBBHSZ24,
    title={Quantifying Privacy Risks of Prompts in Visual Prompt Learning},
    author={Wu, Yixin and Wen, Rui and Backes, Michael and Berrang, Pascal and Humbert, Mathias and Shen, Yun and Zhang, Yang},
    booktitle={USENIX Security Symposium},
    year={2024}
  }
---

{% include advanced_paper_page.liquid %}