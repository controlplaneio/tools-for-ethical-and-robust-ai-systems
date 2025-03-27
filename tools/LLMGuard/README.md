# LLM Guard

## Tool description

Checking is nice, but is there a way to detect problematic situations during runtime to block them?

Mitigating this situations is important, and the state of the art consist of using another LLM to evaluate the prompt question from the user, as well as the answer for the inference LLM, to determine if safety is being breached.

Among this category of tools you can use LLM Guard. It provides several kinds of filters, some based on different “LLMs as a judge” and other classifier models, that will detect with a percentage score if the input contains a possible prompt injection, the answer has been toxic, or includes a denial to the user (which repeatedly may mean the user is trying to force the LLM to do something it shouldn’t). It’s up to you to use these percentages in any way you desire to monitor of block the behavior. 

Another interesting features not present in similar “LLM as a judge” tools is the capacity to detect Private Identifiable Information on the prompt, replace it with markers so it’s not sent to the inference endpoint that may be executing in a SaaS outside, and repopulating the answer, changing the markers back to the real data the user was providing.

All these kinds of tools have the limitation that you either lose the “streaming” behavior of the LLM, where you can see word by word what it’s generating, or risk having an offending answer being shown to the user before it’s then evaluated fully and blocked.

LLM Guard employs several open source models to do their detection, some with their own limitations, for example the prompt injection classification model relies on a dataset that only contains examples in English. Language is a well known attack vector, so this isn’t a trivial limitation, although you could try also to activate the filter it includes to restrict the conversation to a specific language, and choose only English, if you can afford it for your purposes.

## Notebooks

### llm_guard_poetry.ipynb

TODO

## Tooling

- **Input Scanners**: A set of tools designed to scan and filter inputs to detect and prevent unwanted or harmful content before it is processed by a language model.

  - **Anonymize**: Ensure user prompts remain confidential and free of sensitive data, detecting credit card numbers, personal names, phone numbers, URLs, emails, IPs, UUIDs, US social security numbers, crypto wallet addresses, and IBAN codes. Leverages [Presidio](https://github.com/microsoft/presidio/) and various Named Entity Recognition (NER) models.
  
  - **Ban Code**: Detect and ban code from the input to prevent misuse of the model for code generation or attacks involving code. Leverages `vishnun/codenlbert-tiny` and `vishnun/codenlbert-sm` models.

  - **Ban Competitors**: Prevent the use of competitor names in the input. Leverages `guishe/nuner-v1_orgs` model.

  - **Ban Substrings**: Prevent specific harmful substrings from appearing in prompts. Uses a list of harmful substrings, though the list may be outdated. 

  - **Ban Topics**: Restrict certain topics such as religion and violence using a zero-shot classifier. Leverages `collections/MoritzLaurer/zeroshot-classifiers-6548b4ff407bb19ff5c3ad6f` model.

  - **Code**: Detect and validate code in the prompt, allowing or forbidding specific programming languages. Leverages `philomath-1209/programming-language-identification` model.

  - **Gibberish**: Identify and block gibberish text, which could indicate an attack or an attempt to probe for weaknesses. Leverages `madhurjindal/autonlp-Gibberish-Detector-492513457` model.

  - **Invisible Text**: Detect and remove non-printable characters to prevent stenography attacks.

  - **Language**: Identify the language of the prompt, useful for restricting inputs to a single language. Leverages `papluca/xlm-roberta-base-language-detection` model.

  - **Prompt Injection**: Detect if the input is similar to a known prompt injection attack. Leverages `protectai/deberta-v3-base-prompt-injection-v2` model.

  - **Regex**: Detect regular expressions in the input for more powerful pattern matching than static substrings.

  - **Secrets**: Detect secrets such as API keys, tokens, or other access credentials within the input. Leverages `Yelp/detect-secrets` model.

  - **Sentiment**: Classify the sentiment of the prompt as positive, neutral, or negative. Useful for monitoring and moderation. Leverages `nltk.org/howto/sentiment.html` model.

  - **Token Limit**: Ensure prompts do not exceed a token limit to prevent denial-of-wallet attacks or attempts to force the model beyond its limits. Leverages `openai/tiktoken` library.

  - **Toxicity**: Analyze the toxicity of the prompt to help prevent the dissemination of harmful content. Leverages `unitary/unbiased-toxic-roberta` model.

- **Output Scanners**: Similar to input scanners, these tools scan the output from a language model for harmful or undesirable content.

  - **Ban Competitors**: Prevent competitors' names from appearing in the model's output.

  - **Ban Substrings**: Prevent specific harmful substrings from appearing in the output.

  - **Ban Topics**: Restrict certain topics such as religion, violence, or other sensitive subjects from being discussed in the output. Leverages `MoritzLaurer/deberta-v3-base-zeroshot-v1.1-all-33` model.

  - **Code**: Detect and validate code in the output, forbidding or allowing specific programming languages.

  - **Language**: Ensure the output matches the language of the prompt to prevent jailbreaks that exploit weaker guardrails in other languages.

  - **Gibberish**: Block gibberish responses in the output.

  - **Regex**: Detect regular expressions in the output.

  - **Sentiment**: Classify the sentiment of the output as positive, neutral, or negative.

  - **Toxicity**: Analyze the toxicity of the output to prevent harmful content from being generated.

  - **Bias**: Detect potential bias in the model's output. Leverages `valurank/distilroberta-bias` model.

  - **Deanonymize**: Reintroduce previously anonymized information back into the model's output to preserve the appearance of uncensored responses while maintaining confidentiality.

  - **JSON**: Ensure the output is in valid JSON format.

  - **Language Same**: Ensure the model’s output is in the same language as the prompt, preventing language-based jailbreaks.

  - **Malicious URL**: Detect potentially harmful URLs in the output, such as phishing URLs. Leverages `DunnBC22/codebert-base-Malicious_URLs` model.

  - **No Refusal**: Detect refusals in the output, which could indicate attempts to bypass the model's guardrails.

  - **Reading Time**: Provide an estimate of the total reading time for the output.

  - **Factual Consistency**: Assess whether the model’s output contradicts or refutes any statements or the prompt. Leverages `MoritzLaurer/deberta-v3-base-zeroshot-v1.1-all-33` model.

  - **Relevance**: Ensure that the output is relevant to the input by measuring similarity in embeddings. Uses `BAAI/bge-base-en-v1.5` model.

  - **Sensitive**: Similar to the Anonymize input scanner, this checks if the output contains private identifiable information that may have been inadvertently generated by the model.

  - **URL Reachability**: Ensure that URLs mentioned in the output point to valid web pages (HTTP code 200), to prevent hallucinated or invalid links.
