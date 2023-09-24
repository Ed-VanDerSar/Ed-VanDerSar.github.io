---
title: "The Urn Problem"
mathjax: true
layout: post
---

## How many balls are there at the end of the process?

The Urn Problem was originally stated by the mathematician {John Littlewood}, as a mere puzzle in his 1953 book \textit{Littlewood’s Miscellany} \cite{JL}.
%in the following way:  
%{\small \textit{Balls numbered 1, 2, …  (or for a mathematician the numbers themselves) are put into a box as follows. At 1 minute to noon the numbers 1 to 10 are put in, and the number 1 is taken out. At half a minute to noon numbers 11 to 20 are put in and the number 2 is taken out. At one quarter minute before noon 21 to 30 in and 3 out; and so on. How many are in the box at noon? The answer is none: any selected number, e.g. 100, is absent, having been taken out at the 100th operation.}} 
It was also later extensively analyzed  by Sheldon Ross in his 1988 book \textit{A First Course in Probability}\cite{SR}, who described the probabilistic nature of this problem. The aim of this expository paper is to discus the \textit{Urn Problem} as posed in Ross’s book.

Let us consider the following simplified version of the problem:

{ \small\textit{
We start with an infinite number of balls, numbered. Then, in sequential steps we perform the following experiment: At each step, ten balls are placed in an urn and then one is removed and discarded. The steps are performed so that they are completed in a finite time. The question is, How many balls are in the urn after the end of the process?}
 }


One can immediately say that the answer is that there is an infinite number of balls in the urn by the end of the process. This is in accordance with most people’s intuition, based on the fact that at each step more balls are added than are being removed. We shall see that the answer of the question depends on the way the ball is removed at each step. This might seem \textit{chaotic}. Nevertheless, we will prove that if we study all the possible ways of remove balls at each step with tools provided by probability theory, then we gain a deeper understanding of the nature of this problem.


Suppose that we possess an infinitely large urn and an infinite collection of balls labelled with the natural numbers, i.e., each number corresponds to exactly one ball.
Consider an experiment performed as follows: In the first step, the balls  1 through 10 are placed in the urn and the ball number 10 is removed. In the second step, the balls 11 through 20 are placed in the urn and the ball number 20 is removed. In the third step, the balls 21 through 30 are placed in the urn and the ball number 30 is removed. And so on, and so on. If we assume that we can perform infinitely many steps and that the process ends in a finite time, then the question is, How many balls are in the urn at the end of the process? 

The answer to this question is, according to our intuition, that there is an infinite number of balls at the end of the process, since any ball whose number is not of the form $10n$, for $n\geq 1$, will be placed in the urn and will remain in it until the  end of the process. So, the question is solved if the {experiment} is performed as described.

Now, let us change the experiment  and suppose that in the first step, the balls  1 through 10 are placed in the urn and the ball number 1 is removed. In the second step, the balls  11 through 20 are placed in the urn and the ball number 2 is removed. In the third step, the balls 21 through 30 are placed in the urn and the ball number 3 is removed. In the fourth step, the balls 31 through 40 are placed in the urn and the ball number 4 is removed. And so on, and so on. Again, if we assume that we can perform infinitely many steps and that the process ends in a finite time, then we wonder, How many balls are in the urn at the end of the process?  

Surprisingly, the answer is that the urn is empty at the end of the process! Since any ball is removed of the urn in some step: the ball number 1 is removed en the first step, the ball number 2 is removed in the second step, the ball number 3 is removed in the third step and so on, and  son. So that, the ball number  $n$ will be removed exactly in the $n$th step.  Thus, the fact that any ball is labeled with exactly one natural number implies that the urn shall be empty by the end of the process.

 It seems apparent that the answer to the question, How many balls are in the urn at the end of the process?, depends strongly on the way the balls are removed, even though the ways of removing the balls seem \textit{natural} or \textit{reasonable}.

If we study this problem under probabilistic eyes, we can get a glimpse of the very nature of the urn problem. Let us now suppose that whenever a ball is to be removed, that ball is randomly selected from among those present. That is, suppose that in the firs step, balls numbered 1 through 10 are placed in the urn and a ball is randomly selected and removed, and so on. In this case, how many balls are in the urn at the end of the process?

We shall prove that, whit probability 1, the urn is empty at the end of the process. This implies that almost any way of performing the experiment results in an empty urn, which is astonishing, since for some experiments, which may seem natural, the final answer is not zero.

Let $E_i$ be the event that the ball number $i$ is still in the urn at the process. Lets assume without loss of generality that $10(m-1) < i\leq 10m$ for some $m\geq1$. So, the $i$th ball is in the urn exactly at the $m$th step. Let $F_n$ be event that the $i$th ball remains in the urn after  $n$ successive steps. Thus 
\[
\p{F_n}= \prod_{k=m}^{m+n}\frac{9k}{9k+1}.\]
For example, if $m=1$, then 
\[
\p{F_n}= \frac{9\cdot 18\cdot 27\cdot\cdots\cdot 9n}{10\cdot 19\cdot 28\cdot\cdots\cdot (9n+1)}.\]
This identity is easier to understand since, if ball number  $i$ is still to be in the urn after the first $n$, the first ball removals can be any one of 9 that left, the second any one of 18 (there are 19 balls in the urn at the time of the second removal, one of which must be ball number 1), and so on. 

Given that the events $F_n$ are decreasing and $E_i=\bigcap_{n\geq1}F_n$, it follows from the continuity of probability measure, that 
\[
\p{E_i}=\lim_{n\to\infty}\p{F_n}=\prod_{k\geq m}\frac{9k}{9k+1}.
\]
Since
\begin{equation}\label{eq:infty}
    \prod_{k\geq m}\left(1+\frac{1}{9k}\right)=\infty
\end{equation}
and 
\[
\prod_{k\geq m}\frac{9k}{9k+1}=
\left(\prod_{k\geq m}\left(1+\frac{1}{9k}\right) \right)^{-1},
\]
we know that 
\[
\prod_{k\geq m}\frac{9k}{9k+1}=0
\]
Finally, inasmuch as the event that the urn is not empty at the end of the process is $ \bigcap_{i\geq n}E_i$, it follows that 
\[
\p{\bigcap_{i\geq n}E_i}\leq \sum_{i\geq 1}\p{E_i}=0.
\]
Hence, the urn is empty at the end of the process with probability 1. \hfill $\square$

The identity \eqref{eq:infty} holds due to, for some $M\geq m$ 
\begin{align*}
    \prod_{k\geq m}\left(1+\frac{1}{9k}\right)&\geq \prod_{k= m}^M\left(1+\frac{1}{9k}\right)\\
&>\frac{1}{9m}+\frac{1}{9(m+1)}+\dots+\frac{1}{9M}\\
&=\frac{1}{9}\sum_{k=m}^M\frac{1}{k}.
\end{align*}
Now, in view of the well-known fact that $\displaystyle \sum_{k\geq 1}\frac{1}{k}=\infty$ and taking the limit as $M\to\infty$, its clear that \eqref{eq:infty} holds.





 Ross, S. M. (1998). A First Course in Probability. Pearson Prentice Hall, 2010

 John E. Littlewood. Littlewood's Miscellany. Cambridge University Press, Cambridge, 1986. p. 26. (First published as "A Mathematician's Miscellany" (ed. Béla Bollobás, Methuen \& Co., 1953)

