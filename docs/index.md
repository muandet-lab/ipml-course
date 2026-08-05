# Imprecise Probabilistic Machine Learning

![IPML](course-logo.png)
 
> “There are known knowns. There are known unknowns. But there are also unknown unknowns—things we do not yet realize we do not know.”—Donald Rumsfeld (2002)

<br>

While modern machine learning (ML) algorithms have made significant progress, most are built on classical probability theory and associated decision theory. This framework often struggles to capture the multifaceted uncertainties inherent in complex, real-world systems, which can negatively impact the robustness, trustworthiness, and safety of deployed models. Imprecise probability (IP) provides a more flexible and faithful approach to representing and manipulating uncertainty. By relaxing the additivity axiom, which is a foundational rule in Kolmogorov’s classical probability theory, we can create more flexible models for quantifying uncertainty. These models, which go beyond standard probability measures, include concepts like capacities, lower and upper previsions, and belief functions, along with possibility and necessity measures. Imprecise Probabilistic Machine Learning (IPML) is a growing area of research dedicated to developing ML models that leverage IP theory to achieve greater robustness, trustworthiness, and safety.

In this course, students will learn the theoretical foundations of imprecise probability (IP), its ability to capture the complex uncertainties in real-world systems, and its practical applications in machine learning. The course will explore the field's breadth, from philosophical debates surrounding the nature and interpretation of probability to cutting-edge applications in areas such as classification, regression, conformal prediction, reinforcement learning, causal inference, and foundation models. In addition, students will gain hands-on experience implementing simple IPML algorithms to solve problems in different application areas.

This course covers four main topics:
1. **Foundation of Imprecise Probability**: Learn the core principles behind this powerful theory.
2. **Imprecise Probabilistic Machine Learning (IPML)**: Discover how to integrate IP into machine learning models.
3. **IPML in Modern AI**: Explore its application in cutting-edge fields like deep learning, foundation models, large language models (LLMs), and generative AI (GenAI).
4. **Applications for Trustworthy AI**: Understand how IPML can be used to improve fairness, privacy, ethics, and safety in AI systems.

Throughout the course, students will solidify their understanding by completing a combination of written and coding exercises. This hands-on approach allows them to implement and evaluate the techniques they learn.

## Outline of the Course
This course is divided into two main parts.

**`Part 1`** establishes the foundational concepts of imprecise probability (IP). We will look at various IP models, exploring their intuitive motivations and technical underpinnings. The core focus will be on possibility measures, random sets, belief functions, and lower/upper previsions. This section concludes with an examination of key decision-making criteria tailored for imprecise probability models.

**`Part 2`** explores the practical applications of imprecise probability in machine learning. Topics covered will include its use in classification, regression, conformal prediction, and uncertainty quantification, as well as its relevance to reinforcement learning, causal inference, and foundation models. Students will also learn to implement fundamental imprecise probability algorithms for these diverse applications. 
A course project, detailed below, allows students to further tailor the material to their specific interests.

### Part I: Foundation of Imprecise Probability

- **<a name="lecture-01"></a>`Lecture 1: Introduction`** introduces the fundamentals of statistical machine learning, emphasising the ultimate goal of learning from data. We will explore how uncertainty arises in machine learning—through data, models, and environments—and why managing it is central to effective learning. Core paradigms such as classification, regression, unsupervised, semi-supervised, self-supervised, and reinforcement learning will be discussed alongside Bayesian methods and generative modeling. Finally, we examine the limitations of current approaches in terms of generalization, robustness, trustworthiness, and safety, and show how these challenges are deeply rooted in probability theory.

   <em>Lecture notes: [Slides](lecture-01/lecture-01-introduction.pdf)</em>

   <em>Recommended reading:</em> TBA

