## Hierarchical Reinforcement Learning

### The Predictron: End-To-End Learning and Planning [[arXiv 2016]](https://arxiv.org/pdf/1612.08810.pdf)
  - Proposes a NN architecture capable of learning an internal MRP and outputting value estimates
  - Shows that the NN queries different depths on different tasks
  
### Stochastic Neural Networks for Hierarchical Reinforcement Learning [[ICLR 2017]](https://arxiv.org/pdf/1704.03012.pdf)
  - Uses a stochastic neural network to learn skills before task is presented(pre-training)
  - Trains skills by maximizing channel capacity
  - Solves continuous control tasks that were previously unsolved
  
### Surprise-based Intrinsic Motivation for Deep Reinforcement Learning [[ICLR 2017]](https://arxiv.org/pdf/1703.01732.pdf)
  - Introduces an additional reward term proportional to how unexpected the state transition was to the agent's model
  
### Strategic Attentive Writer for Learning Macro-Actions [[NIPS 2016]](https://arxiv.org/pdf/1606.04695v1.pdf)
  - Develops an algorithm that learns to plan sequences of actions in addition to their level of commitment
  - Only works for finite action spaces and a predetermined timeline
  
### Hierarchical Deep Reinforcement Learning: Integrating Temporal Abstraction and Intrinsic Motivation [[NIPS 2016]](https://arxiv.org/pdf/1604.06057v2.pdf)
  - Introduces h-DQN, a deep network version of the options framework
  - Uses hardwired goals(similar to 'salient events' from Singh 2004)

### The Option-Critic Architecture [[NIPS Workshop 2015]](https://arxiv.org/pdf/1609.05140v1.pdf)
  - Derives policy gradient theorems for options

### Intrinsically Motivated Reinforcement Learning [[NIPS 2004]](http://web.eecs.umich.edu/~baveja/Papers/FinalNIPSIMRL.pdf)
  - Intrinsic motivation suggests that there is value in defining options independently of the task
  - The agent creates options to achieve 'salient events': events that are predetermined to be inherently interesting to the agent

### Recent Advances in Hierarchical Reinforcement Learning [[DEDS 2003]](http://www-anw.cs.umass.edu/pubs/2003/barto_m_DEDS03.pdf)
  - Summarizes three approaches to hierarchical RL: options, HAMs, MAXQ
  
### Learning Options in Reinforcement Learning [[ISARA 2002]](http://ftp.bstu.by/ai/To-dom/My_research/Papers-0/For-research/R-navigation/Grid-world/Good-one/stolle2002learning.pdf)
  - Learns options by randomly specifying a task and making the most frequently visited state the termination condition of an option.
  
### Between MDPs and semi-MDPs: A Framework for Temporal Abstraction in Reinforcement Learning [[Artificial Intelligence Journal 1999]](http://www-anw.cs.umass.edu/~barto/courses/cs687/Sutton-Precup-Singh-AIJ99.pdf)
  - Defines an option as a policy with a termination and initiation condition
  - Proves that using options instead of only the primitive actions on an MDP is an SMDP problem
  - Proves that allowing interruption of options increases return
  - Derives and proves convergence of option Q-learning
  - Shows an environment where predefined options considerably shortens learning
  
### Learning Macro-Actions in Reinforcement Learning [[NIPS 1998]](https://papers.nips.cc/paper/1586-learning-macro-actions-in-reinforcement-learning.pdf)
  - Lets previous action influence the choice of action
  - Defines modified Q-value which is a linear combination of Q(s_t, a_t) and Q(a_t-1, a_t)
