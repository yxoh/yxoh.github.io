---
layout: paper
permalink: /papers/usenix24_old/
title: "Quantifying Privacy Risks of Prompts in Visual Prompt Learning"
teaser: "/assets/img/publication_preview/usenix24.jpeg"  # 添加图片路径
teaser_caption: "Overview of prompt usage and inference attacks. The prompt is a pixel patch. The prompted image is an original image with an added prompt. Property inference infers sensitive properties of the target prompt's training dataset that the PaaS provider does not intend to disclose. Membership inference infers whether a given sample was in the target prompt's training dataset."
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
abstract: "Large-scale pre-trained models are increasingly adapted to downstream tasks through a new paradigm called prompt learning. In contrast to fine-tuning, prompt learning does not update the pre-trained model's parameters. Instead, it only learns an input perturbation, namely prompt, to be added to the downstream task data for predictions. Given the fast development of prompt learning, a well-generalized prompt inevitably becomes a valuable asset as significant effort and proprietary data are used to create it. This naturally raises the question of whether a prompt may leak the proprietary information of its training data. In this paper, we perform the first comprehensive privacy assessment of prompts learned by visual prompt learning through the lens of property inference and membership inference attacks. Our empirical evaluation shows that the prompts are vulnerable to both attacks. We also demonstrate that the adversary can mount a successful property inference attack with limited cost. Moreover, we show that membership inference attacks against prompts can be successful with relaxed adversarial assumptions. We further make some initial investigations on the defenses and observe that our method can mitigate the membership inference attacks with a decent utility-defense trade-off but fails to defend against property inference attacks. We hope our results can shed light on the privacy risks of the popular prompt learning paradigm. To facilitate the research in this direction, we will share our code and models with the community."
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

{% include paper_page.liquid %}