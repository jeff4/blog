---
layout: single
title: "Counterfeit Money As An Analogy for GANs"
tags: tech machine-learning research GAN
---

Based on the feedback of a friend, I'm going to revisit [GAN's]((/blog/2018/generative-adversarial-networks/) ) in a more approachable way. This is an adaptation of the analogy introduced in the original [2014 Generative Adversarial Network paper](https://arxiv.org/abs/1406.2661) by Goodfellow et al.

Imagine we have a game with three players: (1) a government mint which prints legitimate money, (2) a counterfeiter which produces fake currency hoping to make some quick criminal profits, and (3) a police officer who wants to tell the difference between the real and fake currency.

During each round of the game, both the mint and the counterfeiter present a batch of real and fake currency to the police officer. The mint can be considered a constant who only produces the same type of money over and over again. However, the counterfeiter is constantly trying to produce fake money that looks more and more like the real thing. At the same time, the police officer is constantly trying to improve at distinguishing between real and fake money. 

At the end of each round, the success of the police officer and the counterfeiter in achieving their oppposite (aka "adversarial") aims is tallied up. Based on those scores, the counterfeiter adjusts his printing techniques to make better looking fake money; and the police officer sharpens her sensitivity to the telltalle traces of fake currency. Then, start another round of play where the counterfeiter and police match wits with better skills of deception and perception, respectively.

In other words, we have an [evolutionary arms race](https://en.wikipedia.org/wiki/Evolutionary_arms_race); for example, we would expect gazelles (and the cheetahs who hunt them) to run faster and faster over successive generations because of predator-prey competition. Similarly, after many rounds of play, we would expect the counterfeiter to steadily improve the quality of his fake currency and the police to get more and more effective at spotting fakes.

In essence, this is how GANs work, where: (1) the mint is actually a library of real ground-truth images, (2) the counterfeiter is the "generative neural network" creating fake images that are supposed to look real, and (3) the police officer is the "discriminator neural network" that is able to accurately distinguish real images from the library versus fake images from the generator.

As a side note, most versions of the counterfeiter-police analogy ignore the mint. I find it helpful to specifically call out who is producing the real money.
