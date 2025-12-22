---
title: "Embodied-RAG: General non-parametric Embodied Memory for Retrieval and Generation"
category: manuscripts
permalink: /publication/2024-embodied-rag/
date: 2024-09-01
venue: "In submission"
paperurl: "https://arxiv.org/abs/2409.18313"
weburl: "https://quanting-xie.github.io/Embodied-RAG-web/"
bibtexurl: "/files/publications/2024-Embodied/ref.txt"
excerpt: "Embodied-RAG equips embodied agents with a non-parametric memory system for retrieval and generation."
header:
  teaser: publications/2024-Embodied/Figure_1_overview.png
---

**Authors:** Quanting Xie, So Yeon Tiffany Min, Tianyi Zhang, Aarav Bajaj, Ruslan Salakhutdinov, Matthew Johnson-Roberson, Yonatan Bisk

## Abstract

There is no limit to how much a robot might explore and learn, but all of that knowledge needs to be searchable and actionable. Within language research, retrieval augmented generation (RAG) has become the workhorse of large-scale non-parametric knowledge, however existing techniques do not directly transfer to the embodied domain, which is multimodal, data is highly correlated, and perception requires abstraction.

To address these challenges, we introduce Embodied-RAG, a framework that enhances the foundational model of an embodied agent with a non-parametric memory system capable of autonomously constructing hierarchical knowledge for both navigation and language generation. Embodied-RAG handles a full range of spatial and semantic resolutions across diverse environments and query types, whether for a specific object or a holistic description of ambiance. At its core, Embodied-RAG's memory is structured as a semantic forest, storing language descriptions at varying levels of detail. This hierarchical organization allows the system to efficiently generate context-sensitive outputs across different robotic platforms. We demonstrate that Embodied-RAG effectively bridges RAG to the robotics domain, successfully handling over 200 explanation and navigation queries across 19 environments, highlighting its promise for a general-purpose non-parametric system for embodied agents.

## Links

- Paper: `https://arxiv.org/abs/2409.18313`
- Project: `https://quanting-xie.github.io/Embodied-RAG-web/`
- BibTeX: `/files/publications/2024-Embodied/ref.txt`