- **<a name="lecture-02"></a>`Lecture 2: Overview of Imprecise Probability`** introduces different ways of understanding and representing uncertainty. We begin by asking what uncertainty is and how probability is used to model it, before exploring key interpretations of probability and their implications for machine learning. We then discuss categories of uncertainty, such as aleatoric and epistemic, and examine the limits of traditional probability theory. Finally, we look at the game-theoretic approach to uncertainty and introduce lower and upper previsions as a more flexible framework for reasoning under uncertainty.

   <em>Lecture notes: [Slides](lecture-02/lecture-02-overview-of-imprecise-probability.pdf)</em>

   <em>Recommended reading:</em>
   - [Imprecise Probabilities - Stanford Encyclopedia of Philosophy](https://plato.stanford.edu/entries/imprecise-probabilities/)
   - [Interpretations of Probability - Stanford Encyclopedia of Philosophy](https://plato.stanford.edu/entries/probability-interpret/)
  
- **`Lecture 3: Possibility Theory`** introduces possibility theory, a close relative of probability theory rooted in the theory of belief functions. We will explore how it differs from probability through concepts such as basic belief assignments, possibility and necessity values, and their interpretations. The lecture covers key perspectives on possibility theory—from the theory of surprise to flexible linguistic constraints, comparative possibility, and Baconian probabilities. We will also examine special cases of possibility distributions, their links to imprecise probability models, and how they support reasoning and decision-making. Finally, we discuss when possibility theory is needed, particularly in machine learning, and how to learn possibility models from data or expert input using principles like minimal specificity and conjunctive combination.

   <em>Lecture notes: [Slides](lecture-03/lecture-03-possibility-theory.pdf)</em>

   <em>Recommended reading:</em>
   - [Possibility Theory and Statistical Reasoning](https://www.irit.fr/~Didier.Dubois/Papers0804/D_CSDA06.pdf) by Didier Dubois (2006)
   - [Possibility Theory and its Applications: Where Do we Stand ?](https://www.irit.fr/publis/ADRIA/papersDDUBOIS/possibility-Encyclo.pdf) by Didier Dubois and Henri Prade (2014)
   - [Possibilistic Inferential Models: A Review](https://arxiv.org/pdf/2507.09007) by Ryan Martin (2025)

- **`Lecture 4: Belief Function Theory`** introduces belief function theory, a framework that generalizes both probability and possibility theories. We will cover the concept of basic belief assignments (and their link to cooperative games), belief and plausibility measures, and methods for computing lower and upper expectations, including Choquet integration. Different interpretations of the theory will be discussed, from Dempster’s multi-valued mappings to Shafer’s theory of evidence and Smets’ transferable belief model. We will also explore Dempster’s rule for information fusion and conditioning, the inverse Möbius transformation, and applications of belief functions in machine learning.

   <em>Lecture notes: [Slides](lecture-04/lecture-04-belief-function.pdf)</em>

   <em>Recommended reading:</em>
   - [Decision-Making with Belief Functions: a Review](https://arxiv.org/pdf/1808.05322) by T. Denœux (2019)


- **`Lecture 5: Convex Sets of Probabilities`** explores credal sets—convex sets of probabilities—as a unifying framework for imprecise probability models. We will study examples and characterizations of credal sets, and learn how to compute lower and upper probabilities and expectations through envelope functions. Key topics include marginal and conditional credal sets, robust Bayesian inference, and inference via the Generalised Bayes Rule (GBR). We will also discuss different notions of independence, and conclude with recent advances in credal-set methods for machine learning.

   <em>Lecture notes: [Slides](lecture-05/lecture-05-convex-sets-of-probabilities.pdf)</em>

   <em>Recommended reading:</em>
   - [Introduction to the Theory of Sets of Probabilities](https://www.cs.cmu.edu/~qbayes/Tutorial/quasi-bayesian.html) by Fabio Cozman
   - [Introduction to the Theory of Imprecise Probability](https://pure.tue.nl/ws/portalfiles/portal/356224229/978-3-030-83640-5_3.pdf) by Erik Quaeghebeur
   - [SIPTA School 2024: Introduction to Imprecise Probabilities](https://www.youtube.com/watch?v=gyDqpSY5B5s) by Erik Quaeghebeur

- **`Lecture 6: Decision Making under Imprecision`** How should we make decisions when probabilities are uncertain or incomplete? This lecture begins with a review of classical decision theory and then explores decision-making with imprecise probabilities, supported by real-world examples. We introduce key imprecise decision rules—such as maximality, E-admissibility, Γ-maximin, and interval dominance—and show how they provide more robust choices under ambiguity. Finally, we connect these ideas to modern machine learning, where imprecise decision-making plays an important role in building safer and more trustworthy AI systems.

  <em>Lecture notes: [Slides](lecture-06/lecture-06-decision-making-under-imprecision.pdf)</em>

   <em>Recommended reading:</em>
   - [Decision Making under Uncertainty using Imprecise Probabilities](https://arxiv.org/abs/1807.03705) by Matthias C. M. Troffaes
   - [SIPTA School 2024: Decisions](https://www.youtube.com/watch?v=3P8eMHtW8Sk) by Matthias C.M. Troffaes

### Part II:  Imprecise Probability in Machine Learning

- **`Lecture 7: Imprecise Classification and Regression`** explores how imprecise probability can improve classification and regression in machine learning. We discuss why standard models often fall short—showing overconfidence, vulnerability to adversarial examples, and lack of robustness—and how imprecise probability offers a principled way to address these issues. Finally, we look at concrete examples of machine learning models that have been extended with imprecise probability to make their predictions more reliable.

   <em>Lecture notes: [Slides](lecture-07/lecture-07-imprecise-classification-and-regression.pdf)</em>

   <em>Recommended reading:</em>
   - [The Naïve Credal Classifier](https://www.sciencedirect.com/science/article/abs/pii/S0378375801002014) by Marco Zaffalon
   - [Statistical modeling under partial identification: Distinguishing three types of identification regions in regression analysis with interval data](https://www.sciencedirect.com/science/article/pii/S0888613X14001145) by Georg Schollmeyer and Thomas Augustin (IJAR 2015)
   - [Neural network model for imprecise regression with interval dependent variables](https://www.sciencedirect.com/science/article/pii/S0893608023000680) by Krasymyr Tretiak, Georg Schollmeyer, and Scott Ferson (Neural Networks 2023)

- **`Lecture 8: Uncertainty Quantification`** introduces uncertainty quantification in machine learning. We discuss why it matters, how to distinguish and measure different types of uncertainty (aleatoric, epistemic, and total), and what properties good measures should have. We then examine common approaches, their limitations—especially in capturing epistemic uncertainty—and the challenges of building a universal framework. Finally, we look at practical applications of uncertainty quantification in modern ML.

   <em>Lecture notes: [Slides](lecture-08/lecture-08-uncertainty-quantification.pdf)</em>

   <em>Recommended reading:</em>
   - [Aleatoric and epistemic uncertainty in machine learning: an introduction to concepts and methods](https://arxiv.org/abs/1910.09457) by Hüllermeier, E. and Waegeman, W
   - [Quantification of Credal Uncertainty in Machine Learning: A Critical Analysis and Empirical Comparison](https://proceedings.mlr.press/v180/hullermeier22a.html) by Hüllermeier, E., Destercke, S., and Shaker, M.H.
   - [Integral Imprecise Probability Metrics](https://arxiv.org/abs/2505.16156) by Siu Lun (Alan) Chau, Michele Caprio, and Krikamol Muandet

- **`Lecture 9: Conformal Prediction and Calibration`** introduces conformal prediction, a framework for distribution-free uncertainty quantification that works with almost any machine learning model. We cover the basics of the method, its connections to calibration and imprecise probability, and how these ideas are used to improve the trustworthiness of modern ML systems.

   <em>Lecture notes: [Slides](lecture-09/lecture-09-conformal-prediction-and-calibration.pdf)</em>

   <em>Recommended reading:</em>
   - [A Gentle Introduction to Conformal Prediction and Distribution-Free Uncertainty Quantification](https://arxiv.org/abs/2107.07511) by Anastasios N. Angelopoulos and Stephen Bates
   - [A Tutorial on Conformal Prediction](https://jmlr.org/papers/v9/shafer08a.html) by Glenn Shafer and Vladimir Vovk

- **`Lecture 10: Lecture 10: Reflections, Open Problems, and Outlook`** explores how imprecise probability can be applied to modern machine learning, including deep learning, foundation models, large language models, fine-tuning, and generative AI. We discuss its potential to improve reliability and robustness in these areas, as well as the key challenges of adopting it in large-scale applications. It also asks whether imprecise probability can help address key societal concerns at the intersection of AI and society, such as fairness, privacy, ethics, and safety. We will explore important use cases that demonstrate its potential benefits in tackling these challenges.

   <em>Lecture notes: [Slides](lecture-10/lecture-10-reflections-open-problems-and-outlook.pdf)</em>
   
- **`Lecture 11: Project and use case presentation`**

## Course Project

The course project gives students a chance to apply what they've learned to a problem that interests them. After completing Part I, students will form groups of up to two people and choose a real-world problem to solve. Each group will present the final project to the class at the end of Part II.

## Logistic

- Lecture: Friday, 10 a.m. to 12 p.m., TBA
- Exercise: Friday, 12 p.m. to 2 p.m., TBA
- Location: TBA
- Exam dates: TBA

## Course Schedule

- TBA

## Useful Resources

Additional resources related to this course are listed in [`references.md`](references.md). 

If you are aware of any relevant resources that should be included (e.g., your own work), please feel free to submit a pull request or contact me directly by [`email`](mailto:muandet@cispa.de?subject=IPML:%20Missing%20Resources).
