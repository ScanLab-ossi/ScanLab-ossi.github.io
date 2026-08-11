---
layout: post
title: "New: Open-Source, Large-Scale, Temporal Random Network Generator"
date: 2021-09-22 21:23:53+0000
description: DynamicRandomGraphs, a Python package for generating scalable temporal random graphs, by Yanir Marmor and Alex Abbey.
tags: temporal-networks open-source
categories: research
---

ScanLab is happy to share [DynamicRandomGraphs](https://github.com/ScanLab-ossi/DynamicRandomGraphs): a Python package for the generation of scalable temporal random graphs, by Yanir Marmor and Alex Abbey.

**RandomDynamicGraph** is a **Python package** that implements the algorithm from [1] for generating large-scale dynamic temporal random graphs. The package **focuses on massive data generation: it uses efficient math calculations, writes to file instead of in-memory when datasets are too large, and supports multi-processing.**

_Background:_ Large-scale real-world interaction systems, such as social, technological, and biological networks, are dynamic structures that change with time. There is an increased interest in studying the dynamics and temporal evolution of these systems. One of the ways is by modeling these systems using dynamic temporal networks.

Models for studying networks are primarily static. The work in [1] offered a natural generalization to the Erdős–Rényi static network model, where one assumes that continuous-time Markov processes govern the appearance and disappearance of edges. Thus, the fundamental unit of analysis is the entire history of the network. Edges appear and disappear by making transitions from present to absent or vice versa at certain rates. For example, in temporal random networks, the rate depends on the required probability of having an edge between any two nodes.

The package has many uses, including in epidemiology. Temporal modeling is fundamental in the research and understanding of virality and epidemics: airborne diseases spread over networks of contacts between individuals that change in time, and ideas dynamically spread over social networks.

<img src="{{ '/assets/img/blog/temporal-random-graph-density.png' | relative_url }}" class="img-fluid rounded" alt="Temporal network density across 10,000 snapshots" />

[1] Zhang, Xiao, Cristopher Moore, and Mark E. J. Newman. "Random graph models for dynamic networks." _The European Physical Journal B_ 90.10 (2017): 1--14.
