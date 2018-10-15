# nn4ent

This project aims at finding the minimal surface in curved space ending on given Dirichlet conditions.

## Motivations

In AdS/CFT many information related quantities are proposed as areas or volumes of extremal geometrical objects. Usually this process could be interpreted as a Euler-Lagrange equation, i.e., PDEs with quite general boundary conditions. 

However, this sort of computation could be time-consuming, or even, finding the minimal surface itself is diffcult enough. In this project we focus on neural network method to solve general minimal surface, in the light of the power of neural network of finding minimum of a given target function and its utilities of the massive power of GPUs. Moreover, the neural network method could be much simpler to solve the minimal surface since it can minimize the Lagrange itself.

## minimal surface and holographic entanglement entropy in general spacetime

Given a spacetime at a time-slice the reduced geometry is space-like, say it is $g_{ab}$ with boundary $S$ at $d$-dimensional space. Consider $A\subset S$ as the configuration of partition.

Then according to Ryu-Takayanagi formalism, the holographic entanglement entropy of $A$ is,
$$S_{A} \sim \text{Area}\left(\tilde A\right)$$
where $\tilde A$ is the minimal surface stretching into the dual gravitational spacetime with $\partial A = \partial \tilde A$. The minimal surface is $d-1$-dimensional surface $\Sigma$ whose area is minimal, with coordinate $\sigma_{1},\sigma_{2},\cdots,\sigma_{d-1}$.
Then we have 
$$S_{A}\sim \text{Min} \left(\int_{\Sigma} \sqrt{h} d\sigma_{1} \cdots d\sigma_{d-1}\right)$$
As can be seen from the above formula, the hologarphic entanglement entropy is to find the surface $\Sigma$ that minimize $S_{A}$.

## Deriving the minimal surface through NN

NN is powerful in this sort of computation due to:

- NN is capable of approximating any continuous function
- The minimal surface cooresponds to minimizing the $S_{A}$ direction, i.e., the action directly, rather than solving a PDE. This observation greatly simplify the computation.
- Minimizing the action can make use of the power of GPU. Instead of typical computation of solving a PDE usually involves massive CPU computations.
