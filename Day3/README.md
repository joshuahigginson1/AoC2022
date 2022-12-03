# Advent of Code - Day 3

This challenge involves rearranging coded 'backpacks' according to a set of instructions.

Each rucksack has two large compartments. All items of a given type are meant to go into exactly one of the two compartments. The Elf that did the packing failed to follow this rule for exactly one item type per rucksack.

The puzzle input is a list of all of the items currently in each rucksack, but the elves need help finding the errors.

Every item type is identified by a single lowercase or uppercase letter.

Note that the characters *a* and *A* refer to different types of items.

The list of items for each rucksack is given as characters all on a single line.

A given rucksack always has the *same number* of items in each of its two compartments:

- The first half of the characters represent items in the first compartment.
- The second half of the characters represent items in the second compartment.

For example, suppose you have the following list of contents from six rucksacks:

```text
vJrwpWtwJgWrhcsFMMfFFhFp
jqHRNqRjqzjGDLGLrsFMfFZSrLrFZsSL
PmmdzqPrVvPwwTWBwg
wMqvLMZHhHMvwLHjbvcjnnSBnvTQFn
ttgJtRGJQctTZtZT
CrZsJsPPZsGzwwsLwLmpwMDw
```

The first rucksack contains the items "vJrwpWtwJgWrhcsFMMfFFhFp":

- The first compartment contains the items vJrwpWtwJgWr.
- The second compartment contains the items hcsFMMfFFhFp.
- The only item type that appears in both compartments is lowercase p.

The second rucksack's compartments contain jqHRNqRjqzjGDLGL and rsFMfFZSrLrFZsSL. The only item type that appears in both compartments is uppercase L.

The third rucksack's compartments contain PmmdzqPrV and vPwwTWBwg; the only common item type is uppercase P.

The fourth rucksack's compartments only share item type v.

## Rules

To help prioritize item rearrangement, every item type can be converted to a priority:

Lowercase item types a through z have priorities 1 through 26.
Uppercase item types A through Z have priorities 27 through 52.
In the above example, the priority of the item type that appears in both compartments of each rucksack is 16 (p), 38 (L), 42 (P), 22 (v), 20 (t), and 19 (s); the sum of these is 157.

## Part A

Find the item type that appears in both compartments of each rucksack. What is the sum of the priorities of those item types?

## Part B

Every elf carries one of three badges.

Within each group of three Elves, the badge is the only item type carried by all three Elves.

If a group's badge is item type B, then all three Elves will have item type B somewhere in their rucksack, and at most two of the Elves will be carrying any other item type.

All of the badges need to be pulled out of the rucksacks so the new authenticity stickers can be attached.

The only way to tell which item type is the right one is by finding the one item type that is common between all three Elves in each group.

Note: We have to find the one item type common between all three Elves in each group.

Every set of three lines in your list corresponds to a single group, but each group can have a different badge item type. So, in the above example, the first group's rucksacks are the first three lines:

```text
vJrwpWtwJgWrhcsFMMfFFhFp
jqHRNqRjqzjGDLGLrsFMfFZSrLrFZsSL
PmmdzqPrVvPwwTWBwg
```

In the first group, the only item type that appears in all three rucksacks is lowercase r; this must be their badges.

And the second group's rucksacks are the next three lines:

```text
wMqvLMZHhHMvwLHjbvcjnnSBnvTQFn
ttgJtRGJQctTZtZT
CrZsJsPPZsGzwwsLwLmpwMDw
```

In the second group, their badge item type must be Z.

Priorities for these items must still be found to organize the sticker attachment efforts: here, they are 18 (r) for the first group and 52 (Z) for the second group. The sum of these is 70.

Find the item type that corresponds to the badges of each three-Elf group.

What is the sum of the priorities of those item types?
