# Adversarial Robustness Toolbox

## Tool description

Adversarial Robustness Toolbox (ART for friends and family) is a python framework with a huge collection of attacks, metrics and defenses targeted against Machine Learning models.It was originally developed by IBM and it’s considered a standard in ML security. 

The wide range of attacks is massive and goes from evasion attacks to poisoning, extraction and inference attacks.

The defences cover, detector based defences, which detects attacks, pre-processing defences that act before the input reaches the model, post-processing defences that on the contrary acts after the model made a prediction and training defences that are applied during training.

As an example, when we were experimenting with the tool we ran a database reconstruction attack. In this scenario, the attackers had access to parts of the training dataset and were able to reconstruct it totally. We repeated the attack after applying a training defense (private gaussian naive bayes classifier) after which we weren’t able to reconstruct the dataset.

The main benefit of this tool is the sheer amount of resources it possesses in form of attacks, metrics and defences. It can be a bit challenging to people not very familiar with machine learning but it definitely compensates that difficulty with its versatility and power.

## Notebooks

### Art_attack_database_reconstruction.ipynb

This example is based in [attack_database_reconstruction.ipynb](https://github.com/Trusted-AI/adversarial-robustness-toolbox/blob/main/notebooks/attack_database_reconstruction.ipynb). In it we will try to reconstruct the training dataset of a given model with and without defences.

## Tooling

- **Attacks**
  - **Evasion:** Techniques that generate adversarial examples to mislead models into making incorrect predictions.
    - **Adversarial Patch:** Generates a patch that, when applied to images or videos, causes misclassification.
    - **Projected Gradient Descent (PGD):** Iteratively perturbs input data to find adversarial examples within a specified norm.
    - **Carlini and Wagner (C&W) Attack:** Optimizes perturbations to minimize distortion while causing misclassification.
  - **Extraction:** Methods aiming to duplicate or steal model functionality or parameters.
    - **Functionally Equivalent Extraction:** Reconstructs a functionally equivalent model by leveraging the original model's predictions.
    - **Copycat CNN:** Trains a substitute model to mimic the target model's behavior using synthetic data.
  - **Inference:** Attacks that seek to infer sensitive information about the training data.
    - **Attribute Inference:** Attempts to deduce sensitive attributes of input data.
      - **Attribute Inference Black-Box:** Infers attributes without access to model internals, relying solely on model outputs.
    - **Membership Inference:** Determines whether specific data points were part of the model's training set.
      - **Membership Inference Black-Box:** Assesses membership using only the model's output probabilities.
    - **Model Inversion:** Reconstructs input data from model outputs, potentially revealing sensitive information.
      - **Model Inversion Attack:** Generates representative inputs that match a given output, effectively inverting the model's function.
  - **Poisoning:** Involves injecting malicious data into the training set to corrupt the model's performance.
    - **Backdoor Attack:** Embeds hidden triggers in the model that cause misclassification when activated.
    - **Adversarial Embedding:** Trains the model with additional objectives to create non-differentiable representations between poisoned and clean data.

- **Defenses**
  - **Detector:** Mechanisms that identify adversarial inputs before they affect the model.
    - **Evasion Detection:** Detects inputs crafted to evade model predictions.
    - **Poison Detection:** Identifies and filters out malicious data from the training set.
  - **Postprocessor:** Applies transformations to model outputs to mitigate the effects of adversarial attacks.
    - **Gaussian Noise Addition:** Adds noise to outputs to obscure potential adversarial signals.
  - **Preprocessor:** Processes input data before feeding it into the model to neutralize adversarial perturbations.
    - **Feature Squeezing:** Reduces the complexity of input data to limit adversarial manipulation.
  - **Trainer:** Incorporates strategies during model training to enhance robustness against adversarial attacks.
    - **Adversarial Training:** Trains the model on adversarial examples to improve resilience.
  - **Transformer:** Modifies either the model or data representations to defend against specific attack vectors.
    - **Evasion Transformer:** Adjusts model parameters to reduce susceptibility to evasion attacks.
    - **Poisoning Transformer:** Alters data representations to mitigate the impact of poisoning attacks.
