# DMS_experiments_rebuttal

## Figure Captions

### Exponential Graph (`figures/plot_best_acc_exp.pdf`)

```latex
\begin{figure}[h]
    \centering
    \includegraphics[width=0.48\textwidth]{figures/plot_/best_acc_exp.pdf}
    \caption{Best accuracy as a function of the number of machines $M \in \{9, 16, 36\}$
    on an exponential graph topology (spectral gap $1/\rho = \mathcal{O}(\log M)$),
    comparing \textsc{DMS} and \textsc{DAT-SGD}. Shaded bands denote standard deviation
    across random seeds. \textsc{DMS} consistently achieves higher accuracy and degrades
    more gracefully as $M$ grows. The decline observed at $M = 36$ is expected: this
    regime lies beyond the theoretical parallelism bound guaranteed by our analysis,
    and iterations are tracked past this threshold deliberately to expose the degradation
    behavior. Notably, \textsc{DMS} remains substantially more robust than
    \textsc{DAT-SGD} even in this over-parallel regime, highlighting its improved
    scalability on fast-mixing topologies.}
    \label{fig:exp_graph_accuracy}
\end{figure}
```

---

### Ring Graph (`figures/plot_best_acc_ring.pdf`)

```latex
\begin{figure}[h]
    \centering
    \includegraphics[width=0.48\textwidth]{figures/plot_best_acc_ring.pdf}
    \caption{Best accuracy as a function of the number of machines $M \in \{9, 16, 36\}$
    on a ring graph topology (spectral gap $\rho = \mathcal{O}(M^{-2})$),
    comparing \textsc{DMS} and \textsc{DAT-SGD}. Shaded bands denote standard deviation
    across random seeds. \textsc{DMS} maintains substantially higher accuracy across all
    values of $M$, retaining $\sim\!71\%$ accuracy at $M = 36$ while \textsc{DAT-SGD}
    collapses to $\sim\!14\%$. As with the exponential graph, the degradation at large
    $M$ is consistent with theory: $M = 36$ exceeds the theoretical parallelism bound,
    and we track iterations beyond this bound to illustrate the graceful degradation of
    \textsc{DMS} relative to \textsc{DAT-SGD}. The ring topology, being poorly connected,
    amplifies consensus bias --- making the advantage of \textsc{DMS}'s variance-reduced
    momentum most pronounced.}
    \label{fig:ring_graph_accuracy}
\end{figure}
