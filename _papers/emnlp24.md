---
layout: paper
permalink: /papers/emnlp24/
title: "The Death and Life of Great Prompts: Analyzing the Evolution of LLM Prompts from the Structural Perspective"
teaser: "/assets/img/publication_preview/emnlp24.jpeg"
teaser_caption: "Example prompts with component annotation. Prompts are adopted from our dataset."
authors: 
    - name: "Yihan Ma"
      affiliation: "CISPA Helmholtz Center for Information Security"
    - name: "Xinyue Shen"
      affiliation: "CISPA Helmholtz Center for Information Security"
    - name: "Yixin Wu"
      affiliation: "CISPA Helmholtz Center for Information Security"
    - name: "Boyang Zhang"
      affiliation: "CISPA Helmholtz Center for Information Security"
    - name: "Michael Backes"
      affiliation: "CISPA Helmholtz Center for Information Security"
    - name: "Yang Zhang"
      affiliation: "CISPA Helmholtz Center for Information Security"
conference: "Empirical Methods in Natural Language Processing (EMNLP) 2024"
abstract: "Effective utilization of large language models (LLMs), such as ChatGPT, relies on the quality of input prompts. This paper explores prompt engineering, specifically focusing on the disparity between experimentally designed prompts and real-world “in-the-wild” prompts. We analyze 10,538 in-the-wild prompts collected from various platforms and develop a framework that decomposes the prompts into eight key components. Our analysis shows that and Requirement are the most prevalent two components. Roles specified in the prompts, along with their capabilities, have become increasingly varied over time, signifying a broader range of application scenarios for LLMs. However, from the response of GPT-4, there is a marginal improvement with a specified role, whereas leveraging less prevalent components such as Capability and Demonstration can result in a more satisfying response. Overall, our work sheds light on the essential components of in-the-wild prompts and the effectiveness of these components on the broader landscape of LLM prompt engineering, providing valuable guidelines for the LLM community to optimize high-quality prompts."
paper: "https://aclanthology.org/2024.emnlp-main.1227.pdf"
code: "."
slides: "."
citation: |
  @inproceedings{MSWZBZ24,
    title={The Death and Life of Great Prompts: Analyzing the Evolution of LLM Prompts from the Structural Perspective},
    author={Ma, Yihan and Shen, Xinyue and Wu, Yixin and Zhang, Boyang and Backes, Michael and Zhang, Yang},
    booktitle={Empirical Methods in Natural Language Processing},
    year={2024}
  }
---

{% include paper_page.liquid %}