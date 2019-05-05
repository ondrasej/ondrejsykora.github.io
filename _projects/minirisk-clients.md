---
title: Minirisk Clients
layout: page
short: AI implementations for the game Minirisk.
---
Minirisk is a simple bidding card game for two to five players. Though the game itself is fun, it does much better job as a platform for testing AI algorithms. The game is simple enough to be analysed in various ways, but it is complex enough for better algorithms to make a difference at the same time. Minirisk is mostly about finding the optimal strategy against the current opponent(s), which makes it an ideal platfom for testing learning and opponent modelling algorithms.

Jiří Iša built an open-source client/server platform for the game, and also maintains a web page with detailed description of the game and existing agents.

I've created two agents based on the idea, that a good strategy can be found by predicting future actions of the opponents from the actions they performed before. Both clients measure the frequencies, how many times each player used a certain currency card for a given deck card.

## Memory client

Memory client assumes that the opponent will continue to use the same strategy as it used before. More precisely - it expects the opponent to use the currency card, that they most frequently used in this situation in previous games. Given the expected currency card used by the opponent, Memory uses the +1 strategy to outbid it.

## MemoryMC client

MemoryMC client uses the information about the strategy of the opponent to estimate the expected gain from playing each currency card it has available. Then, it plays the most promising card. It uses a Monte Carlo simulation to do that - the value of a currency card is calculated as the expected gain from the whole game, if the player uses that card in the current round. This combination of opponent modeling and "planning" proves to be rather difficult to beat.
