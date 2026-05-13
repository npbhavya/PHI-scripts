# PHI-scripts
A repository to save the scripts run for a paper. 

Tararseko et al., In prep

## Bacterial genome features visualisation 
Figure 1B, 1C, 1D, 2C, 2E, and 3

Run the ipynb `Achromobacter_Genome_Plots.ipynb` in this repo
The input files for this code are provided in this repo under "Files". The names should match the file names being called in the notebook

## Phage gene similarity visualisation 
Fig 2D in the manuscript

Run the ipynb `Achromobacter_Phage_genome_Viz.ipynb` in this repo
- Input: GenBank files for the phages
    - saved to `Files/gbk`

- Output: 
    - Figure in the notebook 
    - `Phage_gene_matrix.csv` contains all-against-all gene similarity scores for all genes across all Achromobacter phages

Also, Fig S2 includes marking the tail-associated gene clusters

## Pearson correlations 
Figure 4 and Table S6 generation 

Run the ipynb `Achromobacter_PearsonCorrelations.ipynb` 
- Input files: saved in `Files` folder in this repo
- Methods: Spearman correlations with Benjamini-Hochberg correction. 
    Testing for significant associations to infectivity among bacterial and phage tail assocated genes 
- Results - 
    Saved in Supplementary Table 6 in the manuscript
    Figure 4 in the manuscript

## Linear mixed models
Provided as the supplementary Methods, and here in the document `Supplementary Methods-LMM.docx`. In this document, summarise the different models tested before selecting the one for the paper. 

The code that tests these models is saved in `Achromobacter_LMM.ipynb`. 
    - Input: saved in Files, `merged_all_data.csv`

## Longitudinal Variant Analysis

This workflow generates:

- **Table S7** — Pairwise SNP distances across the shared callable core genome  
- **Table S8** — Functionally annotated SNPs between longitudinal isolates  

These results are reported in the **Supplementary Information** of the manuscript.

### Run the Analysis
- Open and run the ipynb `Longitudinal Variant Analysis.ipynb` in this repo

### Input Files

Upload all required files to the `Longitudinal Variant Analysis.ipynb` 

| File | Description |
|---|---|
| `aura_ref.fasta` | Reference genome used for read mapping and SNP calling |
| `aura_ref.gff` or `aura_ref.gff3` | Genome annotation required for SNP annotation (Table S8) |
| `neet.fastq` | Oxford Nanopore reads for T0 isolate |
| `aura.fastq` | Oxford Nanopore reads for T1 isolate |
| `cram.fastq` | Oxford Nanopore reads for T2 isolate |

### Workflow Overview

1. **Read mapping** — Aligns ONT reads to the *A. insolitus aura* reference genome using minimap2.  
2. **SNP calling** — Identifies variants using Longshot.  
3. **SNP filtering** — Retains high-confidence SNPs (`QUAL ≥ 30`, `DP ≥ 20`).  
4. **Core genome definition** — Identifies regions with sufficient coverage across all isolates and defines the shared callable core genome (~6.4 Mb).  
5. **Consensus sequence generation** — Generates per-isolate core genome sequences.  
6. **Pairwise SNP comparison (Table S7)** — Calculates SNP counts and SNP density between isolates.  
7. **SNP annotation (Table S8)** — Assigns gene context, functional effects, and amino acid changes.  

### Output Files

| Output | Description |
|---|---|
| `Table_S7.csv` | Pairwise SNP distances: isolate pair, core genome size, SNP count, SNPs per Mb |
| `Table_S8.csv` | Annotated SNPs: genomic position, gene/locus tag, product annotation, effect, amino acid change |

