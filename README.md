# Replication: Why Don’t the Poor Save More? Evidence from Health Savings Experiments

Pascaline Dupas and Jonathan Robinson — *American Economic Review (2013)*.

This [stats.camp](https://stats.camp) repository preserves official AEA deposit
**116115, version V1**, for replication and engine compatibility testing.
**Status: executed on 2026-10-16 and again on 2026-10-17 in the native stats.camp engine from scratch copies; the package runs end to end in the engine.**
The deposited datasets retain their original bytes and archive-relative paths.
Documentation is adapted for stats.camp.

## The study

Uses a field experiment in Kenya to compare informal savings technologies and their effects on health investment and the ability to cope with illness.

## Contents and entry points

The deposit contains the individual-level merged survey dataset, the ROSCA-level master list, and the complete main/appendix analysis script. The code includes clustered regressions, treatment comparisons, and legacy `dprobit`.

The source archive contains **5 original files** totaling
**685,651 bytes**. The source ZIP is
241,775 bytes. Deposited data, reference outputs, and ancillary files are retained;
documentation is adapted for stats.camp.

Analysis entry point:

- [data_AER20110911/HARP_analysis.do](data_AER20110911/HARP_analysis.do)

Authors’ documentation, adapted for stats.camp:

- [data_AER20110911/README_AER20110911.txt](data_AER20110911/README_AER20110911.txt)

## Setup and current scope

The script reads relative dataset names and should be launched from `data_AER20110911/`. It contains semicolon delimiters, legacy `for` loops, `pause on` and interactive `pause` commands. No pauses have been disabled; unattended execution requires a deliberate runtime policy.

The 2026-10-16 runs used scratch copies, so the figures, logs and intermediate
datasets in this repository are still the authors' deposited reference material.

## Inspect in stats.camp

These links open the deposited files for inspection. They do not establish
that the preserved paths, dependencies, or commands are executable in the browser.

- [data_AER20110911/HARP_analysis.do](https://stats.camp/app?open=https%3A%2F%2Fgithub.com%2Fstats-camp%2Freplication-health-savings.git&file=data_AER20110911%2FHARP_analysis.do)

## Source integrity and attribution

- [Official deposit](https://www.openicpsr.org/openicpsr/project/116115/version/V1/view)
- [Deposit DOI](https://doi.org/10.3886/E116115V1)

Archive: `116115-V1.zip`. SHA-256:
`d69f9679052e5b1eea6b31992f53b551595ca267955b6990772254935dab01c7`.

All original file hashes were checked after extraction. `.gitattributes` disables
Git line-ending normalization. Empty folders are represented by `.gitkeep`
files. The root README and Git configuration are stats-camp additions.

The deposited `LICENSE.txt` is retained without modification. It supplies the original code/data terms; this mirror does not relicense the research.

The study, code, and data remain credited to Pascaline Dupas and Jonathan Robinson; stats-camp maintains
this mirror and its preparation documentation.
