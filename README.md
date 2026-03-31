# DMS_experiments_rebuttal

# Figures and Captions Template

## Basic Markdown Format

### Figure 1: [Title of Figure]
![Figure 1 Alt Text](figures/figure_1.png)
**Caption:** Write your detailed caption here explaining what the figure shows, the methodology, key findings, or relevant context.

---

## LaTeX Format (for academic papers)

### Figure 2: [Title of Figure]
```latex
\begin{figure}[h]
    \centering
    \includegraphics[width=0.8\textwidth]{figures/figure_2.png}
    \caption{Write your detailed caption here. Explain what the figure demonstrates, 
    include statistical information if relevant, and any important observations.}
    \label{fig:figure2}
\end{figure}
```

---

## Multiple Figures Side-by-Side

### Figure 3 & 4: [Combined Title]
```latex
\begin{figure}[h]
    \centering
    \begin{subfigure}{0.48\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figures/figure_3a.png}
        \caption{First result showing [description]}
        \label{fig:3a}
    \end{subfigure}
    \hfill
    \begin{subfigure}{0.48\textwidth}
        \centering
        \includegraphics[width=\textwidth]{figures/figure_3b.png}
        \caption{Second result showing [description]}
        \label{fig:3b}
    \end{subfigure}
    \caption{Combined caption explaining the relationship between the subplots.}
    \label{fig:3and4}
\end{figure}
```

---

## Caption Best Practices

- **Be descriptive:** Explain what the figure shows, not just label it
- **Include units:** If applicable, mention scales, axis units, or percentages
- **Reference data:** Cite the source or method if relevant
- **Keep it concise but complete:** Avoid one-word captions, but don't be overly verbose
- **Use past tense:** "showed," "demonstrated," "observed"

### Example Caption Structure
*[What was measured/shown] - [how many subjects/trials] - [key finding or result]. [Additional context or interpretation].*

---

## File Organization

```
DMS_experiments_rebuttal/
├── README.md
├── FIGURES_TEMPLATE.md (this file)
└── figures/
    ├── figure_1.png
    ├── figure_2.png
    └── ... (add your figure files here)
```

---

## Quick Copy-Paste Templates

### Simple Figure
```markdown
![Figure X Alt Text](figures/figure_x.png)
**Figure X – [Title]:** [Caption describing the figure]
```

### Inline Reference
```latex
Figure~\ref{fig:figureName} shows [reference to figure content]
```

---

**Instructions:** Replace `[...]` with your actual content, update file names and paths, and save your figure files in the `figures/` folder.
