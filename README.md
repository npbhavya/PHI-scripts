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
Table S7 and Table S8 in Supplementary Info

run the ipynb 'Achromobacter_ONT_SNPs_Pipline.ipynb' in this repo
- Input files; saved in 'Achromobacter ONT SNPs' folder in this repo
- This pipeline was used to identify and analyse single-nucleotide polymorphisms (SNPs) from Oxford Nanopore Technologies (ONT) sequencing data to investigate within-host variation during infection.
- Results -
      Saved in Supplementary Tables 7 and 8 in the manuscript 
