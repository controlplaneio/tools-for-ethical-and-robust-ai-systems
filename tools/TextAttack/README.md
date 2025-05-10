# TextAttack

## Tool description

Python library for adversarial attacks against language models (NLP)

## Notebooks

### TextAttack.ipynb

we run seq2sick (black-box) against T5 fine-tuned for English-German translation. Seq2Sick is an adversarial attack method designed for sequence-to-sequence (seq2seq) models, which are commonly used in tasks like machine translation, text summarization, and speech-to-text. The goal of the Seq2Sick attack is to subtly modify input sequences (adversarial perturbations) to cause the model to produce incorrect or undesired outputs, while keeping the input perturbation minimal and imperceptible.

## Tooling

- Attacks
  - **alzantot**: Untargeted {Classification, Entailment} attack using counter-fitted word embedding swap with a Genetic Algorithm, measuring percentage of words perturbed, language model perplexity, and word embedding distance. From "Generating Natural Language Adversarial Examples" (Alzantot et al., 2018).
  - **bae**: BERT masked language model transformation attack using greedy word importance ranking (WIR). Measures cosine similarity using Universal Sentence Encoder (USE). From "BAE**: BERT-based Adversarial Examples for Text Classification" (Garg & Ramakrishnan, 2019).
  - **bert-attack**: BERT-based adversarial attack using masked token prediction with subword expansion. Measures USE cosine similarity and number of words perturbed. From "BERT-ATTACK: Adversarial Attack Against BERT Using BERT" (Li et al., 2020).
  - **checklist**: Invariance testing attack that manipulates entity names through contract, extend, and substitute methods. Measures checklist distance. From "Beyond Accuracy: Behavioral Testing of NLP Models with CheckList" (Ribeiro et al., 2020).
  - **clare**: Contextualized perturbation attack for classification and entailment, leveraging RoBERTa masked prediction for token swap, insert, and merge. Uses greedy search. From "Contextualized Perturbation for Textual Adversarial Attack" (Li et al., 2020).
  - **deepwordbug**: Character-level perturbation attack using insertion, deletion, swap, and substitution techniques. Uses greedy-WIR ranking. From "Black-box Generation of Adversarial Text Sequences to Evade Deep Learning Classifiers" (Gao et al., 2018).
  - **faster-alzantot**: A modified, faster version of Alzantot's genetic algorithm, from "Certified Robustness to Adversarial Word Substitutions" (Jia et al., 2019).
  - **hotflip (word swap)**: White-box attack using gradient-based word swap with beam search. Measures word embedding cosine similarity and part-of-speech match. From "HotFlip**: White-Box Adversarial Examples for Text Classification" (Ebrahimi et al., 2017).
  - **iga**: Improved genetic algorithm-based word substitution. Measures word perturbation percentage and embedding distance. From "Natural Language Adversarial Attacks and Defenses in Word Level" (Wang et al., 2019).
  - **input-reduction**: Greedy attack reducing input by deleting words while maintaining model prediction. From "Pathologies of Neural Models Make Interpretation Difficult" (Feng et al., 2018).
  - **kuleshov**: Word swap attack measuring thought vector encoding cosine similarity and language model probability. Uses greedy search. From "Adversarial Examples for Natural Language Classification Problems" (Kuleshov et al., 2018).
  - **pruthi**: Simulates typos using character swap, deletion, insertion, and keyboard-based substitutions. Uses greedy search. From "Combating Adversarial Misspellings with Robust Word Recognition" (Pruthi et al., 2019).
  - **pso**: Particle Swarm Optimization (PSO) attack using HowNet word swaps. From "Word-level Textual Adversarial Attacking as Combinatorial Optimization" (Zang et al., 2020).
  - **pwws**: Greedy attack ranking words based on saliency and WordNet-based synonym swaps. From "Generating Natural Language Adversarial Examples through Probability Weighted Word Saliency" (Ren et al., 2019).
  - **textbugger**: Black-box adversarial text attack using character manipulations like insertion, deletion, and swap. Uses greedy-WIR. From "TextBugger**: Generating Adversarial Text Against Real-world Applications" (Li et al., 2018).
  - **textfooler**: Greedy-WIR attack using counter-fitted word embedding swaps. Measures word embedding distance, part-of-speech match, and USE cosine similarity. From "Is BERT Really Robust?" (Jin et al., 2019).
  - **morpheus**: Minimizes BLEU score by replacing words with inflections. Uses greedy search. From "It’s Morphin’ Time! Combating Linguistic Discrimination with Inflectional Perturbations" (Tan et al., 2020).
  - **seq2sick**: Black-box attack targeting sequence-to-sequence models. Uses counter-fitted word embeddings with greedy-WIR ranking. From "Seq2Sick: Evaluating the Robustness of Sequence-to-Sequence Models with Adversarial Examples" (Cheng et al., 2018).
