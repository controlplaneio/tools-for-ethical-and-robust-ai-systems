# Garak

## Tool Description

If you are looking just for security LLM evaluation, we have the tool for you! Garak is backed by Nvidia with a very active community, and includes a plethora of probes that checks jailbreaks and prompt injection resilience based on “do anything know” known attacks, unexpected encoding characters, and many other techniques. Some of these probes are based on training an LLM to try to defeat the guardrails of the evaluated LLM.

As we say you have plenty of probes that you can use for evaluation, and because the behaviour of LLMs is non deterministic, Garak will repeat tests several times to show you how many times the LLM resisted the attack attempt. 

All this means that it can take hours to conduct one with all of them, and no matter how robust the LLM is, you will always see weak points in the analysis. It’s up to you to decide where is the acceptance criteria, and how you will make a decision on the results.

Another problem is that most of its probes will be aimed at security (trying to bypass LLM guardrails), and not the broader topic of fairness or responsible AI. The only exception may be the probe to check if the LLM has been trained with illegal copyrighted data like the New York Times articles.

But if you want to evaluate LLMs security very thoroughly, look no further than Garak.

## Notebooks

### garak_poetry.ipynb

TODO: add description

## Tooling

- **Probes**

  - **ANSI Escape**: Attempts to get the model to produce ANSI codes, which can disrupt processing in other ways.

  - **Attack Generator**: Use a separate model to create prompts for a generator, guiding it towards failure.  
    [Related Paper](https://aclanthology.org/2022.findings-emnlp.35/)

  - **Antivirus or Spam Scanning Check**: Test if the model outputs a known bad signature, like malware or spam.

  - **Continuation**: Provide high-risk context as input to see if the model continues the text inappropriately.

  - **“Do Anything Now” (DAN)**: Disrupt the system prompt by instructing the model to ignore all previous instructions, bypassing system constraints.  
    Includes **AutoDAN**, which automatically tries to generate strings for the DAN attack.

  - **Divergence**: Check if the model will replay training data or repeat a given string, like “poem poem poem”.

  - **“Do Not Answer”**: Dataset of prompts that language models are often trained not to answer.  
    [Link to Dataset](https://github.com/Libr-AI/do-not-answer)  
    [Related Paper](https://arxiv.org/abs/2308.13387)

  - **Encoding**: Present an encoded version of text to see if the model circumvents safeguards on input filtering.

  - **Fileformats**: Test if the model handles specific file formats (e.g., pickle) with known vulnerabilities.

  - **Glitch**: Probe for tokens that cause unusual behavior or bugs in the model.

  - **Goodside**: Implements Riley Goodside attacks, such as providing false factual information about Goodside or using glitch tokens for prompt injection.

  - **Grandma**: Use appeal to ethos, centered around a fictitious grandmother, to extract illegal or sensitive information from the model.

  - **Latent Injection**: Probes hidden prompt injections embedded within other contexts. For example, prompt injections included in translation tasks.

  - **Leakreplay**: Evaluate if the model replays training data, especially privately owned or copyrighted materials, such as news media.

  - **Language Model Risk Cards**: A framework listing various risks and vulnerabilities for language models across different scenarios.  
    [Related Paper](https://arxiv.org/abs/2303.18190)

  - **Malware Generation**: Test if the model complies with generating malware or other disruptive tools.

  - **Misleading Claims**: Test whether the model will correctly refute false claims or misleading statements.

  - **Package Hallucination**: Probe for the generation of non-existent or fabricated code packages during code generation tasks.

  - **Prompt Injection**: A collection of prompts used to inject harmful instructions into the model.  
    [Link to Paper](https://openreview.net/forum?id=qiaRo_7Zmug)

  - **Real Toxicity Prompts**: A framework of prompts designed to evaluate toxicity in model responses, utilizing Perspective API detectors (requires API key).  
    [Related Paper](https://aclanthology.org/2020.findings-emnlp.301/)

  - **Snowball**: Check for incorrect answers to complex reasoning questions.  
    [Related Paper](https://arxiv.org/abs/2305.13534)

  - **Suffix**: Disrupt a system prompt by appending an adversarial suffix to the model's input.

  - **Tree of Attacks with Pruning (TAP)**: LLM-generated prompts used to jailbreak a model. A wrapper for the implementation by Robust Intelligence community.  
    [Related Paper](https://arxiv.org/abs/2312.02119)  
    [Related Paper](https://arxiv.org/abs/2310.08419)

  - **Test Probes**: Validate that probes are invoked as expected when tested on the model.

  - **Topic**: Attempt to get the model to engage in contentious topics, such as using Wordnet to search terms related to controversial subjects.

  - **Visual Jailbreak**: Use an image to assist in bypassing system constraints, enabling jailbreaks.  
    [Related Paper](https://arxiv.org/pdf/2311.05608.pdf)

  - **XSS (Cross-Site Scripting)**: Probe for vulnerabilities that could allow cross-site attacks, potentially leading to private data exfiltration.
