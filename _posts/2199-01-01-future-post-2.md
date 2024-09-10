---
title: 'ML4LM - Vanishing Gradient Problem?'
date: 2024-01-02
medium_link: "https://hoyath.medium.com/vanishing-gradient-problem-583ce734af39"

permalink: /posts/2024/01/blog-post-2/
tags:
  - Neural Networks
  - Activation Function
  - Vanishing Gradient
---

Ever noticed that while training neural networks, the loss stops decreasing, and weights don't get updated after a certain point? Understanding this hitch involves looking at how we optimize loss using gradient descent, adjusting weights to find the lowest loss.

Let's picture a neural network with the aim of minimizing the loss, called O1. To update weights through gradient descent, we need to know how each weight affects the output. During backpropagation, we find that O1 is influenced by W5 and W6, and h1 is affected by w1 and w2, with w1 also affecting O1 through a chain reaction.

![NN](https://cdn-images-1.medium.com/max/800/1*lTZG3zjs0nm78g2xEiv9rw@2x.jpeg)


Calculating the rate of change to O1 concerning w1 would look something like this using the chain rule:

**Rate of change of O1 (wrt w1) =**  
\[ \text{Rate of change of O1 (wrt w5)} \times \text{Rate of change of w5 (wrt h1)} \times \text{Rate of change of h1 (wrt w1)} \]

In math, this would look like:

\[
\frac{\partial O1}{\partial w1} = \frac{\partial O1}{\partial w5} \times \frac{\partial w5}{\partial h1} \times \frac{\partial h1}{\partial w1}
\]

We end up multiplying all these gradients or derivatives. However, if \( h1 \) here is a sigmoid function whose gradient is always between (0–0.25), as the number of layers increases and this keeps getting backpropagated, the derivative becomes very small, making a negligible effect on the weight \( w1 \).

![formulae](https://cdn-images-1.medium.com/max/800/1*YF1D2Z5xbIuFBZRXf1tdXw@2x.jpeg)


### How Do We Know This Is Happening?
- No changes to Loss.
- Plots of weights against epochs.

### Here Are Some Down-to-Earth Solutions:

- **Simplify the Model:** Decrease the number of layers. Be careful; this might lose the essence of why you used a neural network in the first place.
- **ReLU Activation Function:** Use the ReLU function to tackle negative values by setting them to 0. Think of it like flipping a switch on or off. Watch out for "Dying ReLU," though; sometimes everything becomes zero. Leaky ReLU can help here.
- **Proper Weight Initialization:** Start off with good weight values. It's like giving your neural network a solid foundation to build upon.
- **Batch Normalization:** Keep things in check by normalizing inputs within each mini-batch. It helps maintain stable gradients, overcoming the vanishing gradient problem.
- **Residual Network (ResNet):** Create shortcuts in your neural network to let information flow directly across layers. This helps a lot in dealing with the vanishing gradient problem.

So, if your neural network seems stuck, try these fixes. They're like giving your network a little nudge, helping it learn more effectively.
