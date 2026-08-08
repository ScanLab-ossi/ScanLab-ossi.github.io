---
layout: post
title: "Latent Personal Analysis (LPA) Published with SpringerNature in UMUAI"
date: 2021-08-13 10:23:17+0000
description: Style is the silence between the words. LPA builds a personal signature from missing popular words, with applications across text, music, and biology.
tags: surprisability authorship impersonation
categories: research
---

Glad to share a [new paper](https://rdcu.be/ctKvM) in *User Modeling and User-Adapted Interaction* (UMUAI) with *Hagit Ben-Shoshan*, describing an exploration method in a complex domain: **Latent Personal Analysis (LPA)**, with uses for user/entity modeling, impersonation detection in social media, music, and biology.

The method creates a domain, and a signature and distance for each entity comprising the domain. In language, within a domain, an author's signature can be derived from, in loose terms, the author's missing popular words and frequently used infrequent words. The distance and the signature are determined by **increased** distance for **missing popular** terms and **decreased** distance for the vast tail of **rare** words missing from the person's vocabulary. Paraphrasing Debussy, style is the silence between the words: personal style is also measured by popular domain words missing from a person's vocabulary.

### How about applications?

**Authorship attribution and the digital humanities.**

<img src="{{ '/assets/img/blog/lpa-style-heatmap.png' | relative_url }}" class="img-fluid rounded" alt="Style heatmap of 19th-century writers" />

For example, a style heatmap of 19th-century writers, comparing books' signature distances to determine similarity.

*Qualitative exploration:* the book Robinson Crusoe was taken as a domain, and each chapter as an entity.

<img src="{{ '/assets/img/blog/lpa-robinson-crusoe.jpeg' | relative_url }}" class="img-fluid rounded" alt="Robinson Crusoe chapter-level LPA analysis" />

The lower panel shows the most frequent words in the book (not considering stopwords). Interestingly, *God* is one of the principal words in the domain, i.e., in the book. However, in the last chapter, the word *God* appears much less than in the rest of the book, while the word *lough* is much more frequent.

**Social media user modeling.** LPA can be used for better user modeling. For example, the signatures of two IMDb reviewers form a content-based exploration, exposing preferences as well as less preferred genres.

**Impersonation detection.** LPA can determine a form of sockpuppets, that is, several users authored by a single person. Interestingly, it can also flag a Front User account: a single account operated by multiple authors.

<img src="{{ '/assets/img/blog/lpa-front-users.png' | relative_url }}" class="img-fluid rounded" alt="Front-user account detection via LPA" />

**Music.** Spotify's 2017 dataset of all songs streamed in that year, and their listening frequency in each country, was the basis for an analysis that created an LPA distance and signature for each country. Countries that listen more to popular music have a lower distance — examples are Canada, Switzerland, and Australia, whose signatures are characterized by small differences in listening habits to hit songs. Countries distant from the domain are where local music is preferred, for example Turkey or Uruguay.

<img src="{{ '/assets/img/blog/lpa-music-pca.png' | relative_url }}" class="img-fluid rounded" alt="PCA of countries' Spotify LPA signatures" />

**Biology.** LPA was used to compare the spectral spread of sub-repertoires of B cell clones (B cells with a shared mother cell) within a person. We reiterated previous findings showing that gut and blood tissues have separate repertoires. We further identify a third branch of clonal patterns typical of the lymphatic organs (spleen, MLN, and bone marrow), separated from the other two categories. We also show that the spleen encompasses the closest picture of the entire repertoire, and person-popular clones are as popular in the spleen. [The LPA biology paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8047331/) with Uri Alon and Uri Hershberg.

**Literature debates.** Few have questioned the authorship of the Shakespearean poem "A Lover's Complaint". Creating a domain from all of Shakespeare's writings, most have a typical distance — which is not the case for the poem in question.
