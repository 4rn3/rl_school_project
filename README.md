# 1. Evironment
### 1.1 What is Space invaders

Space invaders is a classic shoot them up arcade game from 1978 developped by Tomohiro Nishikado. <br>
The goal is to defeat wave after wave of descending aliens with a horizontally moving laser to earn as many points as possible without getting hit by the aliens.<br>

![Screenshot](Space_Invaders.jpg)

# 2 Algorithms

### 2.1 Which algorithms to compare

For this project I'll be using the Deep Q Learning algorithm and the Actor-critic algorithm. <br>
The algorithms will be compared on: <ol> <li>Training time</li> <li>#Episodes</li> <li>Agent results</li> </ol>   

### 2.2 Deep Q learning (DQN)

Deep Q learning is a value based algorithm, <br>
A value based algorithm trains a value-function that outputs the value of a state or state-action pair. That value-function is then used by the policy (which is chosen in advanced) to take an action. <br>
Finding the optimal value-function will automatically result in finding the optimal policy.

Q-learning does this by initializing a Q-table (mappings of state-action pair & Q-value) chosing an action based on this table and updating it with the Bellman equation. <br>
When there are too many states/ actions or a continous state space  this approach doesn't work anymore because the Q-table becomes too large. <br>
This is where DQN comes into play: 
    Instead of getting the next action from the Q-table the model predicts the next action.
    Instead of updating the Q-table we fit our model.
    
### 2.3 Actor-critic
