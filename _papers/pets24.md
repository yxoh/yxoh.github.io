---
layout: paper
permalink: /papers/pets24/
title: "Link Stealing Attacks Against Inductive Graph Neural Networks"
teaser: "/assets/img/publication_preview/pets24.jpeg"
teaser_caption: "Overview of the proposed posterior-only attack, combined attack and baselines."
authors: 
  - name: "Yixin Wu"
    affiliation: "CISPA Helmholtz Center for Information Security"
  - name: "Xinlei He"
    affiliation: "CISPA Helmholtz Center for Information Security"
  - name: "Pascal Berrang"
    affiliation: "University of Birmingham"
  - name: "Mathias Humbert"
    affiliation: "University of Lausanne"
  - name: "Michael Backes"
    affiliation: "CISPA Helmholtz Center for Information Security"
  - name: "Neil Zhenqiang Gong"
    affiliation: "Duke University"
  - name: "Yang Zhang"
    affiliation: "CISPA Helmholtz Center for Information Security"
conference: "Privacy Enhancing Technologies Symposium (PETS) 2024"
abstract: "A graph neural network (GNN) is a type of neural network that is specifically designed to process graph-structured data. Typically, GNNs can be implemented in two settings, including the transductive setting and the inductive setting. In the transductive setting, the trained model can only predict the labels of nodes that were observed at the training time. In the inductive setting, the trained model can be generalized to new nodes/graphs. Due to its flexibility, the inductive setting is the most popular GNN setting at the moment. Previous work has shown that transductive GNNs are vulnerable to a series of privacy attacks. However, a comprehensive privacy analysis of inductive GNN models is still missing. This paper fills the gap by conducting a systematic privacy analysis of inductive GNNs through the lens of link stealing attacks, one of the most popular attacks that are specifically designed for GNNs. We propose two types of link stealing attacks, i.e., posterior-only attacks and combined attacks. We define threat models of the posterior-only attacks with respect to node topology and the combined attacks by considering combinations of posteriors, node attributes, and graph features. Extensive evaluation on six real-world datasets demonstrates that inductive GNNs leak rich information that enables link stealing attacks with advantageous properties. Even attacks with no knowledge about graph structures can be effective. We also show that our attacks are robust to different node similarities and different graph features. As a counterpart, we investigate two possible defenses and discover they are ineffective against our attacks, which calls for more effective defenses."
paper: "https://petsymposium.org/popets/2024/popets-2024-0143.pdf"
code: "https://github.com/yxoh/link_steal_pets2024"
slides: "/assets/pdf/pets2024.pdf"
citation: |
  @inproceedings{WHBHBGZ24,
    title={Link Stealing Attacks Against Inductive Graph Neural Networks},
    author={Wu, Yixin and He, Xinlei and Berrang, Pascal and Humbert, Mathias and Backes, Michael and Gong, Neil Zhenqiang and Zhang, Yang},
    booktitle={Privacy Enhancing Technologies Symposium},
    year={2024}
  }
---

{% include paper_page.liquid %}