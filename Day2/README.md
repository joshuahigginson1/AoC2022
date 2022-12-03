# Advent of Code - Day 2

Rock Paper Scissors is a game between two players. Each game contains many rounds; in each round, the players each simultaneously choose one of Rock, Paper, or Scissors using a hand shape. Then, a winner for that round is selected: Rock defeats Scissors, Scissors defeats Paper, and Paper defeats Rock. If both players choose the same shape, the round instead ends in a draw.

## Part A

Input is an encrypted strategy guide for rock-paper-scissors.

First column is what your opponent is going to play:
A - Rock - 1 Point
B - Paper - 2 Points
C - Scissors - 3 Points

Second column is you should play in response:
X - Rock - 1 Point
Y - Paper - 2 Points
Z - Scissors - 3 Points

Winning every time would be suspicious, so the responses must have been carefully chosen.

Scores for outcomes of the round:

Lose - 0
Draw - 3
Win - 6

Playing a different shape has a different score associated with it.

Winner is the player with the highest score. 

Total score = sum of your scores for each round.

score for a single round = Score for the shape + the score for the outcome of the round.

Calculate the score you would get if you were to follow the strategy guide.

For example, suppose you were given the following strategy guide:

A Y
B X
C Z

This strategy guide predicts and recommends the following:

In the first round, your opponent will choose Rock (A), and you should choose Paper (Y). This ends in a win for you with a score of 8 (2 because you chose Paper + 6 because you won).

In the second round, your opponent will choose Paper (B), and you should choose Rock (X). This ends in a loss for you with a score of 1 (1 + 0).

The third round is a draw with both players choosing Scissors, giving you a score of 3 + 3 = 6.

In this example, if you were to follow the strategy guide, you would get a total score of 15 (8 + 1 + 6).

What would your total score be if everything goes exactly according to your strategy guide?

## Part B

Now, the second column says how the round needs to end:

- X means you need to lose.
- Y means you need to end the round in a draw.
- and Z means you need to win.

The total score is still calculated in the same way, but now you need to figure out what shape to choose so the round ends as indicated. The example above now goes like this:

In the first round, your opponent will choose Rock (A), and you need the round to end in a draw (Y), so you also choose Rock. This gives you a score of 1 + 3 = 4.
In the second round, your opponent will choose Paper (B), and you choose Rock so you lose (X) with a score of 1 + 0 = 1.
In the third round, you will defeat your opponent's Scissors with Rock for a score of 1 + 6 = 7.
Now that you're correctly decrypting the ultra top secret strategy guide, you would get a total score of 12.