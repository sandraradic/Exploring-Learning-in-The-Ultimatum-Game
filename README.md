# COGS-303-Models-of-Learning
### This project incorporates Python and Netlogo to explore and model hypotheses to do with different learning styles in [The Ultimatum Game](https://www.sciencedirect.com/topics/neuroscience/ultimatum-game).

##### **Model 1: Difference Proportional Learning**
**Hypothesis:** People compare their own level of success to a potential role model and then copy their strategy with a probability proportional to the difference in success levels.

**Algorithm Implementation:** To model a player comparing their own success to a potential role model and copying the strategy from that player, players assess how well they themselves do and how well someone else did and compute the difference. The player then generates a random number and evaluates an inequality between the random number and the difference in payoffs proportion.
 
##### **Model 2: Motivation by Opposing Player’s Success**
**Hypothesis:** Maybe people don’t need to assess their own level of success. Copying behaviour
could be motivated entirely by the other person’s success.

**Algorithm Implementation:** To model being motivated by another’s success, the “learn” function of the netlogo code was altered to disregard one’s own strategy and always conform to the teacher’s (or other player’s). This hypothesis was implemented by setting the original player’s strategy to the teacher’s whenever the payoff was less than the teacher’s payout, indicating that the turtle was consistently copying their teacher’s strategy regardless of their own success rate (which wasn’t even considered).

#### **Model 3: Motivation by Dissatisfaction**
**Hypothesis:** Maybe people don’t need to know the other person’s level of success. Copying behaviour could be motivated by dissatisfaction.

**Algorithm Implementation:** To model being motivated by dissatisfaction with one’s own success, the model erased the training-data and changed the condition under which each player learned by keeping the payoff, which was each player’s own strategy. If a player’s payoff was less than their payout, then they decided to copy the strategy of another player. As a result, players would then want to change strategies more often when their payoff is low, and less often when their payoff is high, because players are more satisfied when they have a higher strategy. 

##### **Model 4: Deterministic Learning**
**Hypothesis:** Copying behaviour is entirely deterministic.

**Algorithm Implementation:** To model deterministic learning behaviour, the random number component in the “learn” function was removed so that a player’s copying behaviour would be entirely determined by the comparison of their payoff to the training-data (i.e. another random player’s payoff). If the training-data is greater than the player’s payoff, then the player adopts the other player’s strategy. If the training-data is less than or equivalent to a player’s payoff, the player keeps their original strategy. This removes any random component from copying behaviour, making it entirely conditional on the difference in payoffs.

