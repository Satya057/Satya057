 
 State Diagram:
 
3x3 TicTacToe
Our idea revolves around directing the AI agent (in this case the computer) to choose a move based on the utilities of the immediate next moves available to it. The agent must pick the maximum of these utilities for the next move.

 
Analysis of each Complexity Level
As mentioned above in each of the complexity levels, a custom version of the minimax algorithm is run, with two varying factors depth and utility function .
Depth (Difficulty Level): If the complexity level is X , the agent can explore nodes (or board configurations) that are up to a X hop distance from the current state of the board.
For example : With complexity level = 2 , the agent can explore nodes (or board configurations) that are up to a 2 hop distance - that is 2 levels deep - from the current state of the board.
Utility Functions
a) Complexity Level1
At complexity level 1, the agent is extremely naive . Since the agent can choose only amongst the nodes that are at a one hop distance in the recursive tree, we assign the same utility to all the possible board configurations from current configuration and a random function that arbitrarily selects one of the empty cells for the agent to make its next move.

b) Complexity Level2
At level 2, the agent’s smartness is increased and a new function is used to compute the utilities of the next states. The agent can now look at upto 2 levels deep from the current state. The function we have considered here is the number of crossover win states that a particular empty cell can contribute to
c) Complexity Level3
At level 3, there is an extension to the strategies of level 2. As expected, the agent can now explore upto 3 depths from its current configuration. Apart from the crossover win states, we now allow the agent to look for only agent’s win configurations and boost the utilities for those states so that the agent favours them more.
d) Complexity Level4
At level 4, the agent now can look upto 4 depths, adopts all the strategies of level 2 and 3, and additionally now also tries to block the human player from winning. So it now also looks at moves that can cause the human to lose, thereby further increasing the ability of the agent to think.

![WhatsApp Image 2022-09-07 at 10 03 06 PM](https://user-images.githubusercontent.com/107452937/188939730-49979984-b2e0-4df8-885a-b9d4c8ef09c6.jpeg)
