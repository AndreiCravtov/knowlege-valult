There are a few tests that can be performed on [[Series|series]] to determine if they are convergent or divergent. However some of these tests can be inconclusive.

# Tests for Positive Terms
These tests will only concern series of the type $\sum ^\infty_{i=1} a_{i}$ where all $a_{i}>0$. This implies that the [[Series#Partial sums|partial sum]] $S_{n} = \sum^n_{i=1} a_{i}$ is an increasing series, so we can apply the [[Monotone Convergence Theorem|monotone convergence theorem]] to see that, $$S_{n} \ \text{is bounded} \iff S_{n} \ \text{converges}$$
For all upcoming tests, we use:
- $\sum ^\infty_{i=1} a_{i}$ with $a_{i} > 0$, to denote the series, the convergence/divergence of which, we want to establish
- $\sum ^\infty_{i=1} c_{i}$ with $c_{i} > 0$, to denote some convergent series
- $\sum ^\infty_{i=1} d_{i}$ with $d_{i} > 0$, to denote some divergent series

## Comparison Test
Let $\lambda > 0$ and $N \in \mathbb{N}$. Then we have the following rules
1. $\forall i>N(\ a_{i} \leq \lambda c_{i} \ ) \implies \sum ^\infty_{i=1} a_{i} \ \text{converges}$
2. $\forall i>N(\ a_{i} \geq \lambda d_{i} \ ) \implies \sum ^\infty_{i=1} a_{i} \ \text{diverges}$

## Limit Comparison Text
Sometimes relying on a scaling factor is annoying, so we can use
1. $\lim_{ i \to \infty } \frac{a_{i}}{c_{i}} \in \mathbb{R} \implies \sum ^\infty_{i=1} a_{i} \ \text{converges}$
2. $\lim_{ i \to \infty } \frac{d_{i}}{a_{i}} \in \mathbb{R} \implies \sum ^\infty_{i=1} a_{i} \ \text{diverges}$

## D’Alembert’s Ratio Test
Let $N \in \mathbb{N}$. Then we have the following rules
1. $\forall i>N\left( \ \frac{a_{i+1}}{a_{i}} \geq 1 \  \right) \implies \sum ^\infty_{i=1} a_{i} \ \text{diverges}$
2. $\exists k<0, \forall i>N\left( \ \frac{a_{i+1}}{a_{i}} \leq k \  \right) \implies \sum ^\infty_{i=1} a_{i} \ \text{converges}$
This test is kind of hard to use, and mostly exits as a way to prove the correctness of it's easier to use [[#D’Alembert Limit Ratio Test|limit version]].

## D’Alembert Limit Ratio Test
We have the following rules
1. $\lim_{ i \to \infty } \frac{a_{i+1}}{a_{i}}>1 \implies \sum ^\infty_{i=1} a_{i} \ \text{diverges}$
2. $\lim_{ i \to \infty } \frac{a_{i+1}}{a_{i}}<1 \implies \sum ^\infty_{i=1} a_{i} \ \text{converges}$
3. Otherwise, the test is inconclusive

## Integral Test
Define $f(n) = a_{n}$, and extend it to the reals. So we have $f: \mathbb{R} \to \mathbb{R}^+$. Then, assuming $f$ is even integrable, we have the rules
1. $\int^\infty_{N} f(x)  \, dx \ \text{converges} \implies \sum^\infty_{i=1} a_{i} \ \text{converges}$
2. $\int^\infty_{N} f(x)  \, dx \ \text{diverges} \implies \sum^\infty_{i=1} a_{i} \ \text{diverges}$

# Other Tests
Sometimes we are dealing with the series $\sum ^\infty_{i=1} a_{i}$ where $a_{i}$ may be $0$ or even negative. These are the tests to deal with such cases

## Absolute Value Comparison Test
For some convergent series $\sum ^\infty_{i=1} c_{i}$ with $c_{i} \geq 0$, then we have $$\forall i \geq 1 \left( \ |a_{i}| < c_{i} \  \right) \implies \sum ^\infty_{i=1} a_{i} \ \text{is convergent}$$

## Limit Absolute Value Ratio Test
This test is only applicable if $a_{i} \ne 0$ for all $i\geq 1$. We have the rules
1. $\lim_{ i \to \infty } \left| \frac{a_{i+1}}{a_{i}} \right| < 1 \implies \sum^\infty_{i=1} a_{i} \ \text{is absolutely convergent}$
2. $\lim_{ i \to \infty } \left| \frac{a_{i+1}}{a_{i}} \right| > 1 \implies \sum^\infty_{i=1} a_{i} \ \text{is divergent}$
3. Otherwise, the test is inconclusive

## The $n^{\text{th}}$-root test for convergence
Sometimes, the limit of $\frac{a_{n+1}}{a_{n}}$ does not exist, but the sequence still converges. For these cases, even though the limit doesn't exist, the [[Limit Superior and Limit Inferior|limit superior]] might.
1. $\limsup_{n \to \infty}|a_{n}|^{1/n}<1 \implies \sum^\infty_{n=1} a_{n} \ \text{converges absolutely}$
2. $\limsup_{n \to \infty}|a_{n}|^{1/n}>1 \implies \sum^\infty_{n=1} a_{n} \ \text{diverges}$
3. Otherwise, the test is inconclusive