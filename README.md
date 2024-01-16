# TravelingSalesman_Evo
This repo showcases how the TSP can be solved using genetic algorithm.

---
## Background:
The Traveling Salesman Problem (TSP) is a classic optimization problem in the field of computer science, operations research, and mathematics. The problem can be stated as follows: Given a list of cities and the distances between each pair of cities, the task is to find the shortest possible tour that visits each city exactly once and returns to the starting city.


![image](https://upload.wikimedia.org/wikipedia/commons/c/c4/TSP_Deutschland_3.png)


In more formal terms, let's say there are $n$ cities, and a distance matrix $D$ is given where $D[i][j]$ represents the distance between city $i$ and city $j$. The goal is to find a permutation of cities that minimizes the total distance traveled, and the salesperson must return to the original city.

The Traveling Salesman Problem is a well-known NP-hard problem, meaning that as the number of cities increases, the time required to find the optimal solution grows exponentially. There is no known polynomial-time algorithm that can solve the TSP for all cases, and the problem is widely believed to be inherently difficult in terms of computational complexity.

Due to its practical relevance in various fields such as logistics, transportation, and network design, researchers and practitioners have developed approximation algorithms and heuristics to find near-optimal solutions in a reasonable amount of time. Some common approaches include nearest neighbor algorithms, genetic algorithms, simulated annealing, and integer linear programming.

Despite its computational challenges, the Traveling Salesman Problem remains a fundamental problem in optimization and is used as a benchmark for testing the efficiency of algorithms in solving combinatorial optimization problems.

### Sidenote

In mathematics and computation, algorithms are categorized based on their difficulty, measured by the time or computational power needed to solve them. Problems are labeled as NP (Non-deterministic Polynomial) and are further classified into NP-easy, solvable in linear time (N × P increases linearly), and NP-hard, which require exponential time (N² × P or higher) as the number of elements increases, making their complexity grow exponentially.

## Formulation
The Traveling Salesman Problem (TSP) can be formally defined as an optimization problem using mathematical notation. Let's denote the problem as TSP.

### Given

- $n$ cities, represented by the set $C={1,2,...,n}$.
- A distance matrix $D$, where $D[i][j]$ is the distance between city $i$ and city $j$.

### Objective

Find a permutation $π$ of the cities in $C$ such that the total travel cost is minimized. The total travel cost is defined as the sum of distances along the tour:

$$ \text{Minimize}:\sum_{i=1}^{n−1}D[π(i)][π(i+1)]+D[π(n)][π(1)]$$

Here, $π(i)$ represents the $i$-th city in the permutation $π$. The summation goes from the first city to the $(n−1)$-th city, and the last term represents the distance from the $n$-th city back to the first city to complete the tour.

### Constraints

The solution must be a permutation of the cities, visiting each city exactly once:

$$\text{Subject to} :π(i) \neq π(j) \quad \text{for} \quad i \neq j, π(i) \in C  \quad \text{for} \quad  i=1,2,...,n$$

The Traveling Salesman Problem is known to be NP-hard, indicating that finding an optimal solution for large instances becomes computationally intractable in polynomial time. As a result, approximation algorithms and heuristics are often employed to find near-optimal solutions efficiently.

---
## The Problem

The left figure below illustrates a scenario of the traveling salesman problem (TSP) on a map grid measuring 100 units by 100 units. The depicted spots represent the 22 destinations, including the starting point, the salesman has to visit exactly once before returning home at the conclusion of the trip.

The right figure illustrates an initial randomized solution.

<img src="https://github.com/ABr-hub/TravelingSalesman_Evo/blob/ede9a9d6191f8ad23d430e045dff25b66dd65918/ressources/Initial_Problem.png"  width=44% height=44%/> <img src="https://github.com/ABr-hub/TravelingSalesman_Evo/blob/ede9a9d6191f8ad23d430e045dff25b66dd65918/ressources/Randomized_solution.png"  width=45% height=45%/>

---
## Sources 
[1] https://de.wikipedia.org/wiki/Problem_des_Handlungsreisenden
