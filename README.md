# Reinforcement Learning Survey

This is a collection of my notes on reinforcement learning papers.

Typo corrections, additional points, new papers etc are all very welcome. You can either make a pull request or email me at einet89[at]postech.ac.kr


## Table of Contents

- [Policy Gradient](https://github.com/yoonholee/Reinforcement-Learning-Survey#policy-gradient)
- [Q-Learning](https://github.com/yoonholee/Reinforcement-Learning-Survey#q-learning)
- [Imitation Learning](https://github.com/yoonholee/Reinforcement-Learning-Survey#imitation-learning)


## Policy Gradient

### Approximately Optimal Approximate Reinforcement Learning [[ICML 2002]](https://www.cs.cmu.edu/~./jcl/papers/aoarl/Final.pdf)
  - Sham Kakade, John Langford
  - Points out the inefficiency of policy gradients using two example MDPs(section 3.2)
  - Derives a conservative policy iteration scheme that finds a policy that is almost optimal(within epsilon) in polynomial(w.r.t. epsilon) time
  - The key idea is that by using a mixture between the current policy and a greedily improved policy, we can prove that the value function improves

### A Natural Policy Gradient [[NIPS 2002]](http://papers.nips.cc/paper/2073-a-natural-policy-gradient.pdf)
  - Sham Kakade
  - Parameterizes Q(s,a) as a weighted sum of log p(a;s)
  - Proves that the weight vector(above) is the direction of steepest descent with respect to the expectation of the fisher information matrix(natural policy gradient)
  - Implicitly shows(first line of Theorem 3 proof) that the natural policy gradient is a linear approximation of policies with respect to policy parameters
  - Suggests a REINFORCE-style algorithm using the natural gradient
  
### Natural Actor-Critic [[Neurocomputing 2008]] (http://ac.els-cdn.com/S0925231208000532/1-s2.0-S0925231208000532-main.pdf?_tid=5001927e-69ce-11e6-87f9-00000aacb35f&acdnat=1472024730_f49e79f185266d4824826941cec13967)
  - Jan Peters, Stefan Schaal
  - Proves that the weight vector discussed in [A Natural Policy Gradient](https://github.com/yoonholee/Reinforcement-Learning-Survey#a-natural-policy-gradient-nips-2002) is in fact the natural gradient, rather than just a gradient defined by an average of point fisher information matrices
  - Suggests a actor-critic style algorithm using the natural gradient

### Reinforcement learning of motor skills with policy gradients [[Neural Networks 2008]](http://is.tuebingen.mpg.de/fileadmin/user_upload/files/publications/Neural-Netw-2008-21-682_4867[0].pdf)
  - Jan Peters, Stefan Schaal
  - An extensive survey of policy gradient methods
  - Covers naive finite-difference methods, REINFORCE, NAC(natural actor-critic)
  - NAC is shown to be the state of the art
  
### Deterministic Policy Gradient Algorithms [[ICML 2014]](http://jmlr.org/proceedings/papers/v32/silver14.pdf)
  - David Silver, Guy Lever, Nicolas Heess, Thomas Degris, Daan Wierstra, Martin Riedmiller
  - All proofs are in [a seperate document](http://jmlr.org/proceedings/papers/v32/silver14-supp.pdf)
  - Derives a gradient for deterministic policies(assuming a continuous action space)
  - Proves(under mild regularity conditions) that all previously developed machinery for stochastic policy gradients(i.e. compatible function approximation, actor-critic, natural gradients, and episodic/batch methods) are applicable to determinisic policy gradients.
  - Derives deterministic policy gradient algorithms using such machinery

### Trust Region Policy Optimization [[ICML 2015]](https://arxiv.org/pdf/1502.05477)
  - John Schulman, Sergey Levine, Philipp Moritz, Michael Jordan, Pieter Abbeel
  - Builds on [Approximately Optimal Approximate Reinforcement Learning](https://github.com/yoonholee/Reinforcement-Learning-Survey#approximately-optimal-approximate-reinforcement-learning-icml-2002)
  - Instead of using a linear mixture, TRPO uses average KL divergence to ensure that the next policy is sufficiently close to current policy(the algorithm approximates L linearly and KL divergence quadratically)
  - The natural policy gradient has the same direction as TRPO; the difference is the step size choosing scheme of TRPO
  - Empirical performance is comparable to state of the art in both robotic locomotion and atari games
  
### High-dimensional Continuous Control Using Generalized Advantage Functions [[ICLR 2016]](https://arxiv.org/pdf/1506.02438)
  - John Schulman, Philipp Moritz, Sergey Levine, Michael I. Jordan, Pieter Abbeel
  -  Videos available [here](https://sites.google.com/site/gaepapersupp)
  - Derives a class of estimators(GAE) of the advantage function, parameterized by two real numbers in [0,1]
  - Empirical performance of TRPO+GAE is better than TRPO in some tasks

### Continuous Control with Deep Reinforcement Learning [[ICLR 2016]](https://arxiv.org/pdf/1509.02971)
  - Google Deepmind(Timothy P. Lillicrap, Jonathan J. Hunt, Alexander Pritzel, Nicolas Heess, Tom Erez, Yuval Tassa, David Silver, Daan Wierstra)
  - Videos available [here](https://goo.gl/J4PIAz)
  - Suggests DDPG, which improves the actor-critic algorithm in [Deterministic Policy Gradient Algorithms](https://github.com/yoonholee/Reinforcement-Learning-Survey#deterministic-policy-gradient-algorithms-icml-2014) by using a DQN as the critic
  - Empirically shown to be far more efficient than DQN
 

## Q Learning

### On the Convergence of Stochastic Iterative Dynamic Programming Algorithms [[NIPS 1994]](http://papers.nips.cc/paper/764-convergence-of-stochastic-iterative-dynamic-programming-algorithms.pdf)
  - Tommi Jaakkola, Michael I. Jordan, Satinder P. Singh
  - Proves the convergence of Q-Learning to optimal Q values given some mild regulatory conditions
  - Gives a similar proof for TD(lambda)
  

## Imitation Learning

### Algorithms for Inverse Reinforcement Learning [[ICML 2000]](http://citeseerx.ist.psu.edu/viewdoc/download;jsessionid=4C4D16E1D96E10A07A1EFFD5D64C7C68?doi=10.1.1.41.7513&rep=rep1&type=pdf)
  - Andrewy Y. Ng, Stuart Russell
  - Reduces to IRL(Inverse Reinforcement Learning) to a LP(linear programming) problem, and introduces a penalty term to choose a reward function within the class obtained from LP
  - Experiments show promising results on simple enviornments
  
### Guided Policy Search [[ICML 2013]](https://graphics.stanford.edu/projects/gpspaper/gps_full.pdf)
  - Sergey Levine, Vladlen Koltun
  - Videos available [here](https://graphics.stanford.edu/projects/gpspaper/index.htm)
  - Derives a scheme that, given a trajectory, constructs a policy that produces trajectories close to it(using iterative LQR and adding theoretically justified noise)
  - Descibes the Guided Policy Search algorithm, which is designed to explore around the given trajectories and find a good policy

### Model-Free Imitation Learning with Policy Optimization[[ICML 2016]](https://arxiv.org/pdf/1605.08478)
  - Jonathan Ho, Jayesh K. Gupta, Stefano Ermon
  - Given a class of reward functions, find the policy that maximizes the minimum advantage against expert policy over the whole class
  - Suggests two algorithms, IM-REINFORCE and IM-TRPO, both of which iteratively find better and better policies
