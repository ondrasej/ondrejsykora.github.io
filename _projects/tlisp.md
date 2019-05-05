---
title: TLisp
layout: page
short: A LISP-like scripting language created for Trion Team games.
---
When working on the game Projekt 5410, we needed a scripting language for creating levels. The basic structure of the levels (the terrain, placement of enemies and bonuses, background music, etc.) was described in XML format, but we needed more to create more dynamic worlds.

I've evaluated multiple languages, including Java and Python for the job, but I've ultimately decided to create my own, as small and simple as possible, designed to interface well with the game data structures. LISP was chosen because of its simplicity and extensibility of the language without the need to change anything in the compiler itself.

The interpreter itself is designed with respect to game scripting - it is high-level oriented, but with a very fast allocator and generational garbage collector. It would not stand a chance against commercial LISP compilers, but as game scripts are mostly trivial, it works just fine. Moreover, the garbage collection can be finely tuned and it is guaranteed that it never takes too much time to break the frame rate in the game.
