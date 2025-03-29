# LangKit

## Tool description

LangKit is an open source text metrics toolkit for monitoring language models. It comes with a variety of methods for extracting relevant information from the prompts sent and responses coming from a model.

This project is backed by WhyLabs, a company specializing in AI observability and security, providing tools to monitor, manage, and safeguard machine learning (ML) and generative AI applications.

LangKit focuses on runtime monitoring of the inputs and outputs of LLMs. It covers, Text Quality features with readability and complexity scores, Text relevance, to ensure that the prompt/responses are relevant against user-defined themes and that the topics they cover are similar, Security and Privacy, which covers, among other things, jailbreaks, prompt injections and hallucinations, and lastly, Sentiment and toxicity analysis.

Since we are talking about real time monitoring, visualization of he results are key. Langkit offers two possibilities. The first is sending the results to WhyLabs platform to visualize them, which requires opening an account and creating an API key to use (there is a free tier that you can benefit from). The second is using another open source library that WhyLabs provides, which is WhyLogs and with which you can visualize the results as well without needing to send them outside.

In general, we found LangKit very easy to use, it’s not the best maintained tool from the ones we analyzed but the status of the repository is acceptable, and very useful in terms of real time monitoring of LLMs.

## Notebooks

### LangKit.ipynb

In this notebook we use a given dataset from **WhyLabs** to perform analysis using LangKit and visualize the results using `whylogs`.

## Tooling

- Prompt Features


  - **prompt.aggregate_reading_level**: An aggregated score representing the overall readability of the prompt.
  - **prompt.automated_readability_index**: A metric assessing the readability of the prompt based on sentence length and word complexity.
  - **prompt.character_count**: The total number of characters in the prompt.
  - **prompt.difficult_words**: The count of complex or uncommon words in the prompt.
  - **prompt.flesch_reading_ease**: A readability test score indicating how easy the prompt is to read.
  - **prompt.has_patterns**: Detection of predefined patterns within the prompt, such as specific phrases or structures.
  - **prompt.jailbreak_similarity**: Measures the similarity of the prompt to known jailbreak attempts designed to bypass model restrictions.
  - **prompt.letter_count**: The number of alphabetic characters in the prompt.
  - **prompt.lexicon_count**: The count of unique words used in the prompt.
  - **prompt.monosyllable_count**: The number of monosyllabic words in the prompt.
  - **prompt.polysyllable_count**: The count of words with multiple syllables in the prompt.
  - **prompt.sentence_count**: The total number of sentences in the prompt.
  - **prompt.sentiment_nltk**: Sentiment analysis score derived using the Natural Language Toolkit (NLTK), indicating the emotional tone of the prompt.
  - **prompt.syllable_count**: Total number of syllables in the prompt.
  - **prompt.toxicity**: Assessment of harmful or toxic language present in the prompt.

- Response Features


  - **response.aggregate_reading_level**: An aggregated score representing the overall readability of the response.
  - **response.automated_readability_index**: A metric assessing the readability of the response based on sentence length and word complexity.
  - **response.character_count**: The total number of characters in the response.
  - **response.difficult_words**: The count of complex or uncommon words in the response.
  - **response.flesch_reading_ease**: A readability test score indicating how easy the response is to read.
  - **response.has_patterns**: Detection of predefined patterns within the response, such as specific phrases or structures.
  - **response.letter_count**: The number of alphabetic characters in the response.
  - **response.lexicon_count**: The count of unique words used in the response.
  - **response.monosyllable_count**: The number of monosyllabic words in the response.
  - **response.polysyllable_count**: The count of words with multiple syllables in the response.
  - **response.refusal_similarity**: Measures the similarity of the response to known refusal patterns, indicating potential non-compliance.
  - **response.relevance_to_prompt**: Evaluates how closely the response aligns with the content and intent of the prompt.
  - **response.sentence_count**: The total number of sentences in the response.
  - **response.sentiment_nltk**: Sentiment analysis score derived using NLTK, indicating the emotional tone of the response.
  - **response.syllable_count**: Total number of syllables in the response.
  - **response.toxicity**: Assessment of harmful or toxic language present in the response.
