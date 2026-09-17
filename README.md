# Casimir Force Model

Numerical comparison of theoretical models for the Casimir interaction between a sphere and
a plate, each normalised against the proximity force approximation.

**Undergraduate research model · University College London**

![Python](https://img.shields.io/badge/Python-3.x-blue)
![SciPy](https://img.shields.io/badge/SciPy-constants-8caae6)
![Topic](https://img.shields.io/badge/topic-quantum%20vacuum-orange)
![License](https://img.shields.io/badge/License-MIT-green)

## Overview

The Casimir effect is an attractive force between neutral bodies arising from quantum vacuum
fluctuations. For sphere–plate geometry there is no single exact expression, so several
approximations are used in different regimes — and they disagree.

This model implements three and compares them directly:

- **Proximity force approximation (PFA)** — `E ∝ −ħcR / (L − 2R)²`, valid when the separation
  is small relative to the sphere radius. Used here as the normalising baseline.
- **Casimir–Polder** — `E ∝ −ħcR⁶ / L⁷`, the large-separation limit where the sphere behaves
  as a point polarisable object.
- **Perfect metal expansion** — a nine-term series in `R/L`, capturing the crossover region
  between the two limits where neither simple expression holds.

Each model is divided through by the PFA energy, so the plots show directly where the
approximations agree and where they diverge as a function of `R/L`.

## Notebooks

| Notebook | Content |
| --- | --- |
| `Force_Calculations.ipynb` | The three energy models as functions of separation `L` and sphere radius `R` |
| `Plotting the  Perfect Metal Values.ipynb` | Evaluating and plotting the models against one another |

Physical constants come from `scipy.constants`, so results are in SI units throughout.

## Author

Harvey Bermingham — MSci Physics, University College London

## License

Released under the MIT License. See [LICENSE](LICENSE).
