# Closing the Variance Gap: Spectral PINN for Lévy-Driven SPDEs

**Hubert Lipski** — 2026

## Repository structure

```
spde/
├── paper_v2_jcp/               # JCP submission (Spectral PINN only)
│   ├── paper_jcp_short.tex     # 35-page condensed version ← SUBMIT THIS
│   ├── paper_jcp_short.pdf     # Compiled PDF
│   ├── paper_jcp_full.tex      # 43-page uncompressed version
│   ├── paper_jcp_full.pdf      # Compiled PDF
│   └── references.bib
│
├── paper_v3_fno_standalone/    # Companion paper (Spectral FNO)
│   ├── paper_fno_standalone.tex
│   └── paper_fno_standalone.pdf
│
├── paper_v1/                   # Original version (23 pages, PINN-only)
│   ├── paper.tex
│   └── paper.pdf
│
├── paper_figures/              # Publication figures
│   ├── fig01_method_compare.pdf
│   ├── fig02_variance_gap.pdf
│   ├── fig03_logpsd_bars.pdf
│   ├── fig04_y_outlier.pdf
│   ├── fig05_field_snapshots_spectral.pdf
│   ├── fig06_field_snapshots_fno.pdf
│   ├── fig07_field_errors_spectral.pdf
│   ├── fig08_field_errors_fno.pdf
│   ├── fig09_fno_vs_pinn_evolution.pdf
│   ├── fig10_unified_comparison.pdf
│   ├── fig11_comprehensive_spectral.pdf
│   ├── fig12_comprehensive_fno.pdf
│   ├── fig13_summary_metrics_table.pdf
│   ├── fig14_psd_comparison_2d.pdf
│   ├── fig15_ablation.pdf
│   ├── fig16_spectral_fno_var.pdf
│   ├── fig17_spectral_fno_logpsd.pdf
│   ├── fig_ablation.pdf
│   ├── fig_grid_convergence.pdf
│   ├── fig_spectral_fno_logpsd.pdf
│   └── fig_spectral_fno_var.pdf
│
├── results_data/               # Raw evaluation metrics
│   ├── summary_eval.json       # Spectral FNO eval (5 problems × 2 variants)
│   ├── summary.json            # Training losses (10 runs)
│   ├── grid_convergence_vanilla.json
│   ├── grid_convergence_spectral.json
│   └── grid_convergence_compare.md
│
└── README.md
```

## Key results

- **Spectral PINN** closes variance gap: 0.19→0.83 (hierarchical z-channel), 0.50→0.93 (Burgers-VG)
- **Spectral FNO** closes variance gap: 0.20→0.95 (Heston-VG, 16× improvement)
- **Grid convergence**: Δ L_var varies by <0.015 across 4× grid range
- **Ablation**: all three loss components needed (5×5 seed study)
- **Theory**: Proposition 1 (Gaussian separable convergence), structural argument via Bochner

## Compilation

```bash
cd paper_v2_jcp
pdflatex paper_jcp_short && bibtex paper_jcp_short && pdflatex paper_jcp_short && pdflatex paper_jcp_short
```

## Citation

```bibtex
@article{lipski2026closing,
  author  = {Hubert Lipski},
  title   = {Closing the Variance Gap: Spectral PINN for L\'{e}vy-Driven SPDEs},
  journal = {Submitted to Journal of Computational Physics},
  year    = {2026}
}
```
