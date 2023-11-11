---
tags:
  - polynomials
  - functions
  - graphs
date: 2023-10-15
source: "[[James Stewart Precalculus.pdf]]"
page: 257
aliases:
  - end behavior
---
The behavior of a [[Polynomial Functions|polynomial function]] when it **approaches** infinity can be defined with this fancy ass notation:
- $x \rightarrow \infty$  $x$ increases without bound
- $x \rightarrow -\infty$ $x$ decreases without bond
The end behavior of the polynomial $P(x) = a_{n}x^{n}+ a_{n-1}x^{n-1}+ \cdots + a_{1}x + a_{0}$ is mainly driven by the **leading term**, i mean, when something approaches infinity, the term with the highest power will shadow the others, making them almost insignificant so we can safely guide ourselves by the leading term.
#### Four Types of Behavior
After all those ups and downs of this weird looking function we end up with **four** common behaviors, splitting into **two** cases, **even and odd**, and both being **negative or positive**:
Let $P$ be a polynomial function.
- When $P$ has **odd** degree: 
	- Leading coefficient **positive**:
		- $y \rightarrow \infty$ as $x \rightarrow \infty$ 
		- $y \rightarrow -\infty$ as $x \rightarrow -\infty$ 
	- Leading coefficient **negative**:
		- $y \rightarrow \infty$ as $x \rightarrow -\infty$ 
		- $y \rightarrow -\infty$ as $x \rightarrow \infty$

- When $P$ has **even** degree:
	- Leading coefficient **positive**:
		- $y \rightarrow \infty$ as $x \rightarrow -\infty$
		- $y \rightarrow \infty$ as $x \rightarrow \infty$  
	- Leading coefficient **negative**:
		- $y \rightarrow -\infty$ as $x \rightarrow -\infty$
		- $y \rightarrow -\infty$ as $x \rightarrow \infty$   