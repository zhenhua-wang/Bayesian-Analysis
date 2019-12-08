Beta-Binomial model
-------------------

Suppose the outcome of each observation is either 1 or 0 according to a
unknown parameter *θ*. This dataset could be modeled as a binomial
sampling model.

$$
\\begin{aligned}
y\_1, ..., y\_n \| \\theta \\sim Binomial(n, \\theta)
\\end{aligned}
$$

To find the conjugate prior for *θ*, we rewrite distribution of sampling
model proportional to *θ*.

$$
\\begin{aligned}
P(y\_1, ..., y\_n\|theta) 
&\\propto \\theta^{\\sum{y\_i}} (1-\\theta)^{n - \\sum{y\_i}}
\\end{aligned}
$$

Clearly, its conjugate prior belongs to “beta family”. (Same as before,
we only consider the terms related to *θ*)

$$
\\begin{aligned}
P(\\theta) 
&= dbeta(\\theta, a, b) \\\\
&\\propto \\theta^{a-1}(1-\\theta)^{b-1}
\\end{aligned}
$$

Then, we could compute its posterior distribution easily.

$$
\\begin{aligned}
P(\\theta\|y\_1, ..., y\_n) 
&\\propto P(y\_1, ..., y\_n\|\\theta)P(\\theta) \\\\
&\\propto \\theta^{\\sum{y\_i}} (1-\\theta)^{n - \\sum{y\_i}}
\\end{aligned}
$$
