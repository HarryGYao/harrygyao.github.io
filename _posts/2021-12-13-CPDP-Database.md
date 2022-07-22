---
layout: post
title: Citizen’s Police Data Project
subtitle: with The Dapper Squirrels
cover-img: /assets/img/CPDB/cpdb-2.png
thumbnail-img: /assets/img/CPDB/cpdb-1.png
gh-repo: NU-DSS-The-Dapper-Squirrels/The-Dapper-Squirrels
gh-badge: [star, fork, follow]
categories:
    - Project
tags: [CPDB, Data Science]
---

#### Team: the dapper squirrels

## Table of Contents

- [Table of Contents](#table-of-contents)
- [Theme](#theme)
- [Relational Analysis Questions](#relational-analysis-questions)
- [Verification Technique](#verification-technique)
  - [Visualization](#visualization)
  - [Interactive Visualization](#interactive-visualization)
  - [Graph Analytics](#graph-analytics)
  - [NLP models](#nlp-models)
- [References](#references)

## Theme

Misconduct analysis in terms of different locations and communities can be valuable.
Is there over-policing in low socio-eco status neighborhoods? We could compare
the low-income area data with high in-come area data. The income of the neighbor
could be a factor to influence the “victim” narrative (complaint report). We plan
to dive deep into the relationship between location, income level, and police
misconduct.

Our final report: [Final Report](Project-Report.pdf);\
Our final presentation: [Final Presentation](DSS-Final-Presentation.pdf).

## Relational Analysis Questions

1. What are the TOP5 richest and lowest income neighborhoods?
2. What are the neighborhoods’ income and CRs(complaint record) per capita?
3. What is the TRRS(tactical response report) per capita?
4. What is the percentage of each race in the community?
5. What are the top 5 streets in allegation counts for each beat area?

Please check out SQLs and findings in [`checkpoint-1`](checkpoint-1/README.md).

## Verification Technique

### Visualization

We would like to dive deep into the relationship between the income of officers
versus common people by visualization tools like Tableau, which is more clear and
interpretable than numbers.
1. Visualize by using a line chart to show the officer hours/year per capita in
each community by years if change over time.
2. Scatterplot of Complaint Report per capita V.S. Tactical Respond Report per
capita. We could also consider lawsuits between “victims” and police officers;
search warrants granted in each complaint?

Please check out our code and findings in [`checkpoint-2`](checkpoint-2//README.md).

### Interactive Visualization

Looking into trends of comparisons and numbers in time can be intuitive. We are
specifically interested in the comparisons of complaint rate change as opposed
to income change in time.
1. Highlighting the high and low socio-economy status communities with different
colors and plot TRRs on them. Set up a time slider to see how it changes over time.
2. Using color code(heat map) of A&A (dara_officer assignment attendance) in different
neighborhoods. Set up a time slider to see how it changes over time.

Please check out our code and findings in [`checkpoint-3`](checkpoint-3//README.md).

### Graph Analytics

Graph analytics can be very useful in analyzing relationships between different
groups of people. We can create nodes based on their income, race, neighborhood,
and other attributes. After building the graph, we can analyze interactions among
different nodes and even graphlets.
1. Making nodes of officers and victims by their income, race, locations, and even
unsupervised machine learning models to learn the cluster and see if there is a
potential connection between officers and victims.
2. Network dynamics of co-accused in each cohort can be interesting. The analytics
can be done with the following:
    1. Make use of  Triangle Count Algorithms for each cohort.
    2. Make use of the Page Rank Algorithm to find the most connected officer in all cohorts.
    3. How many CRs that officers have and how many co-accused for each cohort.
    4. Compare the top k largest cohort of police officers in high and low socio-economy
  status.

Please check out our code and findings in [`checkpoint-4`](checkpoint-4//README.md).

### NLP models

Topic modeling is quite popular and useful in the NLP area. We are interested in
topics in CRS in each cohort. Just as the descriptions put, manual labeling by
officers is fallacious in many cases. However, with the development of natural
language processing, we may apply it to label complaint texts with high accuracy.
This would help a lot in understanding and analyzing misconduct. Technical solutions
span classical algorithms like TF-IDF and cutting-edge research methods like graph
neural networks **[2]** and BERT **[3]**. We plan to dive deeper
into the area and find out more effective and proper methods for us.

Please check out our code and findings in [`checkpoint-5`](checkpoint-5//README.md).

Click [HERE](https://nu-dss-the-dapper-squirrels.github.io/The-Dapper-Squirrels/){:target="_blank"} to see more about the project.

## References

[1] Liang et al. EURASIP Journal on Wireless Communications and Networking (2017)
2017:211

[2] O. Alqaryouti, T. A. Farouk, A. R. Nabhan and K. Shaalan, "Graph-Based Keyword
Extraction," in Intelligent Natural Language Processing: Trends and Applications,
Springer, Cham, 2018, pp. 159-172. [DOI:10.1007/978-3-319-67056-0_9]

[3] Keyword Extraction with BERT
https://towardsdatascience.com/keyword-extraction-with-bert-724efca412ea




