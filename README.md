# ProbeInformatics

The purpose of this project is to generate molecular properties and features for the 8-Aminoquinolines (8-AQ) Primaquine and Tafenoquine, and their fluorescent probes using the RDKit package. These probes were synthesized by Adonis McQueen, Ph.D for his dissertation work. Data for the Primaquine and Primaquine-Coumarin Probe (PQCP) were published in:

Bioorg Med Chem Lett. 2017 Oct 15; 27(20): 4597–4600.

Data for Tafenoquine and the Tafenoquine-Coumarin Probe(TQCP) are published in the dissertation document:

https://digitalcommons.usf.edu/etd/7062/

The data for the molecular characterization (<sup>1</sup>H-NMR, High Resolusion Mass Spectometry (HRMS), and fluorescent activity), anti-malarial activities, and fluorescent localization of the 8-AQ fluorescent probes in *Plasmodium falciparum* parasites are all within these two references.

## Compounds

Here are the molecular structures for the compounds:

![Primaquine]Probe_informatics_7_0.png

![PQCP]Probe_informatics_9_0.png

![Tafenoquine]Probe_informatics_8_0.png

![TQCP]Probe_informatics_10_0.png

## Comparison of Similarity Scores for Different Fingerprints

I was interested in how differnt fingerprint methods(Morgan, Avalon, MACCS) affected different types of similarity scoring (Tanimoto, Dice, Cosine). Here are the bar graphs depicting the different similarity scores for different fingerprints, using Primaquine (PQ) as a standard:

![Similarity Scoring using Morgan fingerprints]Probe_informatics_77_0.png
From the above image we can see that the similarity scoring is lowest for Tanimoto, while scoring for dice and cosine are relatively similar when using morgan fingerprints. Cosine seems to be consistently higher than dice across the molecules.

We see a similar trend when using MACCS and Avalon fingerprints as well:

![Similarity Scoring using MACCS]Probe_informatics_79_0.png

![similarity Scoring using Avalon]Probe_informatics_82_0.png

MACCS scores are closer in magnitude across molecules, but we see a similar trend for all molecules and fingerprints.
However, there's something interesting happening with the comparisons to Tafenoquine (TQ) and PQCP. Notice that the similarity score between PQ and PQCP is actually higher with Tanimoto scoring for Morgan fingerprints than the probe molecules, but when you examine MACCS and Avalon fingerprints, the similarity score is higher for PQ and TQ for Tanimoto scoring.

Why is this the case? Perhaps it's due to the fact that Morgan fingerprints have more bits to describe molecular features than MACCS (fixed at 162), and typically have more than Avalon, though they can overlap at 512 bits each. The 8-AQ core of the compound accounts for the similarity between all of these molecules when using PQ as a reference. 


## Repository Structure

```
├── README.md                           <- The top-level README for reviewers of this project
├── Probe_Informatics.ipynb             <- Data construction, fingerprint, similarity scores, and molecular descriptor calculations
├── Probedata.xlsx                      <- Dataframe with molecular descriptors and compound structures, but no similarity scores or fingerprint calculations.

```