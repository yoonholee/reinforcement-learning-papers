## Policy Gradient


### Continuous Control with Deep Reinforcement Learning [[ICLR 2016]](https://arxiv.org/pdf/1509.02971)
  - Google Deepmind(Timothy P. Lillicrap, Jonathan J. Hunt, Alexander Pritzel, Nicolas Heess, Tom Erez, Yuval Tassa, David Silver, Daan Wierstra)
  - Videos available [here](https://goo.gl/J4PIAz)
  - Suggests DDPG, which improves the actor-critic algorithm in [Deterministic Policy Gradient Algorithms](https://github.com/yoonholee/Reinforcement-Learning-Survey/blob/master/policy_gradient.md#deterministic-policy-gradient-algorithms-icml-2014) by using a DQN as the critic
  - Empirically shown to be more efficient than DQN
  
### High-dimensional Continuous Control Using Generalized Advantage Functions [[ICLR 2016]](https://arxiv.org/pdf/1506.02438)
  - John Schulman, Philipp Moritz, Sergey Levine, Michael I. Jordan, Pieter Abbeel
  -  Videos available [here](https://sites.google.com/site/gaepapersupp)
  - Derives a class of estimators(GAE) of the advantage function, parameterized by two real numbers in [0,1]
  - Empirical performance of TRPO+GAE is better than TRPO in some tasks

### Trust Region Policy Optimization [[ICML 2015]](https://arxiv.org/pdf/1502.05477)
  - John Schulman, Sergey Levine, Philipp Moritz, Michael Jordan, Pieter Abbeel
  - Builds on [Approximately Optimal Approximate Reinforcement Learning](https://github.com/yoonholee/Reinforcement-Learning-Survey/blob/master/policy_gradient.md#approximately-optimal-approximate-reinforcement-learning-icml-2002)
  - Instead of using a linear mixture, TRPO uses average KL divergence to ensure that the next policy is sufficiently close to current policy(in practice, approximate L linearly and KL divergence quadratically)
  - The natural policy gradient has the same direction as TRPO; the difference is that TRPO chooses a step size based on the trust region defined by KL divergence
  - Empirical performance is comparable to state of the art in both robotic locomotion and atari games
  
### Deterministic Policy Gradient Algorithms [[ICML 2014]](http://jmlr.org/proceedings/papers/v32/silver14.pdf)
  - David Silver, Guy Lever, Nicolas Heess, Thomas Degris, Daan Wierstra, Martin Riedmiller
  - All proofs are in [a seperate document](http://jmlr.org/proceedings/papers/v32/silver14-supp.pdf)
  - Derives a gradient for deterministic policies(assuming a continuous action space)
  - Proves(under mild regularity conditions) that all previously developed machinery for stochastic policy gradients(i.e. compatible function approximation, actor-critic, natural gradients, and episodic/batch methods) are applicable to determinisic policy gradients.
  - Derives deterministic policy gradient algorithms using such machinery

### Reinforcement learning of motor skills with policy gradients [[Neural Networks 2008]](http://is.tuebingen.mpg.de/fileadmin/user_upload/files/publications/Neural-Netw-2008-21-682_4867[0].pdf)
  - Jan Peters, Stefan Schaal
  - An extensive survey of policy gradient methods
  - Covers naive finite-difference methods, REINFORCE, NAC(natural actor-critic)
  - NAC is shown to be the state of the art
  
### Natural Actor-Critic [[Neurocomputing 2008]] (http://ac.els-cdn.com/S0925231208000532/1-s2.0-S0925231208000532-main.pdf?_tid=5001927e-69ce-11e6-87f9-00000aacb35f&acdnat=1472024730_f49e79f185266d4824826941cec13967)
  - Jan Peters, Stefan Schaal
  - Proves that the weight vector discussed in [A Natural Policy Gradient](https://github.com/yoonholee/Reinforcement-Learning-Survey/blob/master/policy_gradient.md#a-natural-policy-gradient-nips-2002) is in fact the natural gradient, rather than just a gradient defined by an average of point fisher information matrices
  - Suggests a actor-critic style algorithm using the natural gradient
  
### A Natural Policy Gradient [[NIPS 2002]](http://papers.nips.cc/paper/2073-a-natural-policy-gradient.pdf)
  - Sham Kakade
  - Parameterizes Q(s,a) as a weighted sum of log p(a|s)
  - Proves that the weight vector(above) is the direction of steepest descent with respect to the expectation of the fisher information matrix(natural policy gradient)
  - Suggests a REINFORCE-style algorithm using the natural gradient
 
### Approximately Optimal Approximate Reinforcement Learning [[ICML 2002]](https://www.cs.cmu.edu/~./jcl/papers/aoarl/Final.pdf)
  - Sham Kakade, John Langford
  - Points out the inefficiency of policy gradients using two example MDPs(section 3.2)
  - Derives a conservative policy iteration scheme that finds a policy that is almost optimal(within epsilon) in polynomial(w.r.t. epsilon) time
  - The key idea is that we can get a provably improved policy by using a linear mixture between the current policy and the greedily improved policy
