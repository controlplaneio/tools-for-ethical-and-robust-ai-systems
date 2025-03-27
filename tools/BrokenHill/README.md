# BrokenHill

## Tool description

To be fair, we had a lot of fun with BrokenHill. It covers just a single attack against LLM, the Greedy Coordinate Gradient (GCG) attack which is essentially a jailbreak adversarial attack.

The logic behind the attack is simple, you define an input, which is normally something that under normal conditions the LLM wouldn’t respond to (in our tests, we asked how to annihilate the human race, for a reasonable price I’m willing to disclose that information) and the beginning of an ideal response (i.e: Sure thing, the best way to annihilate the human race would be…). Then, the adversarial attack model will slightly modify the input with strange characters or with other sentences until the target model responds something that starts more or less as the beginning of your ideal response using gradient descent.

Despite all the fun, it would be difficult to use it in a production grade environment because it requires a sheer amount of resources (>20GB Memory of GPU) and it’s not very well maintained unfortunately (deprecated libraries and broken dependencies), however, we find it useful for academic purposes or for enjoying yourself on a boring day.

## Notebooks

### BrokenHill.ipynb

In this notebook we perform a Greedy Coordinate Gradient attack to make Microsoft's phi 2 model give us a plan to annihilate the humanity.

Note: It requires a relatively big GPU (>20GB memory), therefore, we recommend to run it in colab using A100 runtime.

## Tooling

- **Attacks**
  - **Greedy Coordinate Gradient (GCG)**: the logic behind the attack is simple, you define an input, which is normally something that under normal conditions the LLM wouldn’t respond to (in our tests, we asked how to annihilate the human race, for a reasonable price I’m willing to disclose that information) and the beginning of an ideal response (i.e: Sure thing, the best way to annihilate the human race would be…). Then, the adversarial attack model will slightly modify the input with strange characters or with other sentences until the target model responds something that starts more or less as the beginning of your ideal response using gradient descent.
