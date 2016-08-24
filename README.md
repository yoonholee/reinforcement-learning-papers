# Reinforcement Learning Survey

This is a collection of my notes on reinforcement learning papers.


## Table of Contents

- [Policy Gradient](https://github.com/yoonholee/Reinforcement-Learning-Survey#policy-gradient)


## Policy Gradient

### A Natural Policy Gradient [[NIPS 2002]](http://papers.nips.cc/paper/2073-a-natural-policy-gradient.pdf)
  - Sham Kakade
  - Parameterizes Q(s,a) as a weighted sum of log p(a;s)
  - Shows that the weights(above) are the direction of steepest descent with respect to the expectation of the fisher information matrix(natural policy gradient)
  - Implicitly shows(first line of Theorem 3 proof) that the natural policy gradient is a linear approximation of policies with respect to policy parameters

### Reinforcement learning of motor skills with policy gradients [[Neural Networks 2008]](http://is.tuebingen.mpg.de/fileadmin/user_upload/files/publications/Neural-Netw-2008-21-682_4867[0].pdf)
  - Jan Peters, Stefan Schaal
  - An extensive survey of policy gradient methods
  - Covers naive finite-difference methods, REINFORCE, NAC(natural actor-critic)
  - NAC is shown to be the state of the art
