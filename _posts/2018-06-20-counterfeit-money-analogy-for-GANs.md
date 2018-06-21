---
layout: single
title: "Counterfeit Money As An Analogy for GANs"
tags: tech machine-learning research GAN
---

Based on feedback from a friend, I'm going to revisit [GANs](/blog/2018/generative-adversarial-networks/) in a more approachable way. This is an adaptation of the analogy Goodfellow et al. introduced in their original [2014 Generative Adversarial Network paper](https://arxiv.org/abs/1406.2661).

Imagine we have a game with three players: (1) a government mint which prints legitimate money, (2) a counterfeiter which produces fake currency hoping to make some quick criminal profits, and (3) a police officer who wants to tell the difference between the real and fake currency.

During each round of the game, the mint and the counterfeiter each present a batch of money (real and fake, respectively) to the police officer. The mint can be considered a constant–it  only produces the same type of real money over and over again. However, the counterfeiter is constantly trying to produce fake money that looks more and more realistic. At the same time, the police officer is constantly trying to her skill at telling fake money apart from real money. 

At the end of each round, the success of the police officer and the counterfeiter is tallied up. Based on their scores, the counterfeiter adjusts his printing techniques to make better looking fake money; and the police officer sharpens her sensitivity to the telltalle traces of fake currency. We then play another round and repeat the process with counterfeiter and police who are better at their tasks.

In other words, we have an [evolutionary arms race](https://en.wikipedia.org/wiki/Evolutionary_arms_race). We would expect gazelles (and the cheetahs who hunt them) to [run faster and faster](https://thelandscapeofreality.com/2016/02/14/the-evolutionary-arms-race/) over successive generations because of predator-prey competition.

 Similarly, after many rounds of play, we would expect the counterfeiter to steadily improve the quality of his fake currency and the police to get more and more effective at spotting fakes.

In essence, this is how GANs work, where: (1) the mint is actually a library of real ground-truth images, (2) the counterfeiter is the "generative neural network" creating fake images that are supposed to look real, and (3) the police officer is the "discriminator neural network" that is able to accurately distinguish real images from the library versus fake images from the generator.

As a side note, most versions of the counterfeiter-police analogy ignore the mint. I find it helpful to specifically call out who is producing the real money.
