# Advent of Code - Day 5

This challenge involves a map of 'crates', and a given set of moves.

The elves want to know which crate will end up where after the set of moves, and they want to be ready to unload them as soon as possible so they can embark.

The input file looks like so:

```text

    [D]    
[N] [C]    
[Z] [M] [P]
 1   2   3 

move 1 from 2 to 1
move 3 from 1 to 3
move 2 from 2 to 1
move 1 from 1 to 2
```

In this example, there are three stacks of crates. Stack 1 contains two crates: crate Z is on the bottom, and crate N is on top. Stack 2 contains three crates; from bottom to top, they are crates M, C, and D. Finally, stack 3 contains a single crate, P.

Then, the rearrangement procedure is given. In each step of the procedure, a quantity of crates is moved from one stack to a different stack. In the first step of the above rearrangement procedure, one crate is moved from stack 2 to stack 1, resulting in this configuration:

``` text
[D]        
[N] [C]    
[Z] [M] [P]
 1   2   3 
```

In the second step, three crates are moved from stack 1 to stack 3. Crates are moved one at a time, so the first crate to be moved (D) ends up below the second and third crates:

```text
        [Z]
        [N]
    [C] [D]
    [M] [P]
 1   2   3
 ```

Then, both crates are moved from stack 2 to stack 1. Again, because crates are moved one at a time, crate C ends up below crate M:

```text
        [Z]
        [N]
[M]     [D]
[C]     [P]
 1   2   3
```

Finally, one crate is moved from stack 1 to stack 2:

```text
        [Z]
        [N]
        [D]
[C] [M] [P]
 1   2   3
```
# Part 1

The Elves just need to know which crate will end up on top of each stack; in this example, the top crates are C in stack 1, M in stack 2, and Z in stack 3, so you should combine these together and give the Elves the message CMZ.

Noting that each box is moved one at a time,

After the rearrangement procedure completes, what crate ends up on top of each stack?


# Part 2

The CrateMover 9001 has the ability to pick up and move multiple crates at once, rather than one at a time.

After the rearrangement procedure completes, what crate ends up on top of each stack?