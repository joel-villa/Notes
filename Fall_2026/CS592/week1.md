# Quantum computing for quantum chemistry and materials science

by Susan Atlas, University of New Mexico

## Questions

1. Could you go into more detail about a QPUs capabilities?
2. Are these superpositions handled via probability method?
3. What does she mean by better science enabled by quantum computing?
4. How to debug in quantum mechanics?

## Quantum Computing in 2026

- Quantum computing until about 3 years ago, quantum computing was completely 
  theoretical, for hypothetical quantum computers
- Companies are deploying working quantum computers
- Some Architechtures:
    - How to make a quantum bit?
    - trapped ions
    - nuetral atoms
    - superconducting transmons
- Today's landscape: similar to early supercomputing
    - Co-design: 
    - Full stack: quantum compilers, quantum languages (Qiskit - python based), 
      "QPUs"
    - Transition from 'NISQ' or 'Noisy' to 'fault-tolerant':
        - Mitigate noise (from environment and physics): using logical quibits
    - AI: use GPUs for quantum circuit tuning, calibration, and algorithm 
      optimization
    - Democratization of Quantum Computing: establish a center with quantum 
      computing architectures available for researchers

## What is a quantum computer?

- Quantum bits (qubits)
- Qubits exist in oone of two quantum mechanical (QM) states: |0> and |1>
- These are realized by the two quantum mechanical states of the atom:
    - The 
- A qubit can also exist in a linear superposition of states: 
    - Think of it like a point on a sphere, with two poles
- Can have the 'input' of an initial quantum state, and an output known as 
  'quantum measurement'
- REsults are probabilistic due to probabilstic nature of quantum mechanics
- Algorithms are implemented, and multiple runs, to give some statistical 
  analysis of an 'answer'

## Quantum Advantage:

- Can we do something useful with these systems?
- Computational state space is much broader than a classical supercomputer:
    - Can have linear combination of zero and one states -> more capabilities 
      of representing complex input
- Entanglement: enables new modes of representation:
    - 'Better science'
    - Example: a state that cannot be factorized into seperate quantum states

## A 'Killer APP' For Quantum Computing?

- Is there an application of quantum computers taht would justify all the funds
- EX: make back the cost of the supercomputer in one night by using it to find 
  an oil field

## Why is the Rational Design of Molecules and Materials 'hard'?

- Rational Design: on a computer
- Answer: Electron Correlation Problem:
    - Ex: is there a unified theory explaining alll correlated electron systems
    - The time indpendent schrodinger equation, couples all electrons in a 
      system concurrently, through all possible binary Coulombic interactions
    - How to understand the relation between all electrons in a system
    - The wave function is a function of all electronic coordinates in the 
      sytem (cannot be measured)
- Everything that exists, exists due to subtle interractions of the electrons
- Misconceptions:
    - Can do local approximations (long distance relations play a role)

## Atomic Building Blocks Have Quantum mechanical Substructure

- Wave function tells you how everything behaves, the experimantal observable 
  that corresponds to it is electron density
- No such things as purely inioc bonds or purely covelnt bonds:
    - Bonds can become more or less ionic, but at the end of the day, the 
      question is how to calculate the wave function to the closeset accuracy
      
## The Electronic Structure Problem

- Goal: solve a time independent Schroginger equation

## "Quantum Chemistry" Approach to Electronic Structure Problem

- Variational method: guess and check parameters to solve Schrodinger equation
- Problems: 
    - exponential scaling with system size (number of electrons)
    - slow convergence as number of terms grow
    - Not applicable to periodic systems (can't do materials)

## The Electron Density and Statistical Interpretation of Quatnum mechanics

- Recall: electron density has only one degree of freedom
- The electron density is a probability distribution derrived from the wave 
  function
- Methodology: replace wave function with electron density:
    - Works in materials, but can be useable also on molecules
- Any calculation of a physical property that you could do with the wave 
  function you can now do with the electron density
- Correlation energy functional, has had many approximations made for it that
  does extremely well. So how can we do things with density theory w/ quantum 
  computer to advance the field?
- Driver for her research: construct a modified correlation functional, that 
  packages: the idea being that b/c the quantum computer intrinsically involves
  entangled quibits, it will enable the ability to map real-world phenomena on 
  the quantum computer
  
## Quantum Advantage

- Take advantage of a formal mapping from teh Hartree Fock equations of 
  quantum chemistry (no correlation) + Kohn-Sham (density-based) 
    - Replace one model w/ another, to model complex combinationals

## Question: Can we do Quantum Computing for quantum chemistry

- Need more quibits, better quibits, better logical gates, 
- Mapping of the electron correlation problem into qubits

## Current Community

- Community moving in the direction of eelctron density theory
- Can we understand electron correlations betwen arbitrary atoms and electrons
