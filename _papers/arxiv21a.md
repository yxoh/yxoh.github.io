---
layout: paper
permalink: /papers/arxiv21a/
title: "Node-Level Membership Inference Attacks Against Graph Neural Networks"
teaser: "/assets/img/publication_preview/arxiv21a.png"
teaser_caption: "A schematic overview of node-level membership inference attack against GNNs. Note that for the combined attack, we conduct 0-hop, 1-hop, and 2-hop query to obtain the inputs of the attack model."
authors: 
    - name: "Xinlei He"
      affiliation: "CISPA Helmholtz Center for Information Security"
    - name: "Rui Wen"
      affiliation: "CISPA Helmholtz Center for Information Security"
    - name: "Yixin Wu"
      affiliation: "CISPA Helmholtz Center for Information Security"
    - name: "Michael Backes"
      affiliation: "CISPA Helmholtz Center for Information Security"
    - name: "Yun Shen"
      affiliation: "NetApp"
    - name: "Yang Zhang"
      affiliation: "CISPA Helmholtz Center for Information Security"
conference: "arXiv"
abstract: "Many real-world data comes in the form of graphs, such as social networks and protein structure. To fully utilize the information contained in graph data, a new family of machine learning (ML) models, namely graph neural networks (GNNs), has been introduced. Previous studies have shown that machine learning models are vulnerable to privacy attacks. However, most of the current efforts concentrate on ML models trained on data from the Euclidean space, like images and texts. On the other hand, privacy risks stemming from GNNs remain largely unstudied. In this paper, we fill the gap by performing the first comprehensive analysis of node-level membership inference attacks against GNNs. We systematically define the threat models and propose three node-level membership inference attacks based on an adversary's background knowledge. Our evaluation on three GNN structures and four benchmark datasets shows that GNNs are vulnerable to node-level membership inference even when the adversary has minimal background knowledge. Besides, we show that graph density and feature similarity have a major impact on the attack's success. We further investigate two defense mechanisms and the empirical results indicate that these defenses can reduce the attack performance but with moderate utility loss."
paper: "https://arxiv.org/pdf/2102.05429.pdf"
code: "."
citation: |
  @article{HWWBSZ21,
    title={Node-Level Membership Inference Attacks Against Graph Neural Networks},
    author={He, Xinlei and Wen, Rui and Wu, Yixin and Backes, Michael and Shen, Yun and Zhang, Yang},
    journal={arXiv},
    year={2021}
  }

---

{% include paper_page.liquid %}