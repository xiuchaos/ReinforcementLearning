
# Introduction 

## 1.1 Reinforcement Learning

a learning system that *wants* something, that *adapts* its behavior in order to maximize a special signal from its environment: learn what to do - how to map situations to ations - so as to maximize a numerical reward signal.

* supervised learning - learn a map f(x): X->Y
> supervised learning is learning from a training set of labeled examples provided by a knowledgable external supervisor. However, In uncharted territory - where one would expect learning to be most beneficial- an agent must be able to learn from its own experience.

* unsupervised learning - find some hidden patterns or structures of the data

* reinforcement learning - learn how to take actions in order to maximize reward.


**Most distinguished features**
1. goal-directed learning from interactions 
2. trial and error search
3. delayed reward 

A learning agent must be able to sense the state of its envioronment to some extent and must be able to take actions that affect the state. The agen also must have a goal or **goals relating to the state of the environment**.

**trade-off between exploration and exploration**

To obtain a lot of reward, a reinforcement learning agent must prefer actions that it has tried in the past and found to be effective in producing reward. The agent has to *exploit* that what it has already experienced in order to obtain reward, but it also has to *explore* in order to make better action selections in the future.

All reinforcement learning agents have explicit goals (goal seeking), can sense apspects of their environments(interactive), and choose actions to influence their enviorment (complete). 


## 1.2 Examples

**Phil prepares his breakfast** reveals a complex web of conditional behavior and interlocking goal-subgoal relationships.
* complex,tuned, interactive sequences of behavior are required 
* each step involves a series of eye movements to obtain information and guild reaching
* rapid judgement are continually made about how to carry the objects

All these examples involve goals taht are explicit in the sence that the agent can judge progress toward its goal *based on what it can sense directly*.

In all of these examples the agent can use its experience to improve its performance over time. The knowledege the agent brings to the task at the start - either from previous experience with related tasks or built into by design or evolution - influences what is useful or easy to learn, but interation with the environment is essential for adjusting behavior to exploit specific features of the task.


## 1.3 Elements of Reinforcement Learning

**main elements of a RL system** 
* a policy  - defines the learning agent's way of behaving at a given time

	* a policy is a mapping from perceived stats of the environment to actions to be taken when in those states. It correpponds to *stimulus-response* rules/associations in psychology. the policy is the core of a RL agent in the sense that it alone is sufficient to determine behavior. In general,policies may be stochastic.

* a reward signal - defines the goal in a reinforcement learning problem.
	
	* analogous to the experience of pleasure or pain in biological system. The reward signal is the primary basis for altering the policy. if an action selected by the policy is followed by low reward, then the policy may be changed to select some other action in that situation in the future. In general, reward signals may be stochastic functions of the state of the environment and the actions taken.

* a value function - long run reward

	* reward signal indicates what is good in an immediate sense, value function specifies what is good in the long run. values indicate the long-term desirability of states after taking into account the states that are likely to follow, and the rewards available in those states. Make a human analogy, values corresponds to a more refined and farsighted judgement of how pleased/displeased we are that our environment is in a particular state.

	* rewards a given directly from the environment, but values must be estimated and re-estimated from the sequences of observations an agent makes over its entire life. The central role of value estimation is argubly the most important thing we can learned about reinforcement learning.

* a model of the enviorment (optionally)

	* allows inference to be made about how the environment will behave. the model might predict the resultant next state and next reward.
	* model-based/model-free, planning/trial-and-error
	* moden reinforcement learning spans the spectrum from low-level, trial-and-error learning to high-level, deliberative planning.


## 1.4 Limitations and Scope

**state** a heavily relied concep in RL -- as input to the policy and value function.

* formal definition of stateis given by the framework of Markov decision processing
* more generallly, the informal meaning: think of the state as whatever information is available to the agent about its enviroment.


**evolutionary methods** - without estimating value functions
> evolutionary methods have advantage on problems in which the learning agent cannot sense the complete state of its environment.


## 1.5 An Extentded Example: Tic-Tac-Toe

Tic-Tac-Toe
* classical minimax solution
* optimization methods for sequential decision problems, such as dynamic programming
* evolutionary method
* approached with a method making use of a value function 
	* estimate the state's value
	* most of time we *move greedily* selecting the move that leads to the state with greatest value, that is, with the highest estimated probability of winning
	* occasionally, we randomly moves *exploratory moves*, because they cause us to experience states that we might otherwise never see.


## 1.6 Summary

reinforcement learning is the first field to seriously address the computational issues that arise when learning from interaction with an environment in order to achieve long-term goals.

Reinforcement learning uses the formal framework of *Markov decision processes* to define the inter-action between a learning agent and its environment in terms of states, actions, and rewards. This framework is intended to be a simple way of representing essential features of the artificial intelligence problem.

These features include a sense of *cause and effect*, a sense of *uncertainty and nondeterminism*, and the *existence of explicit goals*. Value and value functions are the key features of most of the reinforcement learning methods in this book.


## 1.7 Early History of Reinforcement Learning
