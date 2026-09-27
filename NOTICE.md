# Third-Party Notices

This repository is a personal portfolio project built on top of, and reporting
results from, several third-party open-source tools and design examples.
Only the analysis, documentation, curated report excerpts, and extended
write-up in this repository are original — everything below is credited to
its respective upstream project.

## Toolchain

- **[OpenROAD](https://github.com/The-OpenROAD-Project/OpenROAD)** and
  **[OpenROAD-flow-scripts](https://github.com/The-OpenROAD-Project/OpenROAD-flow-scripts)**
  — BSD 3-Clause License, Copyright (c) 2018-2023, The Regents of the
  University of California. Used here as the physical design flow
  (floorplan, placement, CTS, routing, STA) and as the source of the
  `gcd` example design, its default configuration, and initial SDC.
- **[Yosys](https://github.com/YosysHQ/yosys)** — ISC License. Used for RTL
  synthesis.
- **[KLayout](https://www.klayout.de/)** — GPL v3 License. Used to view the
  produced GDSII layout.

## RTL Example

`rtl/gcd.v` originates from the `gcd` example design shipped with
OpenROAD-flow-scripts (`flow/designs/src/gcd/gcd.v`), which is itself
"Originally Generated from PyMTL" (a Python-based hardware description
framework) per the file's own header comment. It carries no separate
license header of its own and is distributed here under the same terms as
the OpenROAD-flow-scripts repository (BSD 3-Clause).

## Process Design Kits (PDKs)

- **Nangate45 / FreePDK45** — an open academic standard-cell library
  originally from Nangate / NCSU, bundled with OpenROAD-flow-scripts for
  teaching and research use. Not intended for commercial tapeout.
- **[SkyWater SKY130 PDK](https://github.com/google/skywater-pdk)** — Apache
  License 2.0, © SkyWater Technology Foundry / Google. A real, open-source,
  fabricatable 130nm process, used here for cross-process comparison only.

## What This Means For You

If you reuse this repository:
- The README, documentation, curated `.rpt`/`.json` excerpts, and the
  `docs/RTL-to-GDSII-GCD-Review.html` write-up are yours to reuse under the
  [MIT License](LICENSE) in this repo.
- If you reuse `rtl/gcd.v`, the `config/`, or `constraints/` files, retain
  attribution to OpenROAD-flow-scripts and comply with its BSD 3-Clause
  terms.
- If you reference sky130-specific results, note SkyWater's Apache 2.0
  license and attribution requirements.
