[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/Uzapeobl)
## Student Information

### Full Names: 
- David Alejandro Gutiérrez Leal
- Ginna Alejandra Valencia Macuacé
- Kadiha Muhamard Orta

### Class Number: 
7308

## Environment

Operating System: Windows 11

Programming Language: Python 3.10.2

Tools Used: PyCharm, Visual Studio Code

## Running Instructions

### 1. Ensure you have Python 3 installed.

### 2. Place the DFA description in a text file (e.g., DFA1.txt), following this format:

First line: Number of test cases

Each test case:

- Number of states

- Alphabet symbols separated by spaces

- Final states separated by spaces

- Transition table (each line contains: state, transition for symbol 1, transition for symbol 2)

### 3. Run the script using:

        python script.py

### 4. The output will display the DFA's equivalent state pairs.

## Algorithm Explanation

This implementation finds equivalent states in a Deterministic Finite Automaton (DFA) using partition refinement:

### Initialize partitions: 

- The states are divided into two groups: final states and non-final states.

### Iteratively refine partitions:

- Each state is assigned a signature based on its transitions and which partition those transitions lead to.

- States with the same transition signatures remain in the same partition.

- If a state transitions to different partitions compared to another state in the same partition, a new partition is created.

- This process continues until no more changes occur.

### Extract equivalent states:

- At the end of the partitioning process, states that remain in the same partition are considered equivalent.

- The algorithm outputs these pairs of equivalent states.
