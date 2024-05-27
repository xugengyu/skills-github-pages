---
use_math: true
---

<h1> Diffusion Models </h1>

Diffusion models are generative models which learn by initially *destroying* the training data, and subsequently recovering it through denoising.

When the model is trained, one can generate new data by feeding random noise into the learned denoising process.

A diffusion model model maps input data an into to a latent space using a fixed ***Markov Chain***.

> A Markov chain is a process in which the probability of each event only depends on the state attained in the previous event. We can model a Markov chain with a set of states and a transition matrix that defines the probabilities of moving from one state to all other states.

The Markov chain gradually adds noise to the input data to obtain ...

> The posterior \\(P(\theta\|A)\\), is defined as the probability of observing \\(\theta\\), given the evidence \\(A\\).

<h3> Sources </h3>

1. <https://www.assemblyai.com/blog/diffusion-models-for-machine-learning-introduction/>

2. <https://en.wikipedia.org/wiki/Markov_chain/>