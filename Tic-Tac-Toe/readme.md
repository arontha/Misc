# Tic-Tac-Toe AI Training
#### By Aron Tharp

### Abstract:
A very simple exploration in training an AI based on many simulations, starting with a purely random AI and improving iteratively.

### Summary:
As a proof of concept, I developed an AI to play the classic game of tic-tac-toe. To train the AI, I begin with a purely random AI (choose where to play an x or o randomly). I then make the random AIs play against each other millions of times and record the outcomes to develop a smarter AI. Then, a final iteration of training takes place where the smarter AI plays against itself 150,000 times, and then also plays against the random AI millions of times each first as x and then as o. These three AIs can then be played against by an individual as easy, medium, or hard difficulty, respectively.

### Contents:
**1. Tic-Tac-Toe.ipynb**
- Play the game as a player against the 3 AIs
- Requires the x_wins, o_wins, and ties directories with their contents

**2. Tic-Tac-Toe_Trainer_First_Iteration.ipynb**
- Make the random AI play against itself millions of times
- Generates the first set of data for the ‘smarter’ AI aka medium difficulty

**3. Tic-Tac-Toe_Trainer_Second_Iteration.ipynb**
- Make the smarter AI play against itself and the random AI hundreds of thousands of times
- Generates the second set of data for the even smarter AI aka hard difficulty

**4. x_wins, o_wins, and ties directories**
- each directory contains the results of the 2 trainings saved as x_wins, o_wins, and ties .txt files

### Failures and Successes:
1. Initiatially, the random AI was truly 'random', meaning even if a move was available to immediately win the game, the AI would not take it. Despite this naiveté, the AI still performed decently, about as well as a school child, but it could not compete with a smart human adult tic-tac-toe player and would still lose. As a result, the ranadom AI needed a slight logic boost, and the random play now also evaluates if any immediately moves win the game, and takes the winning move instead of the random move if available. 
2. An Smart AI must play against different styles, otherwise its training data is overfitted. Initially, I just had the smarter AI only play against itself, but that did not generate a smarter AI. By making it also play against the 'dumber' AI, it now had the training data to perform adequately vs. a human.

### "Smart" AI
The way the Smart AI uses the data is as follows:
1. If an immediate move wins, take it.
2. If an immediate move ties, take it.

