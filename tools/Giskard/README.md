# Giskard

## Tool description

We move now to Giskard, a tool also for evaluation but with a different focus.

This tool does not rely on static probes, but it will generate datasets for your specific model description, using its own LLM for doing so, and will not only focus on security. It’s also not only for LLM, but can also evaluate datasets, ML classification, and computer vision.

Here you can find examples Google Colab notebooks updated by us to pin libraries to specific versions to avoid conflicts that you may find on the official ones:

As you see the range of topics is broad, but the number of examples of the generated datasets are very short compared to others described previously. But as they are custom tailored for your model or dataset, they may be enough to catch the specific critical cases. And what's more important, it makes the evaluation more manageable to be conducted continuously with any small change to the AI system, as it won’t take so long to finish or require so many compute resources.

## Notebooks

### giskard_quickstart_nlp.ipynb

TODO

### giskard_quickstart_tabular.ipynb

TODO

### giskard_quickstart_vision.ipynb

TODO

### My_Guiskard_quickstart_llm.ipynb

TODO

## Tooling

- **LLM Detectors**: A set of checks and tools designed to evaluate and detect specific issues with large language models.

  - **Injection Attacks**: Ensure that injecting control characters into a model's prompt does not alter its output.  
    [Related Paper](https://dropbox.tech/machine-learning/prompt-injection-with-control-characters-openai-chatgpt-llm)

  - **Hallucination and Misinformation**: Detect whether the model generates hallucinated information or spreads misinformation during responses.

  - **Sycophancy**: Evaluate if the model generates overly flattering or sycophantic responses, potentially leading to misleading or biased output.

  - **Harmful Content Generation**: Test whether the model generates responses that promote harmful actions or ideas.

  - **Stereotypes**: Check if the model generates responses containing stereotypes, discriminatory content, or biased opinions. This involves creating adversarial inputs based on the model's name and description.

  - **Information Disclosure**: Ensure the model does not divulge or hallucinate sensitive or confidential information. False positives may arise if the model is supposed to provide contact information.

  - **Output Formatting**: Ensure that the model's output is consistent with the format requirements as specified in its description.

  - **Robustness**: TODO add definition

  - **RAG Evaluation Toolkit**: A set of tools designed to assess and evaluate retrieval-augmented generation (RAG) models on various dimensions.

    - **Correctness**: Evaluate whether the model's answer is correct when compared to a reference answer.

      - **RAGAS Metrics**: Metrics used to evaluate the performance and quality of RAG models.

        - **Faithfulness**: Assess the accuracy and reliability of the model’s output, ensuring it aligns with the source or provided reference material.

        - **Answer Relevancy**: Measure how relevant the model's response is to the given input or query.

        - **Context Recall**: Evaluate how well the model retains and uses contextual information during its responses.

  - **ML Model Vulnerabilities**: Detect any weaknesses or vulnerabilities in the machine learning model that could be exploited for malicious purposes.

    - **Performance Bias**: Measure whether the model shows any biases in its performance across different groups or categories.

    - **Unrobustness**: Assess if the model's performance degrades significantly when faced with variations or adversarial inputs.

    - **Overconfidence**: Evaluate if the model provides overly confident answers when uncertain or when the answer is not well-supported by the data.

    - **Underconfidence**: Detect if the model is overly cautious, failing to give definitive answers in situations where it should.

    - **Unethical Behavior**: Check whether the model produces unethical or inappropriate responses based on its inputs.

    - **Data Leakage**: Evaluate if the model inadvertently reveals private or confidential data within its responses.

    - **Stochasticity**: Measure the model's consistency in generating responses to the same input, checking for randomness or variability in output.

    - **Spurious Correlation**: Detect any false correlations that the model might make between input variables and output responses that don't logically follow.
