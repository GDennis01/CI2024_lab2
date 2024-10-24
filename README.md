## Lab 2 of the Computational Intelligence Course at PoliTO
![Lab 2 specification](image.png)
*All rights of the image goes to Giovanni Squillero*

## Choices rationale
- **Flow:** The way the algorithm works is the following: it starts by generating a greedy solution.
From that solution new solutions are created randomly that will serve as the base population. The algorithm then proceeds to evolve the population by applying the mutation operator to each individual. 
The best solution is kept and, if it's not already present, it's added to the population with a certain probability. The algorithm stops when the maximum number of steps is reached.
Unlike we've seen in class, half the population is mutated at each step, not just a single individual. This has been proven to yield better results in this case.
- **Mutation:** The best mutation method found is the simple Inversion Mutation operator. Although very simple, it proved to be the best among the other methods I've tried.
- **Crossover:** Through trial and error I found out that crossover brought no benefit to the algorithm, so I decided to go for a mutation-only approach.
- **Valhalla:** The best solution has a chance to respawn in the population but only if it's not already present. In this way, we avoid an early takeover.  Although it's not really beneficial at all,
I decided to keep it because I find it an interesing concept and I like norse mythology.


## Performance
- **china.csv:** 59779.14909155967 with 10000 steps
- **italy.csv:** 4181.6197997589 with 10000 steps
- **russia.csv:** 34999.927023061864 with 10000 steps
- **us.csv:** 0,00028599503454937935058 with 10000 steps
- **vanuatu.csv:** 1345.5449564733112 with 20 steps

## Contributors
Some techniques implemented in my proposal were discussed and developed jointly with my [colleague]( https://github.com/FerraiuoloP/).
We started from the same template, then we devised together a way to implement a crossover/mutation. We concluded together that the Inversion Mutation operator (explained at this link) was the best choice for our scenario