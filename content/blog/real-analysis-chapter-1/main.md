---
title: "Real Analysis - Some key results from chapter 1 and 2 (W. Rudin, 3rd edition)"
author: "Prashant K. Jha"
draft: true
summary: "Collect some important results from different chapters of Principles of Mathematical Analysis by W. Rudin"
date: 2021-04-20
bibliography: "bibliography.bib"
link-citations: true
featured: true
slug: real-analysis-cap-1-2
reading_time: true
categories: ["Blog", "Theory", "Real Analysis"]
tags: ["Real Analysis", "Theory"]
header:
  caption: ''
  image: ''

header-includes: |
    \usepackage[papersize={4.5in,6in},margin=0.5cm]{geometry}
    \setlength{\parskip}{2pt}
    \usepackage{fourier-orns}
    \newcommand\textbreak{%
    \begin{center}%
    \decothreeleft \aldineleft \decosix \aldineright \decothreeright%
    \end{center}}
    \pagestyle{empty}
    \usepackage[most]{tcolorbox}
    \definecolor{light-yellow}{rgb}{1, 0.95, 0.7}
    \newtcolorbox{myquote}{colback=light-yellow,grow to right by=-10mm,grow to left by=-10mm, boxrule=0pt,boxsep=0pt,breakable}
    \newcommand{\todo}[1]{\begin{myquote} \textbf{TODO:} \emph{#1} \end{myquote}}
---

> :mega: **Remark**: I come from an Engineering background, and I am very interested in Applied mathematics and, in particular Functional Analysis. I spend most of my time on modeling and computational aspects of the problems, and therefore, I find it hard to keep track of some of the main results from purely mathematical subjects. In this series of blogs, I plan to record the key results from Rudin's Real Analysis book. I plan to do the same for Measure Theory, Topology, Functional Analysis, etc.

> Results from chapter 1 and 2 of Principles of Mathematical Analysis by W. Rudin, 3rd edition

> We will use symbols :high_brightness:, :mega:, :bulb: for definition, remark, and theorem.

| :high_brightness: Definition |
|:---------------------------|
| Define |

| :bulb: Theorem |
|:---------------------------|
| Define |

| :mega: Remark |
|:---------------------------|
| Define |

## Ordered sets and fields


---
Definition :high_brightness: **Order**


Let $S$ be a set. An *order* on $S$ is a relation, denoted by $<$, with the following two properties: 

  1. If $x\in S$ and $y\in S$ then one and only one of the statements $$x < y, \quad x = y, \quad y < x$$ is true.

  2. If $x,y,z\in S$, if $x< y$ and $y < z $, then $x < z $.

---

---
Definition :high_brightness: **Ordered set**

An *ordered set* is a set $S$ in which an order is defined.

---

---
:high_brightness: **Bounded above and upper bound**

Suppose $S$ is an ordered set, and $E \subset S$. If there exists a $\beta \in S$ such that $x\leq \beta$ ($x\leq \beta$ means either $x< \beta$ or $x = \beta$), we say that $E$ is *bounded above*, and call $\beta$ an *upper bound* of $E$.

> Lower bounds are defined in the same way (with $\geq$ in place of $\leq$).

---

---
Definition :high_brightness: **Supremum and infimum**

Suppose $S$ is an ordered set, $E \subset S$, and $E$ is bounded above. Suppose there exists an $\alpha \in S$ with the following properties:

  1. $\alpha$ is an upper bound of $E$.
  2. $\gamma < \alpha$ then $\gamma$ is not an upper bound of $E$.

Then $\alpha$ is the *least upper bound of* $E$ [that there is at most one such $\alpha$ is clear from (2)] or the *supremum of* $E$, and we write
$$ \alpha = \sup E .$$

The *greatest lower bound*, or *infimum*, of a set $E$ which is bounded below is defined in the same manner: The statement
$$\alpha = \inf E$$
means that $\alpha$ is a lower bound of $E$ and that no $\beta $ with $\beta > \alpha$ is a lower bound of $E$.

---

---
Definition :high_brightness: **Least upper bound property**

An *ordered set* $S$ is said to have the *least-upper-bound property* if the following is true:

If $E \subset S$, $E$ is not empty, and $E$ is bounded above, then $\sup E$ exists in $S$.

---

---
Theorem :bulb: **Greates lower bound property**

Suppose $S$ is an ordered set with the *least-upper-bound property*, $B\subset S$, $B$ is not empty, and $B$ is bounded below. Let $L$ be the set of all lower bounds of $B$. Then
$$ \alpha = \sup L $$
exists in $S$, and $\alpha = \inf B$. 

In particular, $\inf B$ exists in $S$.

---
