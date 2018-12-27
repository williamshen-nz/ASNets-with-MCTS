# Action Schema Networks with Monte-Carlo Tree Search: The Best of Both Worlds

Research project for COMP3770 at the Australian National University. 

## Abstract

Planning is the essential ability of an intelligent agent to solve the problem of choosing which action to take in an environment to achieve a certain goal. Planning is an extremely important field within Artificial Intelligence that has countless real-world applications, including robotics and operations research.

Monte-Carlo Tree Search (MCTS) is a state-space search algorithm for optimal decision making that relies on performing Monte-Carlo simulations to incrementally build a search tree, and estimate the values of each state. MCTS can often achieve state-of-the-art performance when combined with domain-specific knowledge. However, without this knowledge, MCTS requires a large number of simulations in order to obtain reliable estimates in the search tree.

The Action Schema Network (ASNets) [Toyer et al., 2018](https://github.com/qxcv/asnets) is a very recent contribution  in planning that uses deep learning and neural networks to learn generalized policies for planning problems. ASNets are well suited to problems where the ``local knowledge of the environment can help to avoid certain traps''. However, like most machine learning algorithms, an ASNet may fail to generalize to problems that it was not trained on. For example, this could be due to a poor choice of hyperparameters that lead to an undertrained or overtrained network.

This research project is concerned with investigating how we can improve upon the policy learned by an ASNet by combining it with MCTS. Our project has three key contributions. The first contribution is an ingredient-based framework for MCTS that allows us to specify different flavors of MCTS -- including those which use the policy learned by an ASNet. Our second contribution is two new methods which allow us to use ASNets to perform simulations in MCTS, and hence directly affect the estimated values of states in the search tree. Our third and final contribution is two new methods for using ASNets in the selection phase of MCTS. This allows us to bias the navigation of the search space towards what an ASNet believes is promising.

Our empirical evaluation demonstrates that by combining MCTS with ASNets, we are able to `learn' what the network did not learn during training, improve suboptimal learning, and be robust to changes in the environment or the domain. We can more reliably and effectively solve planning problems when combining MCTS with ASNets, and hence we achieve the best of both worlds.
