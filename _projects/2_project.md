---
layout: page
title: MEXA
description: Multilingual evaluation of English-centric LLMs via cross-lingual alignment (ACL Findings 2025).
img:
importance: 2
category: research
related_publications: true
---

**MEXA** assesses the multilingual capabilities of pre-trained, English-centric LLMs using parallel sentences — available for many more languages than existing downstream tasks. Leveraging the observation that English-centric models use English as a pivot in their intermediate layers, MEXA computes the alignment between English and non-English languages to estimate multilingual performance {% cite kargaran2025mexa %}.

In its default setting, MEXA reaches a statistically significant average Pearson correlation of 0.90 with three established downstream tasks across nine models and two parallel datasets.

- 📄 Paper: [ACL Anthology](https://aclanthology.org/2025.findings-acl.1385/) · [arXiv:2410.05873](https://arxiv.org/abs/2410.05873)
- 💻 Code: [github.com/cisnlp/MEXA](https://github.com/cisnlp/MEXA)
- 🏆 Leaderboard: [huggingface.co/spaces/cis-lmu/Mexa](https://huggingface.co/spaces/cis-lmu/Mexa)
