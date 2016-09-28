## Imitation Learning


### Model-Free Imitation Learning with Policy Optimization[[ICML 2016]](https://arxiv.org/pdf/1605.08478)
  - Jonathan Ho, Jayesh K. Gupta, Stefano Ermon
  - Given a class of reward functions, find the policy that maximizes the minimum advantage against expert policy over the whole class
  - Suggests two algorithms, IM-REINFORCE and IM-TRPO, both of which iteratively find better and better policies
  
### Guided Policy Search [[ICML 2013]](https://graphics.stanford.edu/projects/gpspaper/gps_full.pdf)
  - Sergey Levine, Vladlen Koltun
  - Videos available [here](https://graphics.stanford.edu/projects/gpspaper/index.htm)
  - Derives a scheme that, given a trajectory, constructs a policy that produces trajectories close to it(using iterative LQR and adding theoretically justified noise)
  - Descibes the Guided Policy Search algorithm, which is designed to explore around the given trajectories and find a good policy

### Algorithms for Inverse Reinforcement Learning [[ICML 2000]](http://citeseerx.ist.psu.edu/viewdoc/download;jsessionid=4C4D16E1D96E10A07A1EFFD5D64C7C68?doi=10.1.1.41.7513&rep=rep1&type=pdf)
  - Andrewy Y. Ng, Stuart Russell
  - Reduces IRL(Inverse Reinforcement Learning) to a LP(linear programming) problem, and introduces a penalty term to choose a reward function within the class obtained from LP
  - Experiments show promising results on simple enviornments
