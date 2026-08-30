---
layout: home
title: Imprecise Probabilistic Machine Learning
---

> “There are known knowns. There are known unknowns. But there are also unknown unknowns—things we do not yet realize we do not know.” — Donald Rumsfeld (2002)

## About the Course

While modern machine learning (ML) algorithms have made significant progress, most are built on classical probability theory and associated decision theory. This framework often struggles to capture the multifaceted uncertainties inherent in complex, real-world systems, which can negatively impact the robustness, trustworthiness, and safety of deployed models. Imprecise probability (IP) provides a more flexible and faithful approach to representing and manipulating uncertainty. By relaxing the additivity axiom, which is a foundational rule in Kolmogorov’s classical probability theory, we can create more flexible models for quantifying uncertainty. These models, which go beyond standard probability measures, include concepts like capacities, lower and upper previsions, and belief functions, along with possibility and necessity measures. Imprecise Probabilistic Machine Learning (IPML) is a growing area of research dedicated to developing ML models that leverage IP theory to achieve greater robustness, trustworthiness, and safety.

In this course, students will learn the theoretical foundations of imprecise probability, its ability to capture the complex uncertainties in real-world systems, and its practical applications in machine learning. The course will explore the field's breadth, from philosophical debates surrounding the nature and interpretation of probability to cutting-edge applications in areas such as classification, regression, conformal prediction, reinforcement learning, causal inference, and foundation models. In addition, students will gain hands-on experience implementing simple IPML algorithms to solve problems in different application areas.

This course covers four main topics:

1. **Foundation of Imprecise Probability** — learn the core principles behind this powerful theory.
2. **Imprecise Probabilistic Machine Learning (IPML)** — discover how to integrate IP into machine learning models.
3. **IPML in Modern AI** — explore its application in cutting-edge fields like deep learning, foundation models, large language models (LLMs), and generative AI (GenAI).
4. **Applications for Trustworthy AI** — understand how IPML can be used to improve fairness, privacy, ethics, and safety in AI systems.

Throughout the course, students will solidify their understanding by completing a combination of written and coding exercises. This hands-on approach allows them to implement and evaluate the techniques they learn.

## Outline

The course is divided into two main parts.

**Part I** establishes the foundational concepts of imprecise probability. We will look at various IP models, exploring their intuitive motivations and technical underpinnings. The core focus will be on possibility measures, random sets, belief functions, and lower/upper previsions. This part concludes with an examination of key decision-making criteria tailored for imprecise probability models.

**Part II** explores the practical applications of imprecise probability in machine learning. Topics covered will include its use in classification, regression, conformal prediction, and uncertainty quantification, as well as its relevance to reinforcement learning, causal inference, and foundation models. Students will also learn to implement fundamental imprecise probability algorithms for these diverse applications. A course project allows students to further tailor the material to their specific interests.

## Prerequisite

Students are expected to have completed an introductory course in (probabilistic) machine learning and be familiar with core concepts such as statistical learning, linear regression, classification, clustering, neural networks, Bayes’ rule, probabilistic graphical models, likelihood and maximum likelihood estimation, Bayesian inference, probabilistic prediction, and uncertainty quantification. Familiarity with basic probability theory, linear algebra, and calculus is assumed. Prior knowledge of measure theory is not required, although familiarity with it is beneficial.

## Resources

A curated list of books, articles, theses, and research papers related to the course is maintained in the [references]({{ '/references/' | relative_url }}) page.

If you are aware of any relevant resources that should be included (e.g. your own work), please feel free to submit a pull request on [GitHub]({{ site.github_repo }}) or contact us by [email](mailto:{{ site.contact_email }}?subject=IPML:%20Missing%20Resources).
