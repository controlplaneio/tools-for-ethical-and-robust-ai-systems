# BrokenHill

## Tool description

BrokenHill is a tool designed to execute the Greedy Coordinate Gradient (GCG) attack, an adversarial jailbreak method targeting large language models (LLMs). This attack aims to manipulate an LLM into generating restricted responses by gradually modifying the input.

The process involves defining an initial input that the model would normally reject and specifying the desired beginning of a response. The attack then iteratively alters the input using subtle changes—such as introducing special characters or alternative phrasing—until the model produces an output that aligns with the predefined response pattern. This optimization is achieved through gradient descent.

While BrokenHill effectively demonstrates the vulnerability of LLMs to adversarial attacks, its practical use in real-world environments is limited. The tool requires significant computational resources, including more than 20GB of GPU memory, and suffers from maintenance issues, such as deprecated libraries and broken dependencies. However, it remains an useful resource for research and experimentation in adversarial attack methodologies.

## Notebooks

### BrokenHill.ipynb

In this notebook we perform a Greedy Coordinate Gradient attack to make Microsoft's phi 2 model give us a plan to annihilate the humanity.

Note: It requires a relatively big GPU (>20GB memory), therefore, we recommend to run it in colab using A100 runtime.

## Tooling

- **Attacks**
  - **Greedy Coordinate Gradient (GCG)**: the logic behind the attack is simple, you define an input, which is normally something that under normal conditions the LLM wouldn’t respond to (in our tests, we asked how to annihilate the human race, for a reasonable price I’m willing to disclose that information) and the beginning of an ideal response (i.e: Sure thing, the best way to annihilate the human race would be…). Then, the adversarial attack model will slightly modify the input with strange characters or with other sentences until the target model responds something that starts more or less as the beginning of your ideal response using gradient descent.
