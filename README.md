# moea-automatic-termination
Implementation of the MOEA Entropy based automatic termination algorithm (Saxena et al. 2016)

# Description
This code provides an implementation of the Entropy-Based Termination Criterion for Multiobjective Evolutionary Algorithms described in the publication:

- Saxena, D. K., Sinha, A., Duro, J. A. & Zhang, Q. Entropy-Based Termination Criterion for Multiobjective Evolutionary Algorithms. IEEE Trans. Evol. Comput. 20, 485–498 (2016). - http://ieeexplore.ieee.org/xpl/articleDetails.jsp?reload=true&arnumber=7273886
 
 *Abstract:*
 Multiobjective evolutionary algorithms evolve a population of solutions through successive generations toward the Pareto-optimal front (POF). One of the most critical questions faced by the researchers and practitioners in this domain relates to the number of generations that may be sufficient for an algorithm to offer a good approximation of the POF for a given problem. Ironically, to date, this question largely remains unanswered and the number of generations are arbitrarily fixed a priori, with potentially punitive implications. If the a priori fixed generations are insufficient, then the algorithm reports suboptimal solutions. In contrast, if the a priori fixed generations are far too many, it implies waste of computational resources. This paper proposes a novel entropy-based dissimilarity measure that helps identify on the fly the number of generations beyond which an algorithm stabilizes, implying that either a good approximation has been obtained or that it cannot be obtained due to the stagnation of the algorithm in the search space. Given that in either case no further improvement in the approximation can be obtained, despite additional computational expense, the proposed dissimilarity measure provides a termination criterion and facilitates a termination detection algorithm. The generality, on-the-fly implementation, low-computational complexity, and the demonstrated efficacy of the proposed termination detection algorithm, on a wide range of multiobjective and many-objective test problems, define the novel contribution of this paper.
Published in: IEEE Transactions on Evolutionary Computation ( Volume: 20, Issue: 4, Aug. 2016 )
# What's in here?

The algorithm is implemented through the update() method of the MOEATerminationDetection class. It's initialized with the n_s (generations to consider), n_p (decimal places to consider) and n_b (number of bins to use to partition the solution space during dissimilarity calculation) parameters, and DEBUG prints the mean and standard deviation of the dissimilarity measure at each generation.

Running python automoea.py will run a basic example set in __main__ at the bottom of the file. There is also a modified example of the knapsack problem moea example borrowed from the DEAP project (https://github.com/DEAP/deap). algorithm.py is modified to use the MOEATerminationDetection. To run this example, please install DEAP (pip install deap --user) and run it with python knapsack.py. DEAP is described in these publications:

- François-Michel De Rainville, Félix-Antoine Fortin, Marc-André Gardner, Marc Parizeau and Christian Gagné, "DEAP -- Enabling Nimbler Evolutions", SIGEVOlution, vol. 6, no 2, pp. 17-26, February 2014. Paper

- Félix-Antoine Fortin, François-Michel De Rainville, Marc-André Gardner, Marc Parizeau and Christian Gagné, "DEAP: Evolutionary Algorithms Made Easy", Journal of Machine Learning Research, vol. 13, pp. 2171-2175, jul 2012. Paper

- François-Michel De Rainville, Félix-Antoine Fortin, Marc-André Gardner, Marc Parizeau and Christian Gagné, "DEAP: A Python Framework for Evolutionary Algorithms", in !EvoSoft Workshop, Companion proc. of the Genetic and Evolutionary Computation Conference (GECCO 2012), July 07-11 2012. Paper

# Miscellaneous

As an additional example, a project using the MOEA Automatic Termination algorithm and DEAP is MotifGP; a motif discovery engine for mining network expressions in DNA sequences.

See motifgp/termination in the development branch (git checkout development) of https://github.com/mbelmadani/motifgp

# Support and contributions

Feel free to contact Manuel Belmadani \<mbelm006@uottawa.ca\> for questions or comments. Pull requests are welcome! There's also the issues section (https://github.com/mbelmadani/moea-automatic-termination/issues) where you can file bugs or request enhancements.
