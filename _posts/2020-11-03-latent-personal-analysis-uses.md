---
layout: post
title: "Domain-Based Latent Personal Analysis (LPA) and Its Uses"
date: 2020-11-03 17:46:12+0000
description: A personal signature built from the popular words someone omits and the rare words they favour, with uses from authorship attribution to impersonation detection.
tags: surprisability authorship impersonation
categories: research
---

LPA is an easy-to-use and fast domain-based spectral signature that can be used in a variety of domains and is tailored for big-data computations. It creates a strong and unique signature of both over-used and missing items that identify a user or a component in a domain. It can be used in a variety of domains, from textual to computational.

**Paper:** Mokryn, O., & Ben-Shoshan, H. (2020). "Domain-based Latent Personal Analysis and its use for impersonation detection in social media." Accepted to _User Modeling and User-Adapted Interaction_ (UMUAI), May 2021. arXiv:2004.02346. ([PDF](https://arxiv.org/pdf/2004.02346.pdf))

Zipf's law defines an inverse proportion between a word's ranking in a given corpus and its frequency in it, roughly dividing the vocabulary into frequent (popular) words and infrequent ones. Here, we stipulate that within a domain an author's signature can be derived from, in loose terms, the author's missing popular words and frequently used infrequent words. We devise a method, termed Latent Personal Analysis (LPA), for finding such domain-based personal signatures. LPA determines what words most contributed to the distance between a user's vocabulary and the domain's.

We identify the most suitable distance metric for the method among several and construct a personal signature for authors. We validate the correctness and power of the signatures in identifying authors and utilize LPA to identify two types of impersonation in social media: (1) authors with sockpuppet (multiple) accounts; (2) front-user accounts, operated by several authors. We validate the algorithms and employ them over a large-scale dataset obtained from a social media site with over 4000 accounts, and corroborate the results employing temporal rate analysis. LPA can be used to devise personal signatures in a wide range of scientific domains in which the constituents have a long-tail distribution of elements.

<img src="{{ '/assets/img/blog/lpa-music-pca.png' | relative_url }}" class="img-fluid rounded" alt="LPA signatures of countries from Spotify streaming" />

<!-- IMAGE (from Wix): authorship attribution applications -->

**Impersonation on social media: sockpuppet accounts**

LPA is fast and easy to implement at large scale. We deployed it over 4000 IMDb reviewer accounts to find sockpuppet accounts activated by a single author, performing a 4000x4000 similarity measure between all accounts' LPA signatures. The full list of suspected [sockpuppets](https://github.com/hagitbenshoshan/imdb-soakpuppets) is available.

_Example 1:_ [User 59775972](https://www.imdb.com/user/ur59775972) (joshuadrake-39480) and [User 62431316](https://www.imdb.com/user/ur62431316) (joshuadrake-91275) have 502 common terms in their LPA signatures, and the distance between their signatures is 0.013.

_Example 2:_ [User 24051675](https://www.imdb.com/user/ur24051675) (jpachar82) and [User 53564354](https://www.imdb.com/user/ur53564354) (jasonpachar) have 584 common terms in their LPA signatures, and the distance between their signatures is 0.297.

<img src="{{ '/assets/img/blog/lpa-sockpuppets.png' | relative_url }}" class="img-fluid rounded" alt="Two IMDb accounts identified as sockpuppets by their LPA signatures" />
