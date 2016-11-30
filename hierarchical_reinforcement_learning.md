## Hierarchical Reinforcement Learning
### Surprise-based Intrinsic Motivation for Deep Reinforcement Learning [[review ICLR 2017]](https://openreview.net/pdf?id=Bk8aOm9xl)
  - Joshua Achiam & Shankar Sastry
  
### Exploration: A Study of Count-Based Exploration for Deep Reinforcement Learning[[review ICLR 2017]](https://arxiv.org/pdf/1611.04717v1.pdf)
  - Haoran Tang, Rein Houthooft, Davis Foote, Adam Stooke, Xi Chen, Yan Duan, John Schulman, Filip De Turck, Pieter Abbeel
  
### Options Discovery with Budgeted Reinforcement Learning [[review ICLR 2017]](https://arxiv.org/pdf/1611.06824v1.pdf)
  - Aurélia Léon, Ludovic Denoyer
  
### Stochastic Neural Networks for Hierarchical Reinforcement Learning [[review ICLR 2017]](http://openreview.net/pdf?id=B1oK8aoxe)
  - Carlos Florensa, Yan Duan, Pieter Abbeel
  - Uses a stochastic neural network to learn skills before task is presented(pre-training)
  - Trains skills by maximizing channel capacity
  - This algorithm solves continuous control tasks that were previously unsolved

### Unifying Count-Based Exploration and Intrinsic Motivation [[NIPS 2016]](https://arxiv.org/pdf/1606.01868v2.pdf)
  - Marc G. Bellemare, Sriram Srinivasan, Georg Ostrovski, Tom Schaul, David Saxton, Remi Munos
  
### Learning Purposeful Behaviour in the Absence of Rewards [[ICML 2016]](https://arxiv.org/pdf/1605.07700v1.pdf)
  - Marlos C. Machado, Michael Bowling
  
### Strategic Attentive Writer for Learning Macro-Actions [[NIPS 2016]](https://arxiv.org/pdf/1606.04695v1.pdf)
  - Alexander (Sasha) Vezhnevets, Volodymyr Mnih, John Agapiou, Simon Osindero, Alex Graves, Oriol Vinyals, Koray Kavukcuoglu
  - Develops an algorithm that learns to plan sequences of actions in addition to their level of commitment
  - Only works for finite action spaces and a predetermined timeline

### The Option-Critic Architecture [[arxiv 2016]](https://arxiv.org/pdf/1609.05140v1.pdf)
  - Pierre-Luc Bacon, Jean Harb, Doina Precup
  
### Hierarchical Deep Reinforcement Learning: Integrating Temporal Abstraction and Intrinsic Motivation [[NIPS 2016]](https://arxiv.org/pdf/1604.06057v2.pdf)
  - Tejas D. Kulkarni, Karthik R. Narasimhan, Ardavan Saeedi, Joshua B. Tenenbaum
  
### Variational Information Maximisation for Intrinsically Motivated Reinforcement Learning [[NIPS 2015]](https://arxiv.org/pdf/1509.08731v1.pdf)
  - Shakir Mohamed, Danilo Jimenez Rezende
  - Derives a variational inference algorithm for maximizing mutual information
  - This is the first tractable algorithm capable of computing empowerment
  
### Empowerment–an introduction [[Guided Self-Organization: Inception, 2014]](https://arxiv.org/pdf/1310.1863.pdf)
  - Christoph Salge, Cornelius Glackin, Daniel Polani
  - Gives evolutional justification for the concept of empowerment-having more control over the environment is desirable
  - Formally defines empowerment as the channel capacity between actions and future states

### Intrinsically Motivated Reinforcement Learning [[NIPS 2004]](http://web.eecs.umich.edu/~baveja/Papers/FinalNIPSIMRL.pdf)
  - Satinder Singh, Andrew Barto, Nuttapong Chentanez
  - Using the concept of intrinsic motivation, suggests that there is value in predefining options independently of the task
  - The agent creates options to achieve 'salient events', or events that are predetermined to be inherently interesting to the agent

### Recent Advances in Hierarchical Reinforcement Learning [[DEDS 2003]](http://www-anw.cs.umass.edu/pubs/2003/barto_m_DEDS03.pdf)
  - Andrew Barto, Sridhar Mahadevan
  - Summarizes three approaches to hierarchical RL: options, HAMs, MAXQ
  
### Learning Options in Reinforcement Learning [[ISARA 2002]](http://ftp.bstu.by/ai/To-dom/My_research/Papers-0/For-research/R-navigation/Grid-world/Good-one/stolle2002learning.pdf)
  - Martin Stolle, Doina Precup
  - Learns options by randomly specifying a task and making the most frequently visited state the termination condition of an option.
  
### Between MDPs and semi-MDPs: A Framework for Temporal Abstraction in Reinforcement Learning [[Artificial Intelligence Journal 1999]](http://www-anw.cs.umass.edu/~barto/courses/cs687/Sutton-Precup-Singh-AIJ99.pdf)
  - Richard Sutton, Doina Precup, Satinder Singh
  - Defines an option as a policy with a termination and initiation condition
  - Proves that using options instead of only the primitive actions on an MDP can be viewed as an SMDP problem
  - Proves that allowing interruption of options increases V-value
  - Introduces an option model learning algorithm
  - Defines V- and Q- values for options and proves convergence of option Q-learning
  - Gives example of gridworld where predefined options shortens learning
  
### Learning Macro-Actions in Reinforcement learning [[NIPS 1998]](https://papers.nips.cc/paper/1586-learning-macro-actions-in-reinforcement-learning.pdf)
  - Jette Randløv	
  - Lets previous action influence the choice of action
  - Defines modified Q-value which is a linear combination of Q(s_t, a_t) and Q(a_t-1, a_t)
