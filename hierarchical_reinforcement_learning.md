## Hierarchical Reinforcement Learning

  
###Towards Deep Symbolic Reinforcement Learning [[arxiv 2016]](https://arxiv.org/pdf/1609.05518v2.pdf)
  - Marta Garnelo, Kai Arulkumaran, Murray Shanahan
  - Suggests a pipeline(encoder, symbolic layer, RL layer) to get symbolic representations of envs with images as states
  
###Variational Information Maximisation for Intrinsically Motivated Reinforcement Learning [[NIPS 2015]](https://arxiv.org/pdf/1509.08731v1.pdf)
  - Shakir Mohamed, Danilo Jimenez Rezende
  
###Reward Mapping for Transfer in Long-Lived Agents [[NIPS 2013]](https://papers.nips.cc/paper/5191-reward-mapping-for-transfer-in-long-lived-agents.pdf)
  - Xiaoxiao Guo, Satinder Singh, Richard Lewis

###Intrinsically Motivated Reinforcement Learning [[NIPS 2004]](http://web.eecs.umich.edu/~baveja/Papers/FinalNIPSIMRL.pdf)
  - Satinder Singh, Andrew Barto, Nuttapong Chentanez
  - Using the concept of intrinsic motivation, suggests that there is value in predefining options independently of the task
  - The 'implementation' of intrinsic motivation is done through 'salient events', which are states that the agent tries to learn an option to achieve

###Recent Advances in Hierarchical Reinforcement Learning [[DEDS 2003]](http://www-anw.cs.umass.edu/pubs/2003/barto_m_DEDS03.pdf)
  - Andrew Barto, Sridhar Mahadevan
  
###Learning Options in Reinforcement Learning [[ISARA 2002]](http://ftp.bstu.by/ai/To-dom/My_research/Papers-0/For-research/R-navigation/Grid-world/Good-one/stolle2002learning.pdf)
  - Martin Stolle, Doina Precup
  - Learns options by randomly specifying a task and making the most frequently visited state the termination condition of an option.
  
###Between MDPs and semi-MDPs: A Framework for Temporal Abstraction in Reinforcement Learning [[Artificial Intelligence Journal 1999]](http://www-anw.cs.umass.edu/~barto/courses/cs687/Sutton-Precup-Singh-AIJ99.pdf)
  - Richard Sutton, Doina Precup, Satinder Singh
  - Defines an option as a policy with a termination and initiation condition
  - Proves that using options instead of only the primitive actions on an MDP can be viewed as an SMDP problem
  - Proves that allowing interruption of options increases V-value
  - Introduces an option model learning algorithm
  - Defines V- and Q- values for options and proves convergence of option Q-learning
  - Gives example of gridworld where predefined options shortens learning
  
###Learning Macro-Actions in Reinforcement learning [[NIPS 1998]](https://papers.nips.cc/paper/1586-learning-macro-actions-in-reinforcement-learning.pdf)
  - Jette Randløv	
  - Lets previous action influence the choice of action
  - Defines modified Q-value which is a linear combination of Q(s_t, a_t) and Q(a_t-1, a_t)
