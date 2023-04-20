---
layout: post
permalink: /2023/04/machine-learning-for-license-identification.html
title:  "Using Machine Learning for Open Source License Identification"
author: oscar
categories: [ oss, development, ai ]
tags: [ai, machinelearning, python, oss]
image: images/posts/oslili.jpg
description: "Using Machine Learning for Open Source License Identification"
featured: true
comments: true
---

A few days ago, I discussed with a few colleagues the different techniques for identifying Open Source Licenses using tools. While many approaches exist, most are based on regular expressions and similar methods. While using that technique is fast and straightforward, it involves a lot of maintenance due to the need to keep checking and adding new patterns to map new licenses or adjust for modified versions.
A different technique used by the OSS project [Askalono](https://github.com/jpeddicord/askalono) is using Sørensen–Dice scoring for matching text. Jacob, the author, implemented a fast and reliable method that led me to think that [Askalono](https://github.com/jpeddicord/askalono) is the way to go. Still, I wonder if Machine Learning could also be used to identify licenses, thinking we could combine regular expressions, checksums and hashes, and machine learning in the future.

I had some time during the weekend. Since my coding skills are a little rusty, I jumped to use Python and a precooked library to implement license identification through vectorization and classification. Indeed, the result is not the best code or a product I'm proud of. Still, it was a fun journey that allowed me to explore using Python and ML for coding and ChatGPT as a debugging tool (instead of writing the code for me).

I called the final project [OSLiLi](https://github.com/oscarvalenzuelab/oslili), which stands for Open Source License Identification Library. I used Scikit-learn to implement a Multinomial Naive Bayes classifier trained (old school) with SPDX data to identify Open Source Licenses. I even implemented a [CLI](https://github.com/oscarvalenzuelab/oslili-cli) for the library. It works, but sometimes it needs a little nudge. Give it a try! You can find both projects on my [GitHub account](https://github.com/oscarvalenzuelab/oslili).