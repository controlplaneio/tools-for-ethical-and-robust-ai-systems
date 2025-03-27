# InspectAI

## Tool description

InspectAI is a benchmark for LLM models with many different types of evaluations, only two related to security: Harm and Hazardous knowledge.

It’s created by OpenUK which is a UK-based not-for-profit organisation dedicated to promoting and supporting open technology.

It covers coding tasks, AI assistants benchmarks, cybersecurity tasks, mathematical tasks and knowledge tasks. One key and unique aspect of inspectAI is that it can assess performance and accuracy at the same time as assessing the safety and security of the system, this comes handy as it is understood than in many occasions there is a trade off between security and safety and accuracy and model performance (for example, I can be very safe about my model not responding on how to build a thermonuclear weapon if I don’t teach it any physics but at the expense of not performing well at all in science tasks).

Another benefit of inspectAI is that it’s very simple and lightweight since it doesn’t implement adversarial attacks, but it shouldn’t be the tool of choice if a more in-depth and powerful assessment of the model is required.

Lastly, the result presentation is really user friendly, it generates some logs that can be exposed through an user interface locally.

## Notebooks

### InspectAIOpenUK.ipynb

In this example, we run `inspect_evals/agentharm` eval against `openai/gpt-4o-2024-08-06` and save the results to a drive account. The results can be downloaded and inspected running `inspect view` in a directory in which there is the `logs` folder that contains the results.

## Tooling

