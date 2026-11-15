# An erasure-native multi-qubit architecture for twisted Janus WSSe/MoSSe bilayers: dark valley–Kramers qubits on a self-addressed sublattice, a mirror ancilla lattice, and dipolar-blockade gates

> **Status: in revision.** An internal adversarial audit found issues that are being corrected; the summary below reports only results that survived it.

Companion repository: [janus-wsse-mosse-colocalization](https://github.com/FarukSamiBilgin/janus-wsse-mosse-colocalization). The companion's numbers are being recomputed, so **no Janus-derived numbers are reported here**; figures, scripts and numerical results are withheld until that is done.
System-level feasibility study: [moire-300-logical-qubit-feasibility](https://github.com/FarukSamiBilgin/moire-300-logical-qubit-feasibility).

## Question

In R-stacked polar Janus moiré bilayers (twisted WSSe and MoSSe), electrons and holes co-localize on one moiré sublattice, spectrally separated from its mirror sublattice. Can the platform's natural dualities be mapped onto the roles of a quantum processor so that the leading gate error becomes a located erasure?

## Architecture concept

- **Data / ancilla:** the co-localization sublattice hosts data qubits; the spectrally separated mirror sublattice hosts ancillas.
- **Memory / gate rail:** logical information lives in the dark valley–Kramers pair; two-qubit gates are dipolar-blockade CZ gates run on the bright-exciton rail.
- **Erasure-native errors:** the dominant gate failure, radiative decay on the bright rail, emits a photon, which converts it into a located (heralded) erasure.
- **Configuration vs. runtime:** ferroelectric (permanent) control sets configuration; Stark (volatile) control acts at runtime.
- **Staged error correction:** a passive envelope, a biased-erasure XZZX code, and an autonomous layer gated behind written go/no-go criteria.

## Results that survived the audit (qualitative)

- The mapping of the four platform dualities onto processor roles, and the observation that bright-rail decay heralds its own error, are the architecture's conceptual contributions.
- Slow spectral diffusion inside data–data gate windows is identified as the hardest requirement; syndrome gates on the ancilla line are markedly more tolerant.

## Open problems (being corrected)

- Quantitative inputs (static dipole, blockade energies, gate errors, threshold margin) depend on the companion paper and are being recomputed.
- Site addressing must start from a measured site map; Stark gradients can only make common-mode adjustments over blocks, and drift feed-forward removes only the spatially correlated part of the drift.
- The hBN nuclear-spin dephasing floor, gate-resolution limits and static disorder must be added to the limitations; the autonomous layer is an upper bound, not a claimed net gain.
- The system-level study in [moire-300-logical-qubit-feasibility](https://github.com/FarukSamiBilgin/moire-300-logical-qubit-feasibility) finds per-site/per-bond control layers fatally limited by disorder for this platform family; this architecture does not claim otherwise.

## Repository layout

- `paper/ABSTRACT.md`: extended abstract (manuscript unpublished).
- `scripts/`, `results/`, `figures/`: placeholders; content withheld pending recomputation.

## AI assistance

AI assistance: AI coding assistants were used for code development and for adversarial review. All load-bearing results were re-derived by independent methods and checked by automated tests; the author is responsible for every claim.

## Citation

Faruk Sami Bilgin (Independent Researcher, ORCID [0009-0001-9064-4410](https://orcid.org/0009-0001-9064-4410)), unpublished manuscript in revision, 2026. See `CITATION.cff`.

License: code MIT (`LICENSE`); text, figures and data CC BY 4.0 (`LICENSE-CONTENT`).
