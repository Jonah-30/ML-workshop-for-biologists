# Machine Learning Workshop for Biologists

An intuition-first introduction to classical machine learning, designed and taught for wet-lab scientists with little to no ML background.

**Loscalzo Lab — Brigham & Women's Hospital / Harvard Medical School · Summer 2026**

Designed and Taught by Jonah Sandow

Special thanks to Dr. Hau Xu, Marianna Lamanna, and Dr. Joseph Loscalzo for project guidance.

---

## About this workshop

This is a hands-on workshop that teaches biologists and chemists how machine learning actually works. We build a clear mental picture of each concept before any math or code. Every idea starts with a plain-English problem and a picture, uses a consistent running example (predicting whether a patient is sick or healthy from a biomarker), and pairs slides with an annotated visual. The goal is that a beginner walks away able to explain *why* a model works, not just which library function to call.

Each session is a slide deck plus 2 companion Jupyter notebooks. There is one practice notebook with fill in the blanks and questions and then a solutions notebook. The notebooks can be run easily in google colab (https://colab.research.google.com/) or in an ide like vscode (but then the libraries must be downloaded).


<!-- Recruiter tip: drop a hero image here — one of your best annotated plots (e.g. the overfitting gap or the sigmoid). Replace the line below. -->
<img width="862" height="534" alt="Screenshot 2026-07-21 at 11 09 36 AM" src="https://github.com/user-attachments/assets/102685b1-1180-4f3b-9590-cbd423fdb5be" />

---

## Session 1 — Models and Overfitting

The full lifecycle of a model on a single running example, from a straight line to a regularized classifier.

- **What is a model** — an input-to-prediction rule the model *learns* from examples by shrinking its mistakes, rather than one written by hand. Weights / coefficients / β.
- **How a model learns** — the predict → measure the miss → nudge → repeat loop.
- **Loss functions** — scoring "how wrong" the model is in a single number; Mean Squared Error for regression.
- **Logistic regression** — going from predicting a number to predicting a category (sick / healthy).
- **The sigmoid** — squashing a line into an S-curve so outputs stay valid probabilities (0–1), with multiple features.
- **Thresholds** — turning a probability into a decision, and why the right cutoff depends on which mistake costs more.
- **Train / validation / test split** — why a score on training data is a lie, held-out data as the only honest measure, and Goodhart's Law in ML.
- **Overfitting** — memorizing noise instead of the pattern, and the train–validation gap as its signature.
- **Bias–variance tradeoff** — the two ways to be wrong: too simple (underfitting) vs. too complex (overfitting).
- **Regularization** — penalizing large coefficients to curb overfitting; Ridge (L2) vs. Lasso (L1) and automatic feature selection.

## Session 2 — Trees, Forests, and Boosting

Moving from linear models to tree-based methods and ensembles — still on the same medical-screening example.

- **Decision trees** — a chain of yes/no questions ending in a prediction; each split is one straight cut in feature space.
- **How a tree is built** — searching features and thresholds to best separate the classes, splitting until groups are pure.
- **Gini impurity** — the loss function trees minimize; intuition of a "cleaner split," no hand computation required.
- **Trees overfit** — a tree grown too deep memorizes individual patients instead of the general pattern.
- **Random forests** — don't trust one tree; grow many and let them vote so odd mistakes get outvoted.
- **Bagging** — giving each tree its own random resample of patients (drawn with replacement) so the trees differ.
- **Feature shuffling** — letting each split consider only a random subset of features, so strong features don't dominate every tree.
- **Gradient boosting** — building small trees sequentially, each one correcting the errors left by the last.
- **Forests vs. boosting** — independent-and-averaged vs. a chain that fixes the last tree; where each shines and how boosting is tuned.

---

## Repository structure

```
.
├── session-1-models-and-overfitting/
│   ├── session-1-slides.pdf
│   └──session-1-notebook-practice.ipynb
│   └──session-1-notebook-solutions.ipynb
├── session-2-trees-forests-boosting/
│   ├── session-2-slides.pdf
│   └──session-1-notebook-practice.ipynb
│   └──session-1-notebook-solutions.ipynb
├── assets/                # figures used in the README and slides
└── README.md
```

### Quick Links
* [View Session 1 Slides](./session-1-models-and-overfitting/session-1-slides.pdf)
* 
* [View Session 2 Slides](./session-2-trees-forests-boosting/session-2-slides.pdf)

---

*Built as teaching material for scientists new to machine learning. Feedback and questions welcome.*
