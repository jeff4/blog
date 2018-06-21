---
layout: single
title: "Counterfeit Money As An Analogy for GANs"
tags: tech machine-learning research GAN
---

Based on feedback from a friend, I'm going to revisit [GANs](/blog/2018/generative-adversarial-networks/) in a more approachable way. This is an adaptation of the analogy Goodfellow et al. introduced in their original [2014 Generative Adversarial Network paper](https://arxiv.org/abs/1406.2661).

Imagine we have a game with three players: (1) a government mint which prints legitimate money, (2) a counterfeiter which produces fake currency hoping to make some quick criminal profits, and (3) a police officer who wants to tell the difference between the real and fake currency.

During each round of the game, the mint and the counterfeiter each present a batch of money (real and fake, respectively) to the police officer. The mint can be considered a constant–it  only produces the same type of real money over and over again. However, the counterfeiter is trying to produce fake money that looks as realistic as possible. At the same time, the police officer is doing her best to accurately distinguish fake money from real money. 

At the end of each round, the scores of the police officer and the counterfeiter are tallied up. If the counterfeiter succeeded in fooling the police, he gets a good score and the police gets a low score and vice versa if the police correctly marks the counterfeit as fake currency. Based on these results, the counterfeiter adjusts his printing techniques; and the police officer sharpens her sensitivity to the telltalle traces of fake currency. The players then start a new round with better counterfeiting and detection skills.

In other words, we have an [evolutionary arms race](https://en.wikipedia.org/wiki/Evolutionary_arms_race). We would expect gazelles (and the cheetahs who hunt them) to [run faster and faster](https://thelandscapeofreality.com/2016/02/14/the-evolutionary-arms-race/) over successive generations because of predator-prey competition.

 Similarly, after many rounds of play, we would expect the counterfeiter to steadily improve the quality of his fake currency and the police to get more and more effective at spotting fakes.

In essence, this is how GANs work, where: (1) the mint is  a library of real images, (2) the counterfeiter is the "generative neural network" creating fake images that are supposed to look authentic, and (3) the police officer is the "discriminator neural network" whose job is to tell ground truth images from the library apart from the fake images from the generator net.

As a side note, most versions of the counterfeiter-police analogy ignore the mint. I find it helpful to specifically call out who is producing the real money.
