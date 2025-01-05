---
layout: paper
permalink: /papers/arxiv24a/
title: "Voice Jailbreak Attacks Against GPT-4o"
teaser: "/assets/img/publication_preview/arxiv24a.jpeg"
teaser_caption: "Attack flow of VOICEJAILBREAK."
authors: 
    - name: "Xinyue Shen"
      affiliation: "CISPA Helmholtz Center for Information Security"
      equal_contribution: true
    - name: "Yixin Wu"
      affiliation: "CISPA Helmholtz Center for Information Security"
      equal_contribution: true
    - name: "Michael Backes"
      affiliation: "CISPA Helmholtz Center for Information Security"
    - name: "Yang Zhang"
      affiliation: "CISPA Helmholtz Center for Information Security"
conference: "arXiv"
abstract: "Recently, the concept of artificial assistants has evolved from science fiction into real-world applications. GPT-4o, the newest multimodal large language model (MLLM) across audio, vision, and text, has further blurred the line between fiction and reality by enabling more natural human-computer interactions. However, the advent of GPT-4o's voice mode may also introduce a new attack surface. In this paper, we present the first systematic measurement of jailbreak attacks against the voice mode of GPT-4o. We show that GPT-4o demonstrates good resistance to forbidden questions and text jailbreak prompts when directly transferring them to voice mode. This resistance is primarily due to GPT-4o's internal safeguards and the difficulty of adapting text jailbreak prompts to voice mode. Inspired by GPT-4o's human-like behaviors, we propose VoiceJailbreak, a novel voice jailbreak attack that humanizes GPT-4o and attempts to persuade it through fictional storytelling (setting, character, and plot). VoiceJailbreak is capable of generating simple, audible, yet effective jailbreak prompts, which significantly increases the average attack success rate (ASR) from 0.033 to 0.778 in six forbidden scenarios. We also conduct extensive experiments to explore the impacts of interaction steps, key elements of fictional writing, and different languages on VoiceJailbreak's effectiveness and further enhance the attack performance with advanced fictional writing techniques. We hope our study can assist the research community in building more secure and well-regulated MLLMs."
paper: "https://arxiv.org/pdf/2405.19103.pdf"
code: "https://github.com/TrustAIRLab/VoiceJailbreakAttack"
citation: |
  @article{SWBZ24,
    title={Voice Jailbreak Attacks Against GPT-4o},
    author={Shen, Xinyue and Wu, Yixin and Backes, Michael and Zhang, Yang},
    journal={arXiv},
    year={2024}
  }
---

{% include paper_page.liquid %}