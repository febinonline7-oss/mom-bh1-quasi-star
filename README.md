# MoM-BH\*-1: too light and too cool to be a classic quasi-star

Notebooks behind the draft research note **"The Black Hole Star MoM-BH\*-1 Is Too Light and Too Cool to Be a Classic Quasi-star"** by Febin S (in preparation for *Research Notes of the AAS*).

**Status:** draft, not yet submitted. Numbers may still change.

## What the note finds

MoM-BH\*-1 (z = 7.76) is the prototype "black hole star": a black hole embedded in dense gas (Naidu et al. 2026a).

1. From the public JWST spectrum and photometry, its glowing surface is at about 5,200 ± 300 K and shines at about 2.9 × 10⁴⁴ erg/s. This agrees with the corrected atmosphere fit of Curtis et al. (2026).
2. A classic quasi-star (an n = 3 loaded polytrope with a Bondi inner boundary; Ball et al. 2011) shines near the Eddington limit of its whole mass. One this bright would weigh about 2 million solar masses and hold a black hole of about 10⁴ solar masses.
3. The corrected surface gravity of Curtis et al. (2026) allows only about 7,800 (2,300–58,000) solar masses inside the glowing surface, about 250 times less. At that mass the classic model has no solution: its surface would be at least 12,000–32,000 K.
4. So MoM-BH\*-1 is not a classic quasi-star, and its black hole is at most a few × 10⁴ solar masses.

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
| `stage4_ai_inference_MoM-BH1.ipynb` | Stage 4: neural-network emulator and Bayesian inference of the masses | Section 3 |
| `stage5_eddington_checks_MoM-BH1.ipynb` | Stage 5: the corrected surface gravity, the Hβ gas speed, the "no solution" test, and Figure 1 | Sections 2–6 and Figure 1 |

**Other notebooks** (not used in the note): `companion_search_MoM_BH1.ipynb` and `direct_collapse_test_MoM-BH1.ipynb`, a separate test of whether a neighbouring galaxy could have helped MoM-BH\*-1 form.

**Other files:**
- `figure1_MoM-BH1_v3.png` is Figure 1 of the note, made by the stage 5 notebook.
- `curtis_table_corrected.csv`, if present, is a copy of the corrected Curtis et al. table, saved by the stage 5 notebook on the day it was run. The values are unchanged. It stays under CC BY 4.0; please cite Curtis et al. (2026) if you use it.

**A note on one number.** The earlier notebooks carry a colour temperature of 5,500 K. It came from the rounded magnitude in the discovery paper's text (25.4 mag). `colour_temperature_MoM-BH1.ipynb` uses the flux from the paper's table instead and gives about 5,400 K. The adopted temperature, 5,200 ± 300 K, covers both.

## How to run

Open a notebook in [Google Colab](https://colab.research.google.com) (File → Upload notebook) and run the cells from top to bottom (Shift + Enter). The notebooks download the public data they need. They use NumPy, SciPy, Matplotlib, Astropy, pandas and scikit-learn, which Colab already has.

## Data

- **Spectrum:** JWST/NIRSpec prism spectrum of MoM-BH\*-1 from Naidu et al. (2026a), [Zenodo record 15059215](https://zenodo.org/records/15059215), CC BY 4.0.
- **Photometry, line fits and bolometric luminosity:** Naidu et al. (2026a), Nature, 656, 329 ([arXiv:2503.16596](https://arxiv.org/abs/2503.16596)), Extended Data Tables 2 and 4.
- **Little-red-dot fits:** Curtis et al. (2026), [arXiv:2609.09265](https://arxiv.org/abs/2609.09265). The table is `summary/photospheric_parameters.csv` in [o-curtis/lrd-quasistar-fits](https://github.com/o-curtis/lrd-quasistar-fits), CC BY 4.0. The note uses the corrected version (MoM-BH\*-1 is run BMKA_MoMBH1).
- **Comparison model:** Ball et al. (2011), MNRAS, 414, 2751 ([arXiv:1102.5098](https://arxiv.org/abs/1102.5098)), Table 1.

## Use of AI tools

Claude (Anthropic) was used to help design the analysis, search and compare the literature, write these notebooks and draft the text of the note. I ran all notebooks, checked the results against published values, and take full responsibility for the content.

## License and contact

The code in these notebooks is released under the MIT License. For questions, please open an issue in this repository.
