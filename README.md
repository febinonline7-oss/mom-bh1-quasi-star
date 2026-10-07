# MoM-BH\*-1 as a classic quasi-star

Notebooks behind the draft research note **"A Classic Quasi-star Model for the Black Hole Star MoM-BH\*-1 Implies a ~10⁴ M☉ Black Hole"** by Febin S (in preparation for *Research Notes of the AAS*).

**Status:** draft, not yet submitted. Numbers may still change.

## What the note asks

MoM-BH\*-1 (z = 7.76) is the prototype "black hole star": a black hole embedded in dense gas (Naidu et al. 2026a). The note asks what a *classic* quasi-star model implies for it.

1. From the public JWST spectrum and photometry, the glowing surface is at about 5,200 ± 300 K and shines at about 2.9 × 10⁴⁴ erg/s.
2. In a classic quasi-star model (an n = 3 loaded polytrope with a Bondi inner boundary; Ball et al. 2011), that temperature implies a black hole of about 10⁴ solar masses.
3. This holds only for the classic inner boundary, which newer models dispute (Coughlin & Begelman 2024). It is what the classic model implies, not a measurement.

## Notebooks

Run them in this order. Each one explains itself step by step.

| Notebook | What it does | Where the note uses it |
|---|---|---|
| `balmer_break_MoM-BH1.ipynb` | Measures the Balmer break from the prism spectrum | Section 2 |
| `temperature_fit_MoM-BH1.ipynb` | Fits a blackbody to the continuum | Section 2 |
| `colour_temperature_MoM-BH1.ipynb` | Temperature from the F770W / F444W brightness ratio | Section 2 |
| `size_MoM-BH1.ipynb` | Luminosity and radius of the glowing surface | Section 2 |
| `sustain_simulator_MoM-BH1.ipynb` | Stages 1–2: the envelope model, and its tests against Ball et al. (2011) | Section 3 |
| `stage3_lifetime_MoM-BH1.ipynb` | Stage 3: growth of the black hole; test of the near-Eddington rule | Section 3 |
| `stage4_ai_inference_MoM-BH1.ipynb` | Stage 4: neural-network emulator and Bayesian inference of the masses | Section 4 |
| `stage5_three_weighings_MoM-BH1.ipynb` | Stage 5: is a near-Eddington envelope allowed? Robustness tests; Figure 1 | Sections 2, 4 and 5; Figure 1 |

`figure1_MoM-BH1.png` is Figure 1 of the note, made by the stage 5 notebook.

**A note on one number.** The earlier notebooks carry a colour temperature of 5,500 K. It came from the rounded magnitude in the discovery paper's text (25.4 mag). `colour_temperature_MoM-BH1.ipynb` uses the flux from the paper's table instead and gives about 5,400 K. The adopted temperature, 5,200 ± 300 K, covers both.

## How to run

Open a notebook in [Google Colab](https://colab.research.google.com) (File → Upload notebook) and run the cells from top to bottom (Shift + Enter). The notebooks download the public data they need. They use NumPy, SciPy, Matplotlib, Astropy, pandas and scikit-learn, which Colab already has.

## Data

- **Spectrum:** JWST/NIRSpec prism spectrum of MoM-BH\*-1 from Naidu et al. (2026a), [Zenodo record 15059215](https://zenodo.org/records/15059215), CC BY 4.0.
- **Photometry and line fits:** Naidu et al. (2026a), Nature, 656, 329 ([arXiv:2503.16596](https://arxiv.org/abs/2503.16596)).
- **Little-red-dot fits:** Curtis et al. (2026), [arXiv:2609.09265](https://arxiv.org/abs/2609.09265). The table is `summary/photospheric_parameters.csv` in [o-curtis/lrd-quasistar-fits](https://github.com/o-curtis/lrd-quasistar-fits), CC BY 4.0.
- **Comparison model:** Ball et al. (2011), MNRAS, 414, 2751 ([arXiv:1102.5098](https://arxiv.org/abs/1102.5098)), Table 1.

`curtis_table_copy.csv`, if present, is a copy of the Curtis et al. table saved by the stage 5 notebook on the day it was run. The values are unchanged. It stays under CC BY 4.0; please cite Curtis et al. (2026) if you use it.

## Use of AI tools

Claude (Anthropic) was used to help design the analysis, search and compare the literature, write these notebooks and draft the text of the note. I ran all notebooks, checked the results against published values, and take full responsibility for the content.

## License and contact

The code in these notebooks is released under the MIT License. For questions, please open an issue in this repository.
