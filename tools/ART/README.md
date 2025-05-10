# Adversarial Robustness Toolbox

## Tool description

The Adversarial Robustness Toolbox (ART) is a Python framework that provides a comprehensive suite of attacks, metrics, and defenses designed to enhance the security of machine learning (ML) models. Originally developed by IBM, it is widely regarded as a standard in ML security.

ART includes a vast range of adversarial attacks, covering evasion, poisoning, model extraction, and inference attacks. Its defense mechanisms are categorized into four types:

Detector-based defenses, which identify potential attacks,

Pre-processing defenses, which act on inputs before they reach the model,

Post-processing defenses, which operate after a model has made a prediction, and

Training defenses, which are applied during model training to improve robustness.

The primary advantage of ART is its extensive collection of adversarial tools, making it a powerful resource for ML security research. While it may pose a learning curve for those unfamiliar with machine learning, its versatility and robustness make it a valuable asset for enhancing model security.

## Notebooks

### Art_attack_database_reconstruction.ipynb

This example is based in     -     - [attack_database_reconstruction.ipynb](https://github.com/Trusted-AI/adversarial-robustness-toolbox/blob/main/notebooks/attack_database_reconstruction.ipynb). In it we will try to reconstruct the training dataset of a given model with and without defences.

## Tooling

- **Attacks**
  - **Evasion:** Techniques that generate adversarial examples to mislead models into making incorrect predictions.
    - [Adversarial Patch](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#adversarial-patch)    - [Adversarial Patch - Numpy](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#adversarial-patch-numpy)
    - [Adversarial Patch - PyTorch](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#adversarial-patch-pytorch)
    - [Adversarial Patch - TensorFlowV2](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#adversarial-patch-tensorflowv2)
    - [Adversarial Texture - PyTorch](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#adversarial-texture-pytorch)
    - [Auto Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#auto-attack)
    - [Auto Projected Gradient Descent (Auto-PGD)](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#auto-projected-gradient-descent-auto-pgd)
    - [Auto Conjugate Gradient (Auto-CG)](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#auto-conjugate-gradient-auto-cg)
    - [Boundary Attack / Decision-Based Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#boundary-attack-decision-based-attack)
    - [Brendel and Bethge Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#brendel-and-bethge-attack)
    - [Carlini and Wagner L_0 Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#carlini-and-wagner-l-0-attack)
    - [Carlini and Wagner L_2 Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#carlini-and-wagner-l-2-attack)
    - [Carlini and Wagner L_inf Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#carlini-and-wagner-l-inf-attack)
    - [Carlini and Wagner ASR Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#carlini-and-wagner-asr-attack)
    - [Composite Adversarial Attack - PyTorch](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#composite-adversarial-attack-pytorch)
    - [Decision Tree Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#decision-tree-attack)
    - [DeepFool](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#deepfool)
    - [DPatch](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#dpatch)
    - [RobustDPatch](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#robustdpatch)
    - [Elastic Net Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#elastic-net-attack)
    - [Fast Gradient Method (FGM)](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#fast-gradient-method-fgm)
    - [Feature Adversaries - Numpy](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#feature-adversaries-numpy)
    - [Feature Adversaries - PyTorch](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#feature-adversaries-pytorch)
    - [Feature Adversaries - TensorFlow](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#feature-adversaries-tensorflow)
    - [Frame Saliency Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#frame-saliency-attack)
    - [Geometric Decision Based Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#geometric-decision-based-attack)
    - [GRAPHITE - Blackbox](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#graphite-blackbox)
    - [GRAPHITE - Whitebox - PyTorch](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#graphite-whitebox-pytorch)
    - [High Confidence Low Uncertainty Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#high-confidence-low-uncertainty-attack)
    - [HopSkipJump Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#hopskipjump-attack)
    - [Imperceptible ASR Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#imperceptible-asr-attack)
    - [Imperceptible ASR Attack - PyTorch](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#imperceptible-asr-attack-pytorch)
    - [Basic Iterative Method (BIM)](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#basic-iterative-method-bim)
    - [Projected Gradient Descent (PGD)](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#projected-gradient-descent-pgd)
    - [Projected Gradient Descent (PGD) - Numpy](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#projected-gradient-descent-pgd-numpy)
    - [Projected Gradient Descent (PGD) - PyTorch](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#projected-gradient-descent-pgd-pytorch)
    - [Projected Gradient Descent (PGD) - TensorFlowV2](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#projected-gradient-descent-pgd-tensorflowv2)
    - [LaserAttack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#laserattack)
    - [LowProFool](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#lowprofool)
    - [NewtonFool](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#newtonfool)
    - [Malware Gradient Descent - TensorFlow](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#malware-gradient-descent-tensorflow)
    - [Over The Air Flickering Attack - PyTorch](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#over-the-air-flickering-attack-pytorch)
    - [PixelAttack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#pixelattack)
    - [ThresholdAttack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#thresholdattack)
    - [Jacobian Saliency Map Attack (JSMA)](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#jacobian-saliency-map-attack-jsma)
    - [Shadow Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#shadow-attack)
    - [ShapeShifter Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#shapeshifter-attack)
    - [Sign-OPT Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#sign-opt-attack)
    - [Simple Black-box Adversarial Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#simple-black-box-adversarial-attack)
    - [Spatial Transformations Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#spatial-transformations-attack)
    - [Square Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#square-attack)
    - [Targeted Universal Perturbation Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#targeted-universal-perturbation-attack)
    - [Universal Perturbation Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#universal-perturbation-attack)
    - [Virtual Adversarial Method](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#virtual-adversarial-method)
    - [Wasserstein Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#wasserstein-attack)
    - [Zeroth-Order Optimization (ZOO) Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/evasion.html#zeroth-order-optimization-zoo-attack)
  - **Extraction:** Methods aiming to duplicate or steal model functionality or parameters.

    - [Copycat CNN](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/extraction.html#copycat-cnn)
    - [Functionally Equivalent Extraction](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/extraction.html#functionally-equivalent-extraction)
    - [Knockoff Nets](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/extraction.html#knockoff-nets)
  - **Inference:** Attacks that seek to infer sensitive information about the training data.
    - **Attribute Inference Attack**: Recover missing or sensitive attributes of input data from a trained model. The attacker has partial knowledge about the dataset and queries the model to infer unknown attributes, which can expose personal data such as race, income, or medical conditions.
      - [Attribute Inference Baseline](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/inference/attribute_inference.html#attribute-inference-baseline)
      - [Attribute Inference Black-Box](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/inference/attribute_inference.html#attribute-inference-black-box)
      - [Attribute Inference Membership](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/inference/attribute_inference.html#attribute-inference-membership)
      - [Attribute Inference Base Line True Label](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/inference/attribute_inference.html#attribute-inference-base-line-true-label)
      - [Attribute Inference White-Box Lifestyle Decision-Tree](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/inference/attribute_inference.html#attribute-inference-white-box-lifestyle-decision-tree)
      - [Attribute Inference White-Box Decision-Tree](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/inference/attribute_inference.html#attribute-inference-white-box-decision-tree)

    - **Membership Inference Attack**: Determine whether a specific data sample was part of the model’s training dataset. Attackers exploit differences in confidence scores or output distributions to infer if a record was included, which is particularly concerning for sensitive data like medical records.
      - [Membership Inference Black-Box](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/inference/membership_inference.html#membership-inference-black-box)
      - [Membership Inference Black-Box Rule-Based](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/inference/membership_inference.html#membership-inference-black-box-rule-based)
      - [Membership Inference Label-Only - Decision Boundary](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/inference/membership_inference.html#membership-inference-label-only-decision-boundary)
      - [Membership Inference Label-Only - Gap Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/inference/membership_inference.html#membership-inference-label-only-gap-attack)
      - [Shadow Models](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/inference/membership_inference.html#shadow-models)

    - **Model Inversion Attack**: Reconstruct original training data from a trained model. The attacker optimizes adversarial inputs until they resemble real data, which can expose sensitive images, biometric data, or text samples.
      - [Model Inversion MIFace](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/inference/model_inversion.html#model-inversion-miface)
    - **Reconstruction Attack**: Reconstruct the entire training dataset (or a portion of it) from the model’s responses. This is more powerful than model inversion, as it tries to recover multiple samples using gradients, shadow models, or optimization techniques.
      - [Database Reconstruction](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/inference/reconstruction.html#database-reconstruction)

  - **Poisoning:** Involves injecting malicious data into the training set to corrupt the model's performance.
    - [Backdoor Attack DGM ReD](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/poisoning.html#backdoor-attack-dgm-red)
    - [Backdoor Attack DGM Trail](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/poisoning.html#backdoor-attack-dgm-trail)
    - [Adversarial Embedding Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/poisoning.html#adversarial-embedding-attack)
    - [Backdoor Poisoning Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/poisoning.html#backdoor-poisoning-attack)
    - [Hidden Trigger Backdoor Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/poisoning.html#hidden-trigger-backdoor-attack)
    - [Bullseye Polytope Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/poisoning.html#bullseye-polytope-attack)
    - [Clean Label Backdoor Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/poisoning.html#clean-label-backdoor-attack)
    - [Feature Collision Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/poisoning.html#feature-collision-attack)
    - [Gradient Matching Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/poisoning.html#gradient-matching-attack)
    - [Poisoning SVM Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/poisoning.html#poisoning-svm-attack)
    - [Sleeper Agent Attack](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/attacks/poisoning.html#sleeper-agent-attack)

- **Defenses**
  - **Detector:** Mechanisms that identify adversarial inputs before they affect the model.
    - **Evasion Detection:** Detects inputs crafted to evade model predictions.
      - [Base Class](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/detector_evasion.html#base-class)
      - [Binary Input Detector](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/detector_evasion.html#binary-input-detector)
      - [Binary Activation Detector](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/detector_evasion.html#binary-activation-detector)
      - [Subset Scanning Detector](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/detector_evasion.html#subset-scanning-detector)
    - **Poison Detection:** Identifies and filters out malicious data from the training set.
      - [Base Class](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/detector_poisoning.html#base-class)
      - [Activation Defence](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/detector_poisoning.html#activation-defence)
      - [Data Provenance Defense](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/detector_poisoning.html#data-provenance-defense)
      - [Reject on Negative Impact (RONI) Defense](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/detector_poisoning.html#reject-on-negative-impact-roni-defense)
      - [Spectral Signature Defense](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/detector_poisoning.html#spectral-signature-defense)    
  - **Postprocessor:** Applies transformations to model outputs to mitigate the effects of adversarial attacks.
    - [Base Class Postprocessor](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/postprocessor.html#base-class-postprocessor)
    - [Class Labels](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/postprocessor.html#class-labels)
    - [Gaussian Noise](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/postprocessor.html#gaussian-noise)
    - [High Confidence](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/postprocessor.html#high-confidence)
    - [Reverse Sigmoid](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/postprocessor.html#reverse-sigmoid)
    - [Rounded](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/postprocessor.html#rounded)
  - **Preprocessor:** Processes input data before feeding it into the model to neutralize adversarial perturbations.
    - [Base Class Preprocessor](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/preprocessor.html#base-class-preprocessor)
    - [CutMix](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/preprocessor.html#cutmix)
    - [CutMix - PyTorch](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/preprocessor.html#cutmix-pytorch)
    - [CutMix - TensorFlowV2](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/preprocessor.html#cutmix-tensorflowv2)
    - [Cutout](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/preprocessor.html#cutout)
    - [Cutout - PyTorch](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/preprocessor.html#cutout-pytorch)
    - [Cutout - TensorFlowV2](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/preprocessor.html#cutout-tensorflowv2)
    - [Feature Squeezing](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/preprocessor.html#feature-squeezing)
    - [Gaussian Data Augmentation](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/preprocessor.html#gaussian-data-augmentation)
    - [InverseGAN](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/preprocessor.html#inversegan)
    - [DefenseGAN](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/preprocessor.html#defensegan)
    - [JPEG Compression](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/preprocessor.html#jpeg-compression)
    - [Label Smoothing](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/preprocessor.html#label-smoothing)
    - [Mixup](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/preprocessor.html#mixup)
    - [Mixup - PyTorch](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/preprocessor.html#mixup-pytorch)
    - [Mixup - TensorFlowV2](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/preprocessor.html#mixup-tensorflowv2)
    - [Mp3 Compression](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/preprocessor.html#mp3-compression)
    - [PixelDefend](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/preprocessor.html#pixeldefend)
    - [Resample](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/preprocessor.html#resample)
    - [Spatial Smoothing](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/preprocessor.html#spatial-smoothing)
    - [Spatial Smoothing - PyTorch](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/preprocessor.html#spatial-smoothing-pytorch)
    - [Spatial Smoothing - TensorFlow v2](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/preprocessor.html#spatial-smoothing-tensorflow-v2)
    - [Thermometer Encoding](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/preprocessor.html#thermometer-encoding)
    - [Total Variance Minimization](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/preprocessor.html#total-variance-minimization)
    - [Video Compression](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/preprocessor.html#video-compression)
  - **Trainer:** Incorporates strategies during model training to enhance robustness against adversarial attacks.
    - [Base Class Trainer](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/trainer.html#base-class-trainer)
    - [Adversarial Training](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/trainer.html#adversarial-training)
    - [Adversarial Training Madry PGD](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/trainer.html#adversarial-training-madry-pgd)
    - [Adversarial Training Adversarial Weight Perturbation (AWP) - PyTorch](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/trainer.html#adversarial-training-adversarial-weight-perturbation-awp-pytorch)
    - [Adversarial Training Oracle Aligned Adversarial Training (OAAT) - PyTorch](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/trainer.html#adversarial-training-oracle-aligned-adversarial-training-oaat-pytorch)
    - [Adversarial Training TRADES - PyTorch](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/trainer.html#adversarial-training-trades-pytorch)
    - [Base Class Adversarial Training Fast is Better than Free](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/trainer.html#base-class-adversarial-training-fast-is-better-than-free)
    - [Adversarial Training Fast is Better than Free - PyTorch](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/trainer.html#adversarial-training-fast-is-better-than-free-pytorch)
    - [Adversarial Training Certified - PyTorch](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/trainer.html#adversarial-training-certified-pytorch)
    - [Adversarial Training Certified Interval Bound Propagation - PyTorch](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/trainer.html#adversarial-training-certified-interval-bound-propagation-pytorch)
    - [DP - InstaHide Training](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/trainer.html#dp-instahide-training)
  - **Transformer:** Modifies either the model or data representations to defend against specific attack vectors.
    - **Evasion Transformer:** Adjusts model parameters to reduce susceptibility to evasion attacks.
      - [Defensive Distillation](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/transformer_evasion.html#defensive-distillation)
    - **Poisoning Transformer:** Alters data representations to mitigate the impact of poisoning attacks.
      - [Neural Cleanse](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/transformer_poisoning.html#neural-cleanse)
      - [STRIP](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/defences/transformer_poisoning.html#strip)
