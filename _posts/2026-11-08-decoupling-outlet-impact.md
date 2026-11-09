---
layout: post
title: The Decoupling of Outlet from Impact in Economics
date: 2026-11-08
description: I replicated Kieran Healy's analysis of flagship sociology papers and found a similar decoupling of outlet and impact in economics. A large part of the change seems to be a field growing around journals that stayed the same size (not just top papers being steered elsewhere).
og_image: /assets/img/blog/fig_flagship_share.png
related_posts: false
---

I recently read an interesting article by [Kieran Healy](https://scholars.duke.edu/person/kieran.healy), a sociologist at Duke University, in which he asks the question: _are sociology's most influential papers still published in its most prestigious journals?_ Using Web of Science, he identified the ten most highly-cited sociology articles published in each decade from the 1930s to the 2010s and recorded the journal title. For the first few decades, nearly all were published in ASR or AJS. From the 1970s onward, the ASR/AJS journal share shrinks steadily, until by the 2010s neither flagship has a single paper in the top ten. Healy argues that, due in part to rapid expansion in doctoral degree production and increasing competition in the job market, top papers needed to make "significant contributions on multiple fronts" (theoretical, methodological, empirical). But even though flagship papers have converged to a common template, there has been some decoupling from long-run intellectual influence.

Anyway, Dr. Healy helpfully posted a [replication package online](https://github.com/kjhealy/rp-influence-isomorphism), so I was curious to see what the pattern looks like in economics. Publication in "top five" journals strongly influences tenure and promotion ([Heckman & Moktan, 2020](https://www.aeaweb.org/articles?id=10.1257/jel.20191574)), and the same processes of competition and scarcity highlighted by Healy have intensified competition in these outlets ([Card & DellaVigna, 2013](https://www.aeaweb.org/articles?id=10.1257/jel.51.1.144)). A recent preprint comparing publication patterns across fields identifies unusually strong consensus among economists about what journals are worth publishing in ([Van Buskirk et al., 2026](https://arxiv.org/abs/2603.00807)).

## Methods

This analysis is focused on the six "Top Fives": the *American Economic Review* (AER), the *Quarterly Journal of Economics* (QJE), the *Journal of Political Economy* (JPE), *Econometrica*, the *Review of Economic Studies* (REStud), and the *Review of Economics and Statistics* (REStat). Following [Healy (2026)](https://journals.sagepub.com/doi/abs/10.1177/00027642261497111), I grouped journal articles published between 1930 and 2026 into ten decade cohorts (except for the 2020s), identified the most-cited articles in each cohort, and classified them by the journal in which they appeared. Bibliographic records and lifetime citation counts come from OpenAlex. (OpenAlex does not classify journals by field, so I defined the field as 944 journals with at least 200 articles in which most articles published between 1930 and 2019 had a primary topic in "Economics, Econometrics and Finance", with a lower threshold for journals whose titles had words like "economics", "finance", etc.) I included all articles and reviews published in these 944 journals. For each decade, I identified which of the 10 most-cited articles were published in a Top Five, along with their share of all citations to the decade's papers. I ran it in R 4.6.1 and checked its measures against Healy's published replication package.

## Findings

### Economics shows the same decoupling Healy finds in sociology

In sociology, ASR/AJS start losing the top 10 in the 1970s. By the time you get to the 2010s, ASR/AJS have nothing in the top 10. In economics the decline starts in the 1980s. But by the 2020s the Top Fives still have papers in the top 10 (and probably would have had more had it not been for the *Journal of Econometrics*' trifecta of diff-in-diff papers).

<img src="{{ '/assets/img/blog/fig_top10_by_decade.png' | relative_url }}" class="img-fluid" alt="Top 10 most-cited economics and finance papers from each decade, 1930s to 2020s, by journal">

### Top Fives become *more* cited relative to the field but lose market share overall

The Top Fives' share of all citations to economics papers fell from 56% to 12%. Their share of papers fell even faster, so the average flagship paper became *more* cited relative to the field, rising from 4-6 fold to 8–9 fold. So this complicates a simple decoupling story.

<img src="{{ '/assets/img/blog/fig_flagship_share.png' | relative_url }}" class="img-fluid" alt="Share of each decade's most-cited work that appeared in the 6 Top Fives">
