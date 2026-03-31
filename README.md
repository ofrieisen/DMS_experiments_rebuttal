# DMS_experiments_rebuttal

<img src="figures/plot_best_acc_exp.png" width="30%">

**Figure 1. Exponential Graph.**
Best accuracy on MNIST as a function of the number of machines M in {9, 16, 36} on an exponential graph topology (1/rho = O(log M)). Each machine receives heterogeneous data (8 out of 10 classes); the test set comprises all 10 classes. Shaded bands denote standard deviation across random seeds. DMS consistently achieves higher accuracy than DAT-SGD across all values of M, and degrades more gracefully as the number of machines increases. At M = 9 and M = 16, both methods perform comparably, but at M = 36 the gap widens significantly: DMS retains ~37% accuracy while DAT-SGD drops to ~12%. The decline at M = 36 is expected, as this regime lies beyond the theoretical parallelism bound guaranteed by our analysis; we deliberately track iterations past this threshold to expose the degradation behavior. Notably, DMS remains substantially more robust than DAT-SGD even in this over-parallelized regime, demonstrating that the variance-reduced momentum mechanism of DMS effectively mitigates consensus bias and enables better utilization of additional machines. This highlights DMS's improved scalability on fast-mixing topologies, consistent with our theoretical finding that DMS achieves a parallelism bound of O(N^{3/16}) on exponential graphs compared to O(N^{1/6}) for DAT-SGD.


### Ring Graph

<img src="figures/plot_best_acc_ring.png" width="30%">

**Figure 2. Ring Graph.**
Best accuracy on MNIST as a function of the number of machines M in {9, 16, 36} on a ring graph topology (spectral gap rho = O(M^{-2})). Each machine receives heterogeneous data (8 out of 10 classes); the test set comprises all 10 classes. Shaded bands denote standard deviation across random seeds. DMS and DAT-SGD perform comparably at M = 9 (~85%), but their behavior diverges sharply as M increases: at M = 36, DMS retains ~71% accuracy while DAT-SGD collapses to ~14%. The poor performance of DAT-SGD at high M is partly due to iterations being truncated after a fixed budget, which limits convergence when M exceeds the parallelism bound. The ring topology, being the most poorly connected graph considered (rho = O(M^{-2})), amplifies consensus bias and makes the parallelism bottleneck most severe. Despite this challenging setting, DMS maintains strong performance by leveraging its variance-reduced momentum to effectively control the consensus distance. This result is consistent with our theoretical analysis, which shows that DMS achieves a parallelism bound of O(N^{3/16}) on ring graphs compared to O(N^{1/6}) for DAT-SGD, enabling significantly more machines to be utilized before performance degrades. 
