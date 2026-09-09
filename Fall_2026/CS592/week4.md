# Harnessing Random Molecular Motion to Ratchet Up Information in Self-Assembled Structures

By Matthew Patitz, University of Arkansas

## Questions

1. What is redundancy in Information theory?

## THe Input Fully Specifies the Output

- Systems which input determines output is a 'hardcoded' system

## DNA Origami

- Example of 'hardcoded' system
- DNA Origami - making stapeles (little pieces of DNA) in such a way that they 
  will build specific structures
  
## DNA Bricks

- If we want to make a new shape, need new strands
- 'I'm looking for something more'

## Algorithmic Ratchets

### Turing Machine

- What state to go in, given some input?
- Two different paradigms which explain all computation
- If it can be computationally realized by a device, it can be done with a 
  turing machine
  
### Limits of Computation

- Uncomputable problems
- EX: Halting Problem
    - Does Program P when fed input i ever stop?
    - Unanswerable, uncomputable in general

### THe Abstract Tile Assembly Model (aTAM)

- Holiday Junction: two DNA strands added together = tile with four 'sticky' 
  ends.
    - The tile on its edges has glues, ATCG -> a, b, c, d
- The amount of free energy when one of these sticky ends binds to its 
  complement (strenght 1, and strength 2 glue)
- More sides => advantages
    - Want at least four sides, easiest to build was four, so that's probably
      why square
      
### Algoirthmic self-assembly in the aTAM

- Binding threshold = 2 -> tile can stick with strength one glue, or two
  strength one glues, then it will stick
    - A straightforward design
- Input sides (ones combined)
- Output sides (ones exposed after sticking)
- Tiles are designed s.t. they enforce binary arithmatic
    - Overflow = stop growth
    - Different seeds -> won't grow as far
    - Binary counter!

### The aTAM is Turing Universal

- As the turing would perform its execution, a new row gets added to the 
  model. 
- Iff the turing machine would halt, will the aTAM halt

### ALgorithmic self-assembly in the aTAM

- If we wanted to build a square out of tiles, how many strands would I need?
- Area of square = amount of tiles needed
- Can dramatically more efficiently make structures (like a square)
    - log(n)
- Can build some fractals, some shapes have been proven to not be 
  self-assemblable

### Consequences for self-assembling systems

- IF you looked at the pieces of the puzzle, you could figure out what it'll 
  make
- From staple strands can determine what the shape will be
- We can encode a turing machine, for which we do not know an answer
    - Butt up against the halting problems
- Can build systems that through their designs will build structures, without 
  knowing the structures in advance

## Controlling Randomness

### Growth Errors

- One kind of error: can flip two bits rather than one in our binary counter

### Proofreading via 2x2 block replacement

- Combine two tiles into four tiles, they will each represent one tile in the 
  original system
- They wouldn't start all bound
- This is redundancy in Information Theory
- Just force more errors to have to happen before a single error occurs
- Why not just 3x3 blocks?
    - If you had a system with four tile types, now we have 16 tile types
    - As we increase number of unique types of tiles -> more necessity for 
      unique dna sequences
    - Problem: these sequences are not exactly orthoganol
    - Also using more space and time

### Spurious Nucleation

- Guys that stick together that we don't want outside of our 'program'

### Crisscross slats: nucleation control and highly cooperative binding

- This binds with 16 input glues per slat
- Only once four are in place is there room for another four
- This is a fix for spuerious nucleation
- Throw enormous number of slats into nucleation and no spuerious nucleation 
  occurs without an input seed
- With 16 sticky ends per slat -> requires four mismatches in order to get 
  a wrong attachment -> errors unlikely to propogate
- 
