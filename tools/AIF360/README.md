# AIF360

## Tool description

AIF360 focuses exclusively on bias detection and mitigation.

It was developed by IBM and it was donated to the Linux Foundation AI & Data Foundation.

AIF360 has three main components. Firstly, it has estimators, which are Machine Learning models or libraries that are used to mitigate bias in some ways, they can apply, before training, in training or after training.

It contains metrics as well that can help us assess the model predictions, these are divided into two sub groups. Group metrics, that applies to subpopulations within the dataset or individual metrics which assess that similar individuals are treated similarly.

Lastly it has detectors, which identify subgroups that are favoured or discriminated against by our model.

Our experience with AIF360 was very positive, the documentation was broad and clear, it was easy to use and it is relatively lightweight. It is true that its purpose is very specific but also it is worth to say that there are not many tools that assess bias and discrimination and it is nice to have one as mature and as backed as this one.

## Notebooks

### AIF360_tutorial_bias_advertising.ipynb

In this example, we adapted one of the example notebooks that AIF360 had in its repo: [tutorial_bias_advertising.ipynb](https://github.com/Trusted-AI/AIF360/blob/main/examples/tutorial_bias_advertising.ipynb).

This tutorial shows how bias in advertising data can be discovered, measured and mitigated using AIF360.

## Tooling

- **Algorithms**
  - **Preprocessing:** Techniques applied before model training to mitigate bias in data.
    - **DisparateImpactRemover:** Edits feature values to enhance group fairness while preserving rank-ordering within groups.
    - **Learning Fair Representations (LFR):** Finds a latent representation that encodes data well but obfuscates information about protected attributes.
    - **Optimized Preprocessing:** Learns a probabilistic transformation that edits features and labels with constraints on group fairness, individual distortion, and data fidelity.
    - **Reweighing:** Assigns weights to examples in each (group, label) combination to ensure fairness before classification.
  - **Inprocessing:** Methods that incorporate fairness constraints into the model training process.
    - **Adversarial Debiasing:** Learns a classifier to maximize prediction accuracy while reducing an adversary's ability to determine the protected attribute from predictions.
    - **ARTClassifier:** Wraps an instance of an `art.classifiers.Classifier` to extend Transformer.
    - **GerryFairClassifier:** An algorithm for learning classifiers that are fair with respect to rich subgroups.
    - **MetaFairClassifier:** A meta-algorithm that takes the fairness metric as input and returns a classifier optimized with respect to it.
    - **Prejudice Remover:** Adds a discrimination-aware regularization term to the learning objective to mitigate bias.
    - **Exponentiated Gradient Reduction:** An approach for fair classification that reduces the problem to a sequence of cost-sensitive classification problems.
    - **Grid Search Reduction:** Performs a grid search over classifier parameters to find models that balance fairness and accuracy.
  - **Postprocessing:** Techniques applied after model training to adjust predictions for fairness.
    - **Calibrated Equalized Odds Postprocessing:** Optimizes over calibrated classifier score outputs to find probabilities with which to change output labels with an equalized odds objective.
    - **Equalized Odds Postprocessing:** Solves a linear program to find probabilities with which to change output labels to optimize equalized odds.
    - **Reject Option Classification:** Gives favorable outcomes to unprivileged groups and unfavorable outcomes to privileged groups in a confidence band around the decision boundary with the highest uncertainty.
    - **Deterministic Reranking:** A collection of algorithms for constructing fair ranked candidate lists.

- **Metrics**
  - **Dataset Metrics:** Assess fairness at the dataset level.
    - **AI Fairness 360**
    - **DatasetMetric:** Computes metrics based on a single `StructuredDataset`.
    - **BinaryLabelDatasetMetric:** Computes metrics based on a single `BinaryLabelDataset`.
  - **Classification Metrics:** Evaluate fairness in classification tasks.
    - **AI Fairness 360**
    - **ClassificationMetric:** Computes metrics based on two `BinaryLabelDatasets`, typically the original and predicted datasets.
    - **MDSSClassificationMetric:** Utilizes bias subset scanning to identify bias in predictive models using subset scanning techniques.
  - **Sample Distortion Metrics:** Measure distortions introduced during preprocessing.
    - **SampleDistortionMetric:** Computes metrics based on two `StructuredDatasets` to assess the impact of preprocessing transformations.
  - **Utility Functions:** Provide helper functions for metric computations.
    - **compute_boolean_conditioning_vector:** Computes a boolean conditioning vector based on specified conditions.
    - **compute_num_instances:** Calculates the number of instances conditioned on protected attributes.
    - **compute_num_pos_neg:** Determines the number of positive or negative instances, optionally conditioned on protected attributes.
    - **compute_num_TF_PN:** Computes the number of true/false positives/negatives, optionally conditioned on protected attributes.
    - **compute_num_gen_TF_PN:** Calculates the number of generalized true/false positives/negatives with optional conditioning on protected attributes.
    - **compute_distance:** Computes element-wise distances between two sets of vectors.
