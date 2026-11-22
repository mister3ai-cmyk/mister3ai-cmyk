# Maksym Babych

Systems architect at Synapse Core. I build in-process vector search and memory
for AI-agent loops in C99. Every number below points to the code or record it
comes from.

## Layer 1 — Silicon / Deterministic Edge

*Engineering / tested: runs on ordinary CPUs, measured, reproducible from source.*

**[genesis-l0](https://github.com/mister3ai-cmyk/genesis-l0)**: in-process C99
L0 vector index in front of a local SQLite system of record. No sockets, no
server. Source under Apache-2.0.

- Recall@10 90.6 % against exact brute force at end-to-end p50 359–400 µs
  (OpenAI text-embedding-3-large, 33,234 vectors, 512-dim, shared AMD EPYC VPS).
  Script and conditions are in the README.
- `pip install genesis-l0` (0.2.0, Apache-2.0).
- `hologlyph/`: research L2 memory layer (trust, time, supersession, MCP
  adapter). Its LongMemEval figures come from the dev split only and are
  preliminary.

**[genesis-live-core](https://github.com/mister3ai-cmyk/genesis-live-core)**:
the R&D archive behind genesis-l0. The measured SRP-LSH cascade
([10.5281/zenodo.23447704](https://doi.org/10.5281/zenodo.23447704)), the
`rt_core` C99 kinematic gate with stack and instruction bounds checked on bare
Cortex-M4/M7 under QEMU (no physical board), and research branches.

## Layer 2 — Photonics / Wave Acceleration

*Simulation / R&D: no chip has been fabricated or measured.*

- Preprint: *Sublattice Zak phases and passive exceptional points in thin-film
  lithium niobate waveguide trimers: gauge, symmetry and fabrication-tolerance
  design rules*,
  [10.5281/zenodo.24057382](https://doi.org/10.5281/zenodo.24057382) (CC BY 4.0).
- Code reproducing all its numerical results:
  [10.5281/zenodo.24052931](https://doi.org/10.5281/zenodo.24052931) (Apache-2.0).
- Earlier concept notes from September 2026 are on Zenodo with correction
  notices dated 2026-11-08: they are design studies, not results.

New work in this track is kept in a private repository.

## Contact

contact@synapse-core.pp.ua
