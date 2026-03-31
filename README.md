# DMS Experiments — Rebuttal Figures

## Figure Captions

### Figure 1: Ring Graph

![Ring Graph](figures/plot_best_acc_ring.pdf)

**Caption:** Best accuracy as a function of the number of machines M in {9, 16, 36} on a ring graph topology (spectral gap rho = O(M^{-2})), comparing DMS and DAT-SGD. Shaded bands denote standard deviation across random seeds. DMS maintains substantially higher accuracy across all values of M, retaining ~71% accuracy at M = 36 while DAT-SGD collapses to ~14%. The degradation at large M is consistent with theory: M = 36 exceeds the theoretical parallelism bound, and iterations are tracked beyond this bound to illustrate the graceful degradation of DMS relative to DAT-SGD. The ring topology, being poorly connected, amplifies consensus bias — making the advantage of DMS's variance-reduced momentum most pronounced.

---

### Figure 2: Exponential Graph

![Exponential Graph](figures/plot_best_acc_exp.pdf)

**Caption:** Best accuracy as a function of the number of machines M in {9, 16, 36} on an exponential graph topology (spectral gap 1/rho = O(log M)), comparing DMS and DAT-SGD. Shaded bands denote standard deviation across random seeds. DMS consistently achieves higher accuracy and degrades more gracefully as M grows. The decline observed at M = 36 is expected: this regime lies beyond the theoretical parallelism bound guaranteed by our analysis, and iterations are tracked past this threshold deliberately to expose the degradation behavior. Notably, DMS remains substantially more robust than DAT-SGD even in this over-parallel regime, highlighting its improved scalability on fast-mixing topologies.

---

## LaTeX (copy-paste for paper)

<details>
<summary>Click to expand LaTeX source</summary>

### Side-by-Side Combined Figure

```latex
\begin{figure}[h]
    \centering
    \begin{subfigure}{0.48\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figures/plot_best_acc_ring.pdf}
        \caption{Ring graph ($\rho = \mathcal{O}(M^{-2})$)}
        \label{fig:ring_accuracy}
    \end{subfigure}
    \hfill
    \begin{subfigure}{0.48\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figures/plot_best_acc_exp.pdf}
        \caption{Exponential graph ($1/\rho = \mathcal{O}(\log M)$)}
        \label{fig:exp_accuracy}
    \end{subfigure}
    \caption{Best accuracy vs.\ number of machines $M \in \{9, 16, 36\}$ for
    \textsc{DMS} and \textsc{DAT-SGD} on ring and exponential graph topologies.
    Shaded bands denote standard deviation across random seeds. \textsc{DMS}
    consistently outperforms \textsc{DAT-SGD} and degrades more gracefully as $M$
    increases. The accuracy decline at $M = 36$ is consistent with theory: this point
    exceeds the theoretical parallelism bound, and iterations are deliberately tracked
    beyond this threshold to expose degradation behavior. \textsc{DMS}'s advantage is
    most pronounced on the ring, where poor connectivity amplifies consensus bias and
    makes the gains from variance-reduced momentum most significant.}
    \label{fig:accuracy_topologies}
\end{figure}
```

### Standalone: Ring Graph

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
```

### Standalone: Exponential Graph

```latex
\begin{figure}[h]
    \centering
    \includegraphics[width=0.48\textwidth]{figures/plot_best_acc_exp.pdf}
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

</details>
