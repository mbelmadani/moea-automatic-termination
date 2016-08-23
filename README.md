# moea-automatic-termination
Implementation of the MOEA Entropy based automatic termination algorithm (Saxena et al. 2016)

# Description
This code provides an implementation of the Entropy-Based Termination Criterion for Multiobjective Evolutionary Algorithms described in Saxena, D. K., Sinha, A., Duro, J. A. & Zhang, Q. Entropy-Based Termination Criterion for Multiobjective Evolutionary Algorithms. IEEE Trans. Evol. Comput. 20, 485–498 (2016). - http://ieeexplore.ieee.org/xpl/articleDetails.jsp?reload=true&arnumber=7273886

# What's in here?

The algorithm is implemented through the update() method of the MOEATerminationDetection class. It's initialized with the n_s (generations to consider), n_p (decimal places to consider) and n_b (number of bins to use to partition the solution space during dissimilarity calculation) parameters, and DEBUG prints the mean and standard deviation of the dissimilarity measure at each generation.

Running python automoea.py will run a basic example set in __main__ at the bottom of the file. There is also a modified example of the knapsack problem moea example borrowed from the DEAP project (https://github.com/DEAP/deap). The algorithm class is modified to use the MOEATerminationDetection. To run this example, please install DEAP (pip install deap --user) and run it with python knapsack.py. DEAP is described in these publications:

- François-Michel De Rainville, Félix-Antoine Fortin, Marc-André Gardner, Marc Parizeau and Christian Gagné, "DEAP -- Enabling Nimbler Evolutions", SIGEVOlution, vol. 6, no 2, pp. 17-26, February 2014. Paper

- Félix-Antoine Fortin, François-Michel De Rainville, Marc-André Gardner, Marc Parizeau and Christian Gagné, "DEAP: Evolutionary Algorithms Made Easy", Journal of Machine Learning Research, vol. 13, pp. 2171-2175, jul 2012. Paper

- François-Michel De Rainville, Félix-Antoine Fortin, Marc-André Gardner, Marc Parizeau and Christian Gagné, "DEAP: A Python Framework for Evolutionary Algorithms", in !EvoSoft Workshop, Companion proc. of the Genetic and Evolutionary Computation Conference (GECCO 2012), July 07-11 2012. Paper

# Miscellaneous

As an additional example, a project using the MOEA Automatic Termination algorithm and DEAP is MotifGP; a motif discovery algorithm for network expressions in DNA sequences.

See motifgp/termination in the development branch (git checkout development) of https://github.com/mbelmadani/motifgp

Publications 
- Manuel Belmadani and Marcel Turcotte. (In press) MotifGP: Using multi-objective evolutionary computing for mining network expressions in DNA sequences. In IEEE International Conference on Computational Intelligence in Bioinformatics and Computational Biology (CIBCB 2016), Chiang Mai, Thailand, October, 5-7, 2016. Preprint available upon request.
- Manuel Belmadani. MotifGP: DNA motif discovery using multiobjective evolution. Master of computer science, University of Ottawa, School of Electrical Engineering and Computer Science, 2016. Available from University of Ottawa Research under: http://www.ruor.uottawa.ca/handle/10393/34213


# Support and contributions

Feel free to contact Manuel Belmadani \<mbelm006@uottawa.ca\> for questions or comments. Pull requests are welcome! There's also the issues section (https://github.com/mbelmadani/moea-automatic-termination/issues) where you can file bugs or request enhancements.
