---
layout: page
title: CoBia
description: Constructed conversations that trigger otherwise concealed societal biases in LLMs (EMNLP 2025, Oral).
img:
importance: 1
category: research
related_publications: true
---

**CoBia** is a suite of lightweight adversarial attacks that refine the conditions under which large language models depart from normative or ethical behavior in conversation. CoBia constructs a dialogue in which the model appears to have uttered a biased claim about a social group, then evaluates whether the model can recover and reject biased follow-up questions.

Across 11 open-source and proprietary LLMs and six socio-demographic categories — gender, race, religion, nationality, sexual orientation, and others — we find that purposefully constructed conversations reliably reveal bias amplification that standard, single-turn safety checks miss {% cite nikeghbal2025cobia %}.

- 📄 Paper: [ACL Anthology](https://aclanthology.org/2025.emnlp-main.84/) · [arXiv:2510.09871](https://arxiv.org/abs/2510.09871)
- 💻 Code: [github.com/nafisenik/CoBia](https://github.com/nafisenik/CoBia)
