# Iterated Prisoner's Dilemma – Tournaments and Evolutionary Dynamics

Project for *Laboratory of Computational Physics* (M.Sc. Physics of Data, University of Padova). The
notebook simulates the iterated prisoner's dilemma between simple strategies, first in round-robin
tournaments and then in an evolving population.

**Payoffs:** R = 2 (both cooperate), S = 0 (sucker), T = 3 (temptation), P = 1 (both defect).

## Strategies

| Strategy | Behaviour |
|---|---|
| Nice | always cooperates |
| Bad | always defects |
| Mainly Nice / Mainly Bad | random strategies biased towards cooperation / defection |
| Tit-for-Tat | starts by cooperating, then copies the opponent's last move |
| Evolvable player | chooses its move from a gamma-distributed random variable |

Each player keeps its history of moves and rewards in bounded queues.

## Notebook sections

1. **Match:** repeated games between two strategies.
2. **MPIPD:** multi-player iterated prisoner's dilemma as a round-robin tournament.
3. **Iterative tournament (Moran process):** after each round-robin tournament, the most successful
   strategy replicates (with a probability given by its share of the payoff) and replaces a randomly
   chosen other player. This repeats until a single strategy has taken over the population.
4. **Mutations:** the Moran process extended with mutations between strategies, in two variants.

The final section heading, *Reinforcement Learning (with DQN)*, is a placeholder with no implementation.

Requirements: `numpy`, `pandas`, `matplotlib`, `seaborn`, `plotly`.
