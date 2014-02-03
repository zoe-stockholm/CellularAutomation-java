 A cellular automaton is an array of cells that switch on or off depending on whether other cells are on or off. Even simple rules for deciding when cells turn on or off can lead to complex and beautiful patterns.

Let's consider a particular kind of automaton in which the array contains a single row of cells. At each timestep, all of the cells update their state depending on the states of their neighbours. The state of a particular cell at time T = 1 is determined by the states of the cell itself at T = 0, its left neighbour at T = 0, and its right neighbour at T = 0. Then the state of the cell at T = 2 is determined by the states of the cell and its two neighbours at T = 1, and so on.

The decision whether to turn on or off is governed by a rule. For example, a rule might say, "if the left neighbour is on, then turn on". You can think of a rule as a function with three binary inputs (the state of the left neighbour, the cell itself, and the right neighbour in the previous timestep) and one binary output (the new state of the cell in the next timestep).

A rule can be described by a single number from 0 to 255 in the following manner: convert the rule number into a binary number—base 2 instead of base 10—with 8 bits, which we'll call bit 7, bit 6, and so on down to bit 0, where bit 7 is the most significant bit and bit 0 is the least significant bit. If you take the three inputs as three bits of a binary number, you get a number k from 0 to 7, and bit k of the rule number gives you the output. 