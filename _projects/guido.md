---
title: Guido
layout: page
short: An Unconstrained Influence Diagram solver.
---
An unconstrained influence diagram solver

## About Guido

Guido is an experimental implementation of the Unconstrained Influence Diagram solution method proposed by Jensen and Vomlelová (2002). It was developed as a team software project at Faculty of Mathematics and Physics, under supervision of Mgr. Marta Vomlelová, PhD. The team members were Jiří Iša, Viliam Lisý, Zuzana Reitermanová and Ondřej Sýkora.

## Unconstrained Influence Diagrams

Unconstrained Influence Diagrams (UID) is a framework for description of planning problems using decision, chance and utility variables, and capturing the dependencies between them in terms of conditional probability. Compared to Influence Diagrams, a more classical model known from decision theory and artificial intelligence, UIDs drop the requirement that all decisions must be linearly ordered. This add more flexibility when describing the problems, but also drastically increases the complexity of the problem.

## Solution Method

Compared to solving Influence Diagrams, a part of the solution of an UID is also finding the optimal ordering of decisions. This is done by creating a GS-DAG, a graph that is guaranteed to contain the optimal ordering. However, the size of the graph (in terms of the number of nodes and edges) is super-exponential with respect to the number of decisions of the original UID.
