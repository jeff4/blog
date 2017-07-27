---
layout: single
title: "Chollet, Deep Learning, and The Singularity "
tags: tech machine-learning math
---

[François Chollet](https://twitter.com/fchollet) is the creator of [Keras](https://keras.io), the popular open-source neural network Python library that runs on top of TensorFlow, CNTK, and Theano. Last week, he published articles about the [current limitations](https://blog.keras.io/the-limitations-of-deep-learning.html) of and [future prospects](https://blog.keras.io/the-future-of-deep-learning.html) for deep learning. 

The [first piece](https://blog.keras.io/the-limitations-of-deep-learning.html) emphasizes that all deep learning systems require:

1. **input** that can be represented by n-dimensional vectors that
2. map to **outputs** via
3. a complex geometric **transformation**–which is just a fancy vector-space way of saying *function*. 

Although a lot of tasks are amenable to the above three conditions, that is still only a tiny subset of phenomena in the world.

If that's not difficult enough, there are two additional requirements for deep learning as it is currently implemented: (4) *each* step of the chained geometric transformation must be smooth and continuous and (5) the *overall* soup-to-nuts transformation must also be smooth and continuous.

I had earlier understood that (4) was required during the neural net training phase to make optimization via gradient descent (or other methods) possible via differentiation. But I didn't realize that the entire operation from input to output needed to itself be differentiable. (This is probably obvious to mathemations!)

Chollet writes a beautifully concise description here: 

>That's the magic of deep learning: turning meaning into vectors, into geometric spaces, then incrementally learning complex geometric transformations that map one space to another. All you need are spaces of sufficiently high dimensionality in order to capture the full scope of the relationships found in the original data.

In any case, his [article](https://blog.keras.io/the-limitations-of-deep-learning.html) explains why huge theoretical and engineering breakthroughs are still required to ever build  Artificial General Intelligence or any super-intelligence that will be able to speed us through [the singularity](https://en.wikipedia.org/wiki/Technological_singularity).

Chollet reminds me that those who are actually building AI systems are far less worried about the robot apocalypse. Contrast his perspective with those of AI alarmists like Elon Musk, Stephen Hawking, Martin Rees. Those three are brilliant but not at the "coal face" of building AI systems the way Chollet is. 