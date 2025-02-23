---
layout: paper
permalink: /papers/usenix25a/
title: "Synthetic Artifact Auditing: Tracing LLM-Generated Synthetic Data Usage in Downstream Applications"
authors: 
  - name: "Yixin Wu"
    affiliation: "CISPA Helmholtz Center for Information Security"
  - name: "Ziqing Yang"
    affiliation: "CISPA Helmholtz Center for Information Security"
  - name: "Yun Shen"
    affiliation: "NetApp"
  - name: "Michael Backes"
    affiliation: "CISPA Helmholtz Center for Information Security"
  - name: "Yang Zhang"
    affiliation: "CISPA Helmholtz Center for Information Security"
conference: "USENIX Security Symposium 2025"

content_blocks:
  - title: "Motivation"
    text: |
      Synthetic data have the potential to contain biases and hallucination. In downstream training and analysis process, the bias and inaccurate information could undermine the reliability of the decision-making process.

      Thinking of a real life example of treating potential risks to the consumers with allergies, the allergen labeling is a practice to identifies and discloses the presence of potential allergens in food products to protect consumers with allergies.

      In the same vein, to raise users’ awareness and thereby reduce unexpected consequences and risks in downstream applications, it is necessary to label those trained on or derived from synthetic data!

      Furthermore, many AI companies have usage terms that prohibit competitors from using synthetic data to develop competing products. Nowadays, there are news reports about unauthorized use behaviors that violate such usage terms. There is an emergent need for an auditing tool that assists them in collecting evidence of these unauthorized uses.

  - title: "Main Contributions"
    text: |
      - **Novel Concept**: We introduce the concept of synthetic artifact auditing. Given an artifact, it determines whether it is trained on or derived from LLM-generated synthetic data.
  
      - **Novel Techniques**: We propose an auditing framework with three methods that require no disclosure of proprietary training specifics: metric-based auditing, tuning-based auditing, and classification-based auditing. This framework is extendable, currently supporting auditing for classifiers, generators, and statistical plots.
  
      - **Extensive Evaluation**: We evaluate our auditing framework on seven downstream tasks across three training scenarios. The evaluation demonstrates the effectiveness of all proposed auditing methods across all these tasks.
  - title: "Concept"
    text: "We introduce the concept of synthetic artifact auditing. Given a target artifact, we aim to determine whether the synthetic data was involved in the developing process."
    image: "/assets/img/publication_preview/usenix25a_concept.jpeg"
  - title: "Real Data vs. Synthetic Data (Zero-Shot)"
    image: "/assets/img/publication_preview/usenix25a_intuition2.jpeg"
    image_caption: |
      The distribution for 2-class real data appears well mixed.

      We generate synthetic data conditioned on the label (positive or negative). Two distinct small groups of yellow and purple points at the bottom, indicates different structural pattern in the data. With the synthetic proportion increases, the distinction between data samples from different classes becomes more pronounced, leading to a more distinct decision boundary.
  - title: "Real Data vs. Synthetic Data (Paraphrasing)"
    image: "/assets/img/publication_preview/usenix25a_intuition1.jpeg"
    image_caption: "We then generate synthetic data by paraphrasing existing real data and we can still see a clearer decision boundary between data from different classes, which distinguish the real and synthetic data."
  - title: "Hypothesis"
    text: |
      - Synthetic classifiers tend to be more confident when predicting labels for synthetic input texts and less confident with real input texts compared to real classifiers.
      - Real classifiers tend to be more confident when predicting labels for real input texts and less confident with synthetic input texts compared to synthetic classifiers.
  - title: "Auditing Methods"
    text: |
      In general, our auditing framework follows a procedure:
      1. We train a set of reference synthetic and real artifacts.
      2. By feeding a set of queries into reference artifacts, we get the corresponding outputs, measure them with the performance metrics, and get the threshold.
      3. Then, at the inference time, we feed the same queries into target artifact to calculate the metric value and compare it with the threshold to determine whether the synthetic data was involved.
  
      Queries:
      - With black-box access, we consider random synthetic input texts or real input texts.
      - With white-box access, we tune queries—essentially embeddings—that best represent the unique pattern distinguishing synthetic artifacts from real artifacts.
      - The statistical plots do not provide output to measure performance, but we can directly see the difference between the synthetic and real data, as shown in the t-SNE plots. Therefore, we consider using an image classifier to determine whether synthetic data is involved.
    image: "/assets/img/publication_preview/usenix25a_auditing.jpeg"
    image_caption: "The general auditing framework."
  - title: "Evaluation"
    text: |
      - This paper evaluates the auditing framework on three text classification tasks, two text summarization tasks, and two data visualization tasks with four LLMs across three scenarios.

      - The three scenarios for training synthetic artifacts are:
        1. \\(S_1\\): Training exclusively on synthetic data (100%) generated from a single LLM.
        2. \\(S_2\\): Training on a mix of real and synthetic data from a single LLM; In evaluation, we vary the proportion of synthetic data from 10% to 100% in increments of 10%.
        3. \\(S_3\\): Training on a mix of real and synthetic data from multiple LLMs (all four LLMs); The proportions of synthetic data are randomized.
      
      - In general, it can achieve good auditing performance across all tasks and scenarios. With black-box access and limited resources, it achieves an average accuracy of 0.868±0.071 for auditing classifiers and 0.880±0.052 for auditing generators. Meanwhile, it can also achieve 0.966±0.003 average accuracy for auditing statistical plots.

  - title: "Impact"
    text: |
      Our work has a real-world impact in promoting the responsible use of synthetic data and aligning with corresponding regulations and laws. Regulatory and governmental bodies are increasingly prioritizing data governance and transparency in the development of AI systems. For instance, the UK's ICO requires documentation of synthetic data creation and its properties. Similarly, California recently passed Law AB 2013, mandating the disclosure of training datasets, including the use of synthetic data. Our framework provides a practical means for third parties to audit artifacts without requiring the disclosure of proprietary training details by artifact owners. This supports compliance with data governance and transparency requirements, enhances alignment with regulatory and legal standards (e.g., EU AI Act), and facilitates responsible and accountable AI practices.


paper: "."
code: "https://github.com/TrustAIRLab/synthetic_artifact_auditing"
video: "."
slides: "."
citation: |
  @inproceedings{WYSBZ25,
    title={Synthetic Artifact Auditing: Tracing LLM-Generated Synthetic Data Usage in Downstream Applications},
    author={Wu, Yixin and Yang, Ziqing and Shen, Yun and Backes, Michael and Zhang, Yang},
    booktitle={USENIX Security Symposium},
    year={2025}
  }
---

{% include advanced_paper_page.liquid %}