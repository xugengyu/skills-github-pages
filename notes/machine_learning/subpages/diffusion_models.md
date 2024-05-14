
<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

Source: https://www.assemblyai.com/blog/diffusion-models-for-machine-learning-introduction/

*The following notes are for my personal reference only. They may contain direct quotations or reproductions from external sources, including text and images. These materials are utilized solely for the purpose of personal study and reference. Any use beyond this context may require permission from the original creators or copyright holders.*

### Diffusion Models

Diffusion models are generative models which learn by initially *destroying* the training data, and subsequently recovering it through denoising.

When the model is trained, one can generate new data by feeding random noise into the learned denoising process.

A diffusion model model maps input data an into to a latent space using a fixed ***Markov Chain***.



<div class="warning" style='background-color:#E9D8FD; color: #69337A; border-left: solid #805AD5 4px; border-radius: 4px; padding:0.7em;'>
<span>
<p style='margin-top:1em; text-align:center'>
<b>Note: Markov Chains</b></p>
<p style='margin-left:1em;'>
A Markov chain is a process in which the probability of each event only depends on the state attained in the previous event. We can model a Markov chain with a set of states and a transition matrix that defines the propabailities of moving from one state to all other states.
</p></span>
</div>


The Markov chain gradually addes noise to the input data to obtain 

<div class="warning" style='background-color:#E9D8FD; color: #69337A; border-left: solid #805AD5 4px; border-radius: 4px; padding:0.7em;'>
<span>
<p style='margin-top:1em; text-align:center'>
<b>Note: Posterior Probability</b></p>
<p style='margin-left:1em;'>
The propability of $\theta$

<span class="tex">\(P(\theta|A)\)</span>
</p></span>
</div>