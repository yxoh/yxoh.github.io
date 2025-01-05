---
layout: paper
permalink: /papers/arxiv22a/
title: "Membership Inference Attacks Against Text-to-image Generation Models"
teaser: "/assets/img/publication_preview/arxiv22a.jpeg"
teaser_caption: "Overview of our attack pipeline."
authors: 
    - name: "Yixin Wu"
      affiliation: "CISPA Helmholtz Center for Information Security"
    - name: "Ning Yu"
      affiliation: "Salesforce Research"
    - name: "Zheng Li"
      affiliation: "CISPA Helmholtz Center for Information Security"
    - name: "Michael Backes"
      affiliation: "CISPA Helmholtz Center for Information Security"
    - name: "Yang Zhang"
      affiliation: "CISPA Helmholtz Center for Information Security"    
conference: "arXiv"
abstract: "Text-to-image generation models have recently attracted unprecedented attention as they unlatch imaginative applications in all areas of life. However, developing such models requires huge amounts of data that might contain privacy-sensitive information, e.g., face identity. While privacy risks have been extensively demonstrated in the image classification and GAN generation domains, privacy risks in the text-to-image generation domain are largely unexplored. In this paper, we perform the first privacy analysis of text-to-image generation models through the lens of membership inference. Specifically, we propose three key intuitions about membership information and design four attack methodologies accordingly. We conduct comprehensive evaluations on two mainstream text-to-image generation models including sequence-to-sequence modeling and diffusion-based modeling. The empirical results show that all of the proposed attacks can achieve significant performance, in some cases even close to an accuracy of 1, and thus the corresponding risk is much more severe than that shown by existing membership inference attacks. We further conduct an extensive ablation study to analyze the factors that may affect the attack performance, which can guide developers and researchers to be alert to vulnerabilities in text-to-image generation models. All these findings indicate that our proposed attacks pose a realistic privacy threat to the text-to-image generation models."
paper: "https://arxiv.org/pdf/2210.00968.pdf"
code: "."
citation: |
  @article{WYLBZ22,
    title={Membership Inference Attacks Against Text-to-image Generation Models},
    author={Yixin Wu and Ning Yu and Zheng Li and Michael Backes and Yang Zhang},
    journal={arXiv},
    year={2022}
  }
---

{% include paper_page.liquid %}