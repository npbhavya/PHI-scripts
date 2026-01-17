# PHI-scripts
Repository to save the scripts run for a paper. 

Tararseko et al., In prep

## Bacterial genome features visualisation 
Figure 1B, 1C, 1D, 2C, 2E, and 3

Run the ipynb `Achromobacter_Genome_Plots.ipynb` in this repo
The input files for this code are provided in this repo under "Files". The names should match the file names being called in the notebook

## Phage gene similarity visulisation 
Fig 2D in the manuscript

Run the ipynb `Achromobacter_Phage_genome_Viz.ipynb` in this repo
- Input: genbank files for the phages
- Output: 
    - Figure in the notebook 
    - `Phage_gene_matrix.csv` contains all-against-all gene similarity scores for all genes across all Achromobacter phages

Also Fig S2 that includes marking the tail-associated gene clusters

## Pearson correaltions 
Figure 4 and Table S6 generation 

Run the ipynb `Achromobacter_PearsonCorrelations.ipynb` 
- Input files: saved in `Files` folder in this repo
- Methods: Spearman correalations with Benjamini-Hochberg correction. 
    Testing for signficant assocaitions to infectivity among bacterial and phage tail assocated genes 
- Results - 
    Saved in Supplementary Table 6 in the manuscript
    Figure 4 in manuscript


## Linear mixed models
Provided as the supplementary Methods, and here in document `Supplementary Methods-LMM.docx`. In this document, summarise the different models tested before selecting the one for the paper. 

The code testing these models is saved to `Achromobacter_LMM.ipynb`. 
    - Input: saved in Files, `merged_all_data.csv`
