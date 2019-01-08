# checkers_solver



On this project, we create a class checkers that followed all rules of American checkers. With this class, we tried to apply the principles of reinforcement learning to one of the players, in order to have some advantage against the opponent.

The checkers game is complicated due to many states or board configuration that can happen. Another difficulty is that it is played in turns, having each player 12 pieces. Normally, the examples you see of reinforcement learning are only one agent moving one piece in a limited space. Having this in mind, we had to be creative to find a solution.

The answer to this problem was not too complicated, but it delivers some advantages to one player while the other player moves randomly. 



## Getting Started



to run these notebooks on your computer you have to install anaconda or miniconda with python 3.7. after installation please follow the tutorials to create an environment and install the prerequisites.



## Prerequisites

numpy        1.15.4


pandas        0.23.4


matplotlib    3.0.1



## more information



We start playing randomly with both players. After each game, we use the final score to reward every previous state of that game. If the black player wins we score 1.0 with this all black's previous moves receiving a part of that reward. If the red win than the score is -1.0. The state closer to the end of the game gets the bigger the reward and those, in the beginning, the lower. 

The reason behind this try and error approach because we had to know the reward of every state. That is difficult to calculate, we could score the capture of the enemy pieces or the closer it gets to the enemy side. But that has no guarantee that the player is winning. 

After playing the game over 100000 times, saving the reward of every states and action that was found in this games, we created a huge policy with 1624138 states. If the states are found in this policy the blacks select those that give higher reward and plays it. 

In the end, black had a vantage of 60% over the red while the red plays randomly. The accuracy got better the more you play it in the training. 

For future work, we could play randomly while saving the reward and calculating the policy for the black and red players. this way they both improve the more they play. To ensure that they choose different moves to win a better reward, we could use the exploration and exploitation technic. 

Obs.: The policy file was over 150mb, so it could not be stored in the GitHub.