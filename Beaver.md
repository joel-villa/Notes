# Beaver Tripples Overview

$$ 
\langle s \rangle
$$
- s is a secret 
- Example: secret is mod 7, then the secret sharing would be the sum of all
  integers mod 7
    - If all players get together than they learn the secret, but if any 
      coalition less than all of them gets together, they learn nothing
      
## Secrets and Computation

- If you have secret s, and secret t, you can do local addition, but not local
  multiplication
- Addition and multiplication is all that is needed to represent a circuit

## Can We Compute with Secrets

- Secure multi-party computation
- Goal: Everyone learns $f(s_1, s_2, \dots, s_n)$, but the function $f$ 
  remains secret
- n millionaires problem:
    - A bunch of players have a private net worth, and they want to learn who
      is the richest without revealing the private net worths
- APplications:
    - Federated Learning
    - Smart Contracts: Learn the winner of the auction and learn how much they
      have to pay
## Given secret s and secret t, we want s times t

- Beaver Triples: three seperate sharers, which have nothing to do with s or t
    - a, b, and c = a * b
    - How to get a, b and c is the poin tof the research project
- If we have $a, b, c$, then
- a is uniformly random in the field, revealing to everyone alpha, doesn't 
  reveal anything about s, same with beta
$$
\alpha \gets s - a
\beta \gets t - b
u_i \gets \beta s_i + \alpha b_i + c_i = st
$$

- In order to maintain privacy, need to generate new beaver tripples per 
  computation

## Shamir Secret Sharing

- Secret Sharing by a polynomial
- The shares are the values $s_i$, points on a polynomial, and the secret is 
  the y-intercept
- Note: make degree of polynomial one less than the number of players, so that
  all players need to get together in order to discover the function
    - All players getting together can still fingure out the secret if one is 
      lying
    - How? 

## Finding Beaver Triples

- Can never be rueused
- Can't be easily updated when group changes
- No Cryptographic assumptions
    - No computational bounds on the adversary
    - Information theoretically secure technique
- Goal: Scalable
- Assumption:
    - private channel between every pair of players
    - Many ways to do this: 
        - EX: quantum channel in which you can see if someone read the message

## Discrete Fourier Transform

- Typical: coefficient space to frequency space:
    - Can represent any polynomial as the sum of sines and cosines
- Methodology: go from coefficient space to point-space:
    - Outputs of the function at these roots of unity
- FFT gives a fast way to get Shamir sharers from additive sharers
- This graph: butterfly network: 
    - number of levels is logn
    - every node has degree which is just a constant
## Naive

- Let all players participate in this node here, set these coefficicients to 
  
## Idea: Harden Nodes by Grouping

- Weight the nodes

## Critical Last Step

- We have the abstract concept of weights, we want to do the mapping between 
  the weights and the players at the nodes
- You have weights of these nodes, you assume communication can be done in such
  a way that the channel is private, and adversary doesn't learn the player 
  unless they pay the weight to that node
- GOAL: if you assign players to nodes according to weighting scheme, and you 
  assign communication pattern, it will have the property that the adversary
  doesn't learn the value at a node unless it takes over a number of players 
  that is equal to the weight of that node
- PRIVACY: how to protect against coallitions of 'malicious' players

LOOKUP: information secure multi party computation, 
- Lecture Notes
- 

- Abi's direction:
    - For a single butterfly, to learn
    - 2 key lemmas:
        1. (inductive) for an adversary to learn values at some set of nodes
          s, which has total weight $w(s)$, then the adversary needs to take 
          over a number of players which is close to $w(s)$
        2. Helper Lemma: individual butterfly
            - NOTE: communication goes from butterfly to butterfly
            - If the adversary controls a number of players in the butterfly 
              that is less than the weight of that butterfly, than it learns
              nothing new about the butterfly
              
              
   
