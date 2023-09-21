# ProbeInformatics

The purpose of this project is to generate molecular properties and features for the 8-Aminoquinolines (8-AQ) Primaquine and Tafenoquine, and their fluorescent probes using the RDKit package. These probes were synthesized by Adonis McQueen, Ph.D for his dissertation work. Data for the Primaquine and Primaquine-Coumarin Probe (PQCP) were published in:

Bioorg Med Chem Lett. 2017 Oct 15; 27(20): 4597–4600.

Data for Tafenoquine and the Tafenoquine-Coumarin Probe(TQCP) are published in the dissertation document:

https://digitalcommons.usf.edu/etd/7062/

The data for the molecular characterization (<sup>1</sup>H-NMR, High Resolusion Mass Spectometry (HRMS), and fluorescent activity), anti-malarial activities, and fluorescent localization of the 8-AQ fluorescent probes in *Plasmodium falciparum* parasites are all within these two references.



## Repository Structure

```
├── README.md                           <- The top-level README for reviewers of this project
├── Probe_Informatics.ipynb             <- Data construction, fingerprint, similarity scores, and molecular descriptor calculations
├── Probedata.xlsx                      <- Dataframe with molecular descriptors and compound structures, but no similarity scores or fingerprint calculations.

```