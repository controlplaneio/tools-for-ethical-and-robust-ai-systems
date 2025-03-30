# LangKit

## Tool description

LangKit is an open-source text metrics toolkit for monitoring language models. It includes various methods for extracting relevant information from prompts sent to a model and its responses.

This project is backed by WhyLabs, a company specializing in AI observability and security, providing tools to monitor, manage, and safeguard machine learning (ML) and generative AI applications.

LangKit focuses on real-time monitoring of LLM inputs and outputs. It covers Text Quality, offering readability and complexity scores; Text Relevance, ensuring prompts and responses align with user-defined themes and cover similar topics; Security and Privacy, addressing issues such as jailbreaks, prompt injections, and hallucinations; and Sentiment and Toxicity Analysis.

Since real-time monitoring is essential, visualizing the results is key. LangKit offers two options:

Sending the results to the WhyLabs platform for visualization, which requires creating an account and an API key (a free tier is available).

Using WhyLabs’ open-source library, WhyLogs, to visualize results locally without sending data externally.

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