- **Evals**
  - **Coding**
    - **HumanEval:** Evaluating Large Language Models Trained on Code  
      - Measures the functional correctness of synthesizing programs from docstrings.
    - **MBPP:** Mostly Basic Python Problems  
      - Measures the ability to synthesize short Python programs from natural language descriptions.
    - **SWE-bench Verified:** Resolving Real-World GitHub Issues  
      - Software engineering problems drawn from real GitHub issues and corresponding pull requests across 12 popular Python repositories.
    - **SciCode:** A Research Coding Benchmark Curated by Scientists  
      - Tests the ability of language models to generate code for scientific research problems across mathematics, physics, chemistry, biology, and materials science.
    - **DS-1000:** A Natural and Reliable Benchmark for Data Science Code Generation  
      - Code generation benchmark with a thousand data science problems spanning seven Python libraries.
    - **BigCodeBench:** Benchmarking Code Generation with Diverse Function Calls and Complex Instructions  
      - Python coding benchmark with 1,140 diverse questions drawing on numerous Python libraries.
    - **APPS:** Automated Programming Progress Standard  
      - Evaluates model performance on Python programming tasks across three difficulty levels, covering 10,000 programming tasks.
    - **ClassEval:** A Manually-Crafted Benchmark for Evaluating LLMs on Class-level Code Generation  
      - Evaluates LLMs on class-level code generation with 100 tasks.

  - **Assistants**
    - **GAIA:** A Benchmark for General AI Assistants  
      - Tests reasoning, multi-modality, web browsing, and tool-use proficiency.
    - **OSWorld**  
      - Benchmark for multimodal agents for open-ended tasks in real computer environments.
    - **AssistantBench:** Can Web Agents Solve Realistic and Time-Consuming Tasks?  
      - Evaluates AI agents on real-world web-based tasks.
    - **Sycophancy Eval**  
      - Measures sycophancy in AI responses across various free-form text-generation tasks.

  - **Cybersecurity**
    - **Cybench:** A Framework for Evaluating Cybersecurity Capabilities and Risks of Language Models  
      - 40 professional-level Capture the Flag (CTF) tasks spanning a wide range of difficulties.
    - **CyberMetric:** A Benchmark Dataset for Evaluating LLMs in Cybersecurity Knowledge  
      - Multiple-choice datasets designed to assess cybersecurity knowledge across nine domains.
    - **CyberSecEval_2:** A Wide-Ranging Cybersecurity Evaluation Suite for LLMs  
      - Evaluates LLM capabilities in cybersecurity risks.
    - **InterCode:** Capture the Flag  
      - Measures expertise in coding, cryptography, reverse engineering, and security vulnerabilities.
    - **GDM Dangerous Capabilities:** Capture the Flag  
      - CTF challenges covering web app vulnerabilities, privilege escalation, and password cracking.
    - **SEvenLLM:** Benchmark for Cybersecurity Incident Analysis and Response  
      - Tests LLMs in security event analysis and response with 28 task subcategories.
    - **SecQA:** A Question-Answering Dataset for Evaluating LLMs in Computer Security  
      - Dataset assessing understanding and application of cybersecurity principles.

  - **Safeguards**
    - **AgentHarm:** A Benchmark for Measuring Harmfulness of LLM Agents  
      - 110 explicitly malicious tasks covering fraud, cybercrime, and harassment.
    - **WMDP:** Measuring and Reducing Malicious Use With Unlearning  
      - A dataset evaluating hazardous knowledge in biosecurity, cybersecurity, and chemical security.

  - **Mathematics**
    - **MATH:** Measuring Mathematical Problem Solving  
      - 12,500 competition-level mathematics problems.
    - **GSM8K:** Training Verifiers to Solve Math Word Problems  
      - 8.5K linguistically diverse grade school math problems.
    - **MathVista:** Evaluating Mathematical Reasoning in Visual Contexts  
      - Requires deep visual understanding and compositional reasoning.
    - **MGSM:** Multilingual Grade School Math  
      - Translates 250 GSM8K problems into 10 languages.

  - **Reasoning**
    - **V*Bench:** A Visual QA Benchmark with High-Resolution Images  
      - Evaluates MLLMs on fine-grained visual understanding.
    - **ARC:** AI2 Reasoning Challenge  
      - Grade-school science multiple-choice questions.
    - **HellaSwag:** Evaluating Commonsense Inference  
      - Tests models' ability to complete event descriptions logically.
    - **PIQA:** Physical Commonsense Reasoning  
      - Evaluates understanding of everyday physics scenarios.
    - **∞Bench:** Extending Long Context Evaluation Beyond 100K Tokens  
      - Tests LLMs on long-context inputs.
    - **BBH:** Challenging BIG-Bench Tasks  
      - 23 reasoning-intensive tasks requiring chain-of-thought processing.
    - **BoolQ:** Yes/No Reading Comprehension  
      - Requires inference to determine answers.
    - **DocVQA:** Visual Question Answering for Documents  
      - 50,000 questions covering document images.
    - **DROP:** Discrete Reasoning Over Paragraphs  
      - Requires counting, sorting, and arithmetic reasoning.
    - **WINOGRANDE:** Adversarial Winograd Schema Challenge  
      - Tests pronoun resolution with expert-crafted problems.
    - **RACE-H:** Reading Comprehension and Reasoning  
      - Collected from high school and middle school English exams.
    - **MMMU:** Multimodal Understanding and Reasoning  
      - Requires college-level subject knowledge and deliberate reasoning.
    - **SQuAD:** Reading Comprehension on Wikipedia  
      - 100,000+ questions from Wikipedia articles.
    - **IFEval:** Evaluating Instruction Following in LLMs  
      - Tests adherence to verifiable instructions.
    - **MuSR:** Multistep Soft Reasoning  
      - Evaluates reasoning through free-text narratives.
    - **Needle in a Haystack (NIAH):** In-Context Retrieval for Long-Context LLMs  
      - Assesses ability to extract factual information from long documents.
    - **PAWS:** Paraphrase Detection  
      - Tests models on distinguishing paraphrased sentences.

  - **Knowledge**
    - **MMLU:** Measuring Massive Multitask Language Understanding  
      - 57 diverse knowledge-based tasks.
    - **MMLU-Pro:** More Challenging Multi-Task Language Understanding  
      - Adds reasoning-focused challenges to MMLU.
    - **GPQA:** Graduate-Level Google-Proof Q&A  
      - Expert-written biology, physics, and chemistry questions.
    - **CommonsenseQA:** Commonsense Question Answering  
      - Evaluates models’ ability to apply commonsense knowledge.
    - **TruthfulQA:** Measuring Model Truthfulness  
      - Tests whether models generate factual answers.
    - **XSTest:** Identifying Exaggerated Safety Behaviors in LLMs  
      - Distinguishes between safe and unsafe prompt responses.
    - **Humanity's Last Exam**  
      - A multimodal benchmark assessing frontier human knowledge.
    - **O-NET:** High-School Knowledge Test  
      - English and Thai educational test questions.
    - **PubMedQA:** Biomedical Question Answering  
      - Questions sourced from PubMed abstracts.
    - **AGIEval:** Evaluating Human-Centric Cognitive Tasks  
      - Assesses LLMs on problem-solving and reasoning.
    - **SimpleQA:** Short-Form Factuality Measurement  
      - Tests ability to answer brief factual questions.
