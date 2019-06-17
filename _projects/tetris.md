---
title: Tetris
layout: project
short: Tetris-like game with an evil artificial intelligence.
---
The game Tetris is one of the things, every programmer has written (or will
write once). And, as you probably guessed, I'm not an exception. However,
creating a simple tetris game is not exactly exciting, so I've decided to add
something unique. My version of Tetris does not have great graphics, sounds or
music, interesting bonuses, [lemmings](http://dosgamer.com/lemris/), or [almost
naked girls](http://www.offstudio.cz/new/index.php/en/wilma-tetris.html) in it,
but it has an evil artificial intelligence. If you have played Tetris for a
longer time, you surely had the feeling that the game chose the worst possible
pieces, and you were probably wrong. In this version, you would be right.

The principle is simple enough - the game contains an evaluation function that
adds "score" for each gap closed from above (and a special bonus for gaps
closed from all sides) and chooses pieces that lead to highest scores, with
simple planning based on the MiniMax algorithm.
