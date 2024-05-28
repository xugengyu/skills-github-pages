---
use_math: true
---

<h1> Diffusion Models </h1>

<h3> Disclaimer </h3>
*The following notes are for my personal reference only. They may contain direct quotations or reproductions from external sources, including text and images. These materials are utilized solely for the purpose of personal study and reference. Any use beyond this context may require permission from the original creators or copyright holders.*

<h3> Introduction </h3>

Diffusion models are generative models which learn by initially *destroying* the training data, and subsequently recovering it through denoising.

When the model is trained, one can generate new data by feeding random noise into the learned denoising process.

A diffusion model model maps input data an into to a latent space using a fixed ***Markov Chain***.

> A Markov chain is a process in which the probability of each event only depends on the state attained in the previous event. We can model a Markov chain with a set of states and a transition matrix that defines the probabilities of moving from one state to all other states.

The Markov chain gradually adds noise to the input data to obtain the approximate posterior \\(P(\vec{x}_{1:T}\|\vec{x}_0)\\), where \\(\vec{x}\\) are latent space vectors, all with the same dimensionality.

> The posterior \\(P(\theta\|A)\\), is defined as the probability of observing \\(\theta\\), given the evidence \\(A\\).

<p align="center">
<img src="https://paulxu.me/notes/machine_learning/subpages/diffusion_model/diffusion_forward.jpeg" alt="drawing" width="500"/>
</p>

Through the above noising processing, an input image is eventually transformed into pure Gaussian noise. 

The diffusion model is trained to ***reverse*** the above process by removing the noise. This allows us to generate new data by using Gaussian noise as the input.

<p align="center">
<img src="https://paulxu.me/notes/machine_learning/subpages/diffusion_model/diffusion_backward.jpeg" alt="drawing" width="500"/>
</p>

<h3> Forward and Reverse Diffusion </h3>

To reiterate, the diffusion model consists of

1. A forward process (diffusion), in which the datum is progressively noised.
2. A reverse process (reverse diffusion), in which noise is transformed into a *sample* from the target distribution.

$$
K(a,b) = \int \mathcal{D}x(t) \exp(2\pi i S[x]/\hbar)
$$

<h3> Sources </h3>

1. <https://www.assemblyai.com/blog/diffusion-models-for-machine-learning-introduction/>

2. <https://en.wikipedia.org/wiki/Markov_chain/>