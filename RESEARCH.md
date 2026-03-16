# 1. Representation

For this problem, we can define the representation as real numbers. In an array, we can define the colour a given country will be assigned by the number, which will directly map to a dictionary with labels. Also, the position of the number in array will relate to the country, and each position will be correspond to the country in that position in sorted list. 

# 2. Fitness Function

The fitness function can be define as the number of countris sharing borders that have the same colors. The goal will be to reach 0 as the value, which will represent that all countries have a different colour from their neighbours. 

# 3. Algorithms

For a genetic algorithm, there are several differents sub-algorithms that can be implemented along the steps: recombination, mutation, parent selection and survivor selection. For this assignment, it will be tested two different sub-algorithms for each one of them, and different tests will be ran combining those different options to reach the optimal solution. 

# 3.1. Cross-over 

source: 
- https://www.geeksforgeeks.org/machine-learning/crossover-in-genetic-algorithm/

a. Two-Point Crossover

In this technique, two different points of the parents chromossomes are chosen, and swapped between them.

b. Uniform Crossover

Each gene of the chromosse of the children is chosen randomly, with equal odds, from the corresponding position of their parents.


# 3.2. Mutation

source: https://www.geeksforgeeks.org/dsa/genetic-algorithms/

a. Inversion mutation

Selects a strip of the representation string at random, and then reverses the order of the genes

b. Swap mutation

Selects two random genes in the chromossome and swaps their position

# 3.3. Parent Selection

https://www.geeksforgeeks.org/dsa/genetic-algorithms/

a. Roulette Wheel Selection (RWS)

Selects parents based on a weighted random selection, in which the odds of being chosen is proportional to its fitness value. In the assignment context, since the fitness function aims to decrease the value to 0, the odds of being chosen wil be inversely proportional to the fitness function value

$P_i = \frac{f_i}{\sum_{j=1}^{N} f_j}$

$f'_i = \frac{1}{f_i + 1}$

$P_i = \frac{f'_i}{\sum_{j=1}^{N} f'_j}$

b. Tournament Selection
https://www.baeldung.com/cs/ga-tournament-selection
A random sample of individuals are chosen from the population, and the fittest among them are selected as parents


# 3.4. Survivor Selection 

source: https://www.tutorialspoint.com/genetic_algorithms/genetic_algorithms_survivor_selection.htm

a. Elitism

New generations individuals are mixed with the previous generation, and the fittest amongst them are propagated

b. Age-based selection
https://www.tutorialspoint.com/genetic_algorithms/genetic_algorithms_quick_guide.htm

For each iteration of the algorithm, an individual age increases by one. In this sub-algorithm, the k oldest individuals are replaced, independent of their fitness function.
