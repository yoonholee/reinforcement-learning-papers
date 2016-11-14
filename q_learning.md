## Q Learning
  
### Dueling Network Architectures for Deep Reinforcement Learning [[ICML 2016]](https://arxiv.org/pdf/1511.06581.pdf)
  - Ziyu Wang, Tom Schaul, Matteo Hessel, Hado van Hasselt, Marc Lanctot, Nando de Freitas
  - ICML 2016 Best Paper
  - Two-stream DQN, each representing V(value function) and A(advantage function)
  - Elinimates the instability of adding two numbers of different scale(V is usually much larger than A)
  - Updates actions more frequently than a single-stream DQN, where only a single Q value is updated for each observation
  - Implicitly splits the credit assignment problem into a recursive binary problem of "now or later"
  - Arguably the first major breakthrough in network architectures specifically for deep RL
  - Only works for finite action spaces
  
### Deep Exploration via Bootstrapped DQN [[NIPS 2016]](https://arxiv.org/pdf/1602.04621v3.pdf)

  - Ian Osband, Charles Blundell, Alexander Pritzel, Benjamin Van Roy
  
### Prioritized Experience Replay [[ICLR 2016]](https://arxiv.org/pdf/1511.05952.pdf)
  - Tom Schaul, John Quan, Ioannis Antonoglou, David Silver
  - Samples (s,a,r,s') tuples with probability proportional to their TD error
  - Uses a 'sum-tree' data structure to perform this quickly, where the value of a parent node is the sum of its children
  - Uses importance sampling weights to counteract the change in state distribution
  - Inspired by prioritized sweeping
  
### Deep Reinforcement Learning with Double Q-Learning [[AAAI 2016]](https://arxiv.org/pdf/1509.06461.pdf)
  - Hado van Hasselt, Arthur Guez, David Silver
  - Points out that once [DQN](https://github.com/yoonholee/Reinforcement-Learning-Survey/blob/master/q_learning.md#playing-atari-with-deep-reinforcement-learning-nips-2014-deep-learning-workshop) overestimates a Q value, the overestimation 'spills over' to states that precede it
  - Uses different Q networks for action selection and evaluation
  - Empirically shows that Double DQN outperforms DQN
  
### Human-level Control Through Deep Reinforcement Learning [[Nature 2015]](http://home.uchicago.edu/~arij/journalclub/papers/2015_Mnih_et_al.pdf)
  - Volodymyr Mnih, Koray Kavukcuoglu, David Silver, Andrei A. Rusu, Joel Veness, Marc G. Bellemare, Alex Graves, Martin Riedmiller, Andreas K. Fidjeland, Georg Ostrovski, Stig Petersen, Charles Beattie, Amir Sadik, Ioannis Antonoglou, Helen King, Dharshan Kumaran, Daan Wierstra, Shane Legg & Demis Hassabis
  - Appeared earlier in [NIPS 2013 Deep Learning Workshop](https://arxiv.org/pdf/1312.5602.pdf)
  - Proposes using a deep convolutional network for Q-learning
  - Uses experience replay(similar to  [Neural Fitted Q Iteration](https://github.com/yoonholee/Reinforcement-Learning-Survey/blob/master/q_learning.md#neural-fitted-q-iteration---first-experiences-with-a-data-efficient-neural-reinforcement-learning-method-ecml-2005)), storing only the last N experience tuples while using an epsilon greedy policy
  - Points out that a scheme similar to experience replay happens in the hippocampus of the mammalian brain
  - Difference with [Neural Fitted Q Iteration](https://github.com/yoonholee/Reinforcement-Learning-Survey/blob/master/q_learning.md#neural-fitted-q-iteration---first-experiences-with-a-data-efficient-neural-reinforcement-learning-method-ecml-2005)) is that this is an off-policy learning algorithm where the network determines the policy
  - Periodically fixes network parameters for stability
  - Mentions multiple times that a scheme similar to prioritized sweeping would speed up convergence, which is exactly [Prioritized Experience Replay](https://github.com/yoonholee/Reinforcement-Learning-Survey/blob/master/q_learning.md#prioritized-experience-replay-iclr-2016)
  
### Deep Recurrent Q-Learning for Partially Observable MDPs [[arxiv 2015]](https://arxiv.org/pdf/1507.06527v3.pdf)
  - Matthew Hausknecht, Peter Stone
  - Attaches an LSTM to a standard DQN, so that it can learn even with only timestep as input
  - Experiments show that this is superior to DQN in an env where at each timestep, the state is obscured with probability 1/2
  
### Neural Fitted Q Iteration - First Experiences with a Data Efficient Neural Reinforcement Learning Method [[ECML 2005]](http://ml.informatik.uni-freiburg.de/_media/publications/rieecml05.pdf)
  - Martin Riedmiller
  - Proposes using a neural network for Q-learning
  - Input is a set of (s,a,s') and the neural network does RProp until convergence
  - Closer to supervised learning than reinforcement learning, since the algorithm never acts

### Convergence of Stochastic Iterative Dynamic Programming Algorithms [[NIPS 1994]](http://papers.nips.cc/paper/764-convergence-of-stochastic-iterative-dynamic-programming-algorithms.pdf)
  - Tommi Jaakkola, Michael I. Jordan, Satinder P. Singh
  - Proves the convergence of Q-Learning to optimal Q values given some mild regulatory conditions
  - Gives a similar proof for TD(lambda)
  
