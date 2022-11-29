# 1. Evironment
### 1.1 What is Space invaders

Space invaders is a classic shoot them up arcade game from 1978 developped by Tomohiro Nishikado. <br>
The goal is to defeat wave after wave of descending aliens with a horizontally moving laser to earn as many points as possible without getting hit by the aliens.<br>

![Screenshot](Space_Invaders.jpg)

# 2 Algorithms

### 2.1 Which algorithms to compare

For this project I'll be using the Deep Q Learning algorithm and the Actor-critic algorithm. <br>

I chose for these algorithms since I wanted to test the difference in performance between a value and policy based algortihm.<br>
Even though actor-critic is more of a hybrid architecture of value- and policy-based algorithms it seemed quite a bit faster than the other policy based algorithms i've tried so i'll let it slide.<br>

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
    
### 2.3 Actor-critic (AC)

In the previous section i briefly explained value based algorithms, now we'll take a look at policy based.<br>
In a policy based appoach we aim to optimize the policy directly without using a value function. <br>

The other policy based algorithm we covered was policy gradient, this worked well but took long to train and had high variance.<br>
Actor-Critic methods stabelize training by reducing the variance and where faster. <br>

In AC we have an actor that controls how the agent behaves, this is the policy-based part and a critic that measures how good the taken actions are, this is the value-based part.<br>