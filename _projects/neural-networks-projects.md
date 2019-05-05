---
title: Neural Networks Projects
layout: page
short: Implementations of a couple of neural network models, before they were
       cool (again).
---
Neural networks are an important (or at least popular) field in artificial
intelligence research. To better understand them, it is useful to implementing
them, and do some experiments with training them. Below are some of the models.

Also remember: this was long before TensorFlow, and we had to implement most of
the functionality from scratch.

## Feedforward neural networks

The feedforward neural networks with the back-propagation algorithm are
probably the most popular type of neural networks. I've implemented this type
of networks once in Java as an assignment project for my Java classes. Later,
I've created another implementation in Visual Basic .NET as a custom
development project. Both implementation were created as object libraries, with
focus on modularity and extensibility. Each part of the network - including the
architecture, transition function and learning algorithms - can be changed
according to your needs.

## Palette reduction with Kohonen networks

While there certainly are better ways how to reduce the number of colors used
in an image, this was a fun (school) project to work on. It was implemented as
a Kohonen self-organizing map in the color space, trained by the colors of the
pixels in the original image. The project included a nice visualisation of the
structure of the network and distribution of the neurons.

## Dithering with Hopfield networks

When reducing the palette in an image to a small number of colors, sharp edges
on the borders of different colors are one of the great problems. To overcome
this problem, multiple dithering algorithms were developed. Again, while there
are much better (and more efficient!) ways how to do dithering, in can also be
done with Hopfield networks. Again, this was a school project - and it was a
lecture on neural networks, not image processing.
