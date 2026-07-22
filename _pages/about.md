---
permalink: /
title: "Junteng Liu"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a first-year Ph.D. candidate in the [HKUST NLP Group](https://hkust-nlp.github.io/) at the Hong Kong University of Science and Technology (HKUST), advised by Prof. [Junxian He](https://www.cse.ust.hk/~jhexian/). I received my Bachelor of Engineering degree from Shanghai Jiao Tong University (SJTU) in June 2024.

My research focuses on natural language processing and machine learning. Specifically, I am broadly interested in the following topics:

- **LLM Reasoning and Reinforcement Learning** — developing reasoning capabilities in large language models, including synthesizing verifiable reasoning data at scale.
- **Hallucination in Vision-Language Models (VLMs)** — understanding and mitigating hallucination problems in multimodal models, especially for chart understanding.
- **LLM Truthfulness and Interpretability** — investigating the inner representations of LLMs that encode truthfulness, and using these to mitigate hallucinations.

News & Updates
======
* Feb 2025: Started a research internship at MINIMAX.
* 2024: Paper "On the Universal Truthfulness Hyperplane Inside LLMs" accepted to EMNLP 2024.
* 2024: Paper "In-Context Sharpness as Alerts" accepted to ICML 2024.
* Jun – Sep 2024: Research internship at Tencent WXG, advised by Zifei Shan.
* Jun 2023 – Dec 2023: Research internship at Shanghai AI Lab, advised by Prof. Yu Cheng.
* 2023: Two papers accepted to NeurIPS 2023 (C-Eval, Composing Parameter-Efficient Modules with Arithmetic Operations).

Education
======
* **Ph.D. in Computer Science**, Hong Kong University of Science and Technology, 2024 – Present
* **B.Eng.**, Shanghai Jiao Tong University, 2020 – 2024

Honors
======
* Zhiyuan Honor Scholarship, Shanghai Jiao Tong University

Internships
======
* **Research Intern, MINIMAX**, Feb 2025 – Present
* **Research Intern, Tencent WXG**, Jun 2024 – Sep 2024 (advisor: Zifei Shan)
* **Research Intern, Shanghai AI Lab**, Jun 2023 – Dec 2023 (advisor: Prof. Yu Cheng)

Selected Publications
======

A full list is available on the [Publications]({{ '/publications/' | relative_url }}) page. You can also find my articles on [my Google Scholar profile](https://scholar.google.com/citations?hl=en&user=tbK9jl4AAAAJ&view_op=list_works&sortby=pubdate).

{% include base_path %}

<!-- New style rendering if publication categories are defined -->
{% if site.publication_category %}
  {% for category in site.publication_category  %}
    {% assign title_shown = false %}
    {% for post in site.publications reversed %}
      {% if post.category != category[0] %}
        {% continue %}
      {% endif %}
      {% unless title_shown %}
        <h3>{{ category[1].title }}</h3><hr />
        {% assign title_shown = true %}
      {% endunless %}
      {% include archive-single.html %}
    {% endfor %}
  {% endfor %}
{% else %}
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}

