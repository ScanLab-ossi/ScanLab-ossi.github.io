---
layout: post
title: "Congratulations to Yossi Solomon on His Paper in Computer Networks!"
date: 2023-06-15 21:55:53+0000
description: SDNSandbox builds a provider network in a box, and uses its output to predict congestion.
tags: computer-networks open-source
categories: announcements
---

The paper "[SDNSandbox — Enabling learning-based innovation in provider networks](https://www.sciencedirect.com/science/article/abs/pii/S1389128622004807)" creates a framework of a "provider network in a box" and leverages its output to predict congestion conditions in a network.

**Abstract:** Provider networks are looking to follow the footsteps of cloud-based networks/data centers and incorporate Software-Defined Networking (SDN) technology. This move is problematic for various reasons, such as the networks' size and the providers' inability to control users' activity. Additionally, research into these networks is handicapped by the lack of information stemming from the confidentiality of these complex networks.

To that end, we have created SDNSandbox — an SDN-based provider network simulator prototype. SDNSandbox is an open-source, easy-to-use, provider-network in-a-laptop simulator. It aims to facilitate the creation of reproducible experiments and large-scale synthetic datasets. In its current prototype form, it uses a basic traffic generator module alongside real-world provider topologies.

SDNSandbox allows users to simulate provider networks, enabling them to conduct research in the field and examine practical applications. To demonstrate SDNSandbox, we use the prototype to simulate basic traffic conditions over several topologies. We then feed the generated datasets to DCRNN, a Convolutional Neural Network traffic pattern prediction module. We adapt DCRNN to accept SDNSandbox output and show that it can predict traffic conditions at various points within the network tens of seconds into the future. We further compare its performance with other baseline algorithms.

Our results demonstrate that SDNSandbox can also be used as a testbed for a digital twin, creating datasets that are hard to replicate in production networks. It also serves as a demonstration of the framework's power and versatility as a modular research tool.
