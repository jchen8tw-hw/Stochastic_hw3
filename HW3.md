# HW3

##### R11922045 資工碩一陳昱行

## Problem 1

After 10000 trials, we can see that the simulated distrubution is asymptotically uniform distrubution.

![image](/Users/Mac/github/Stochastic%20Process/Image/Problem1.png)

## Problem 2

From bayesian's rule we know that

$$
P(node\ i\ is\ last) = P(from\ i-1)*P(i\ last|from\ i-1) + \\ P(from\ i+1)*P(i\ last|from\ i+1) 
$$

and if the visiting order is $i+1 \rightarrow i$ , that means we must visit all the `m-1` nodes that are on the left hand side of $node\ i+1$ except $node\ i-1$

e.g

$$
node\ i+1, i+2 .... m,0 ,1 ,2 .... i-2
$$

Therefore,

$$
P(i\ last|from\ i+1)  = P(visiting\ m-1\ left\ nodes\ first)
$$

and by symmetry of both direction

$$
P(i\ last|from\ i+1)  = P(visiting\ m-1\ left\ nodes\ first) \\ = P(i\ last|from\ i-1) = p
$$



and also the symmetry of each node (except for the starting node 0)

$$
\forall\ node\ i \neq 0,\ P(node\ i\ is\ last) = p
$$

We can conclude that

$$
P(node\ i\ is\ last) = p = \frac{1}{m}
$$





## Problem 3

Choose `n=100` and `k=0` 

if `p`  is set to 0.5, the probability of reaching  upper band and lower band are equal which is

$$
\frac{n}{n+k} = \frac{50}{100} = \frac{1}{2}
$$

![image](/Users/Mac/github/Stochastic%20Process/Image/Problem3-1.png)

but slightly tweaking `p` to 0.6, the probability of reaching upper band and lower band change dramatically with zero trials hit the lower band.

![image](/Users/Mac/github/Stochastic%20Process/Image/Problem3-2.png)

## Problem 4

Given `A=1` and `B=2`

when $\Delta t = 0.1$ 

![image](/Users/Mac/github/Stochastic%20Process/Image/problem4-1.png)

when $\Delta t = 0.01$

![image](/Users/Mac/github/Stochastic%20Process/Image/problem4-2.png)

when $\Delta t = 0.001$

![image](/Users/Mac/github/Stochastic%20Process/Image/problem4-3.png)

we can see that as $\Delta t$ becomes smaller

the distribution becomes more closer to the distrubution given from the formula

$$
P(up\ A\ before\ down\ B) = \frac{B}{A+B}
$$

## Appendix:

The experiment result and code are placed [here](http://github.com/jchen8tw-hw/Stochastic_hw3) on github.
