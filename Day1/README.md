# Advent of Code - Day 1


Collect stars by solving puzzles. Two puzzles will be made available on each day in the Advent calendar; the second puzzle is unlocked when you complete the first. Each puzzle grants one star. Good luck!

## Part A

We are given a list of calories like so:

```bash
1000
2000
3000
        # The first Elf is carrying food with 1000, 2000, and 3000 Calories, a total of 6000 Calories.
4000
        # The second Elf is carrying one food item with 4000 Calories.
5000
6000
        # The third Elf is carrying food with 5000 and 6000 Calories, a total of 11000 Calories.
7000
8000
9000
        # The fourth Elf is carrying food with 7000, 8000, and 9000 Calories, a total of 24000 Calories.
10000
        # The fifth Elf is carrying one food item with 10000 Calories.
```
This represents the food carried by five Elves. Each line is a food item. Everything surrounded in a blank line is a new elf's inventory.

Find the Elf carrying the most Calories. How many total Calories is that Elf carrying?

Answer = 69693

## Part B

Find the top three Elves carrying the most Calories. How many Calories are those Elves carrying in total?

# Solution.

First, I want to read the text file into a Pandas dataframe for speedy processing.
I can then perform row operations on the dataframe to easily sort and aggregate values, for BOTH parts.