# DMS_experiments_rebuttal

### Exponential Graph

![Exponential Graph](figures/plot_best_acc_exp.png)

**Figure 1. Exponential Graph.**
Best accuracy as a function of the number of machines M in {9, 16, 36} on an exponential graph topology (spectral gap 1/rho = O(log M)), comparing DMS and DAT-SGD. Shaded bands denote standard deviation across random seeds. DMS consistently achieves higher accuracy and degrades more gracefully as M grows. The decline observed at M = 36 is expected: this regime lies beyond the theoretical parallelism bound guaranteed by our analysis, and iterations are tracked past this threshold deliberately to expose the degradation behavior. Notably, DMS remains substantially more robust than DAT-SGD even in this over-parallel regime, highlighting its improved scalability on fast-mixing topologies.

---

### Ring Graph

![Ring Graph](figures/plot_best_acc_ring.png)

**Figure 2. Ring Graph.**
Best accuracy as a function of the number of machines M in {9, 16, 36} on a ring graph topology (spectral gap rho = O(M^{-2})), comparing DMS and DAT-SGD. Shaded bands denote standard deviation across random seeds. DMS maintains substantially higher accuracy across all values of M, retaining ~71% accuracy at M = 36 while DAT-SGD collapses to ~14%. As with the exponential graph, the degradation at large M is consistent with theory: M = 36 exceeds the theoretical parallelism bound, and we track iterations beyond this bound to illustrate the graceful degradation of DMS relative to DAT-SGD. The ring topology, being poorly connected, amplifies consensus bias — making the advantage of DMS's variance-reduced momentum most pronounced.
