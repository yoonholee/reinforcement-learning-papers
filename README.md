# Reinforcement Learning Survey

This is a collection of my notes on reinforcement learning papers.


## Table of Contents

- [Policy Gradient](https://github.com/yoonholee/Reinforcement-Learning-Survey#policy-gradient)


## Policy Gradient

### A Natural Policy Gradient [[NIPS 2002]](http://papers.nips.cc/paper/2073-a-natural-policy-gradient.pdf)
  - Sham Kakade
  - Parameterizes Q(s,a) as a weighted sum of log p(a;s)
  - Proves that the weight vector(above) is the direction of steepest descent with respect to the expectation of the fisher information matrix(natural policy gradient)
  - Implicitly shows(first line of Theorem 3 proof) that the natural policy gradient is a linear approximation of policies with respect to policy parameters
  - Suggests a REINFORCE-style algorithm using the natural gradient
  
### Natural Actor-Critic [[Neurocomputing 2008]] (http://ac.els-cdn.com/S0925231208000532/1-s2.0-S0925231208000532-main.pdf?_tid=5001927e-69ce-11e6-87f9-00000aacb35f&acdnat=1472024730_f49e79f185266d4824826941cec13967)
  - Jan Peters, Stefan Schaal
  - Proves that the weight vector discussed in [A Natural Policy Gradient](https://github.com/yoonholee/Reinforcement-Learning-Survey#a-natural-policy-gradient) is in fact the natural gradient, rather than just a gradient defined by an average of point fisher information matrices
  - Suggests a actor-critic style algorithm using the natural gradient

### Reinforcement learning of motor skills with policy gradients [[Neural Networks 2008]](http://is.tuebingen.mpg.de/fileadmin/user_upload/files/publications/Neural-Netw-2008-21-682_4867[0].pdf)
  - Jan Peters, Stefan Schaal
  - An extensive survey of policy gradient methods
  - Covers naive finite-difference methods, REINFORCE, NAC(natural actor-critic)
  - NAC is shown to be the state of the art
