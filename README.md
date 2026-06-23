# PHI-scripts
A repository to save the scripts run for  Achromobacter phages paper in prep.

Tararseko, Papudeshi et al., In prep

## Bacterial genome features visualisation 
Figure 1B, 1C, 1D and 3

Run the ipynb `Achromobacter_Genome_Plots.ipynb` in this repo
The input files for this code are provided in this repo under "Files". The names should match the file names being called in the notebook

## Phage gene similarity visualisation 
Fig 2B in the manuscript

Run the ipynb `Achromobacter_Phage_genome_Viz.ipynb` in this repo
- Input: GenBank files for the phages
    - saved to `Files/gbk`

- Output: 
    - Figure in the notebook 
    - `Phage_gene_matrix.csv` contains all-against-all gene similarity scores for all genes across all Achromobacter phages

Also, Fig S2 includes marking the tail-associated gene clusters

Fig 2C in the manuscript

Run the the ipynb `Achromobacter_PearsonCorrelations.ipynb` 
- Input: Input files: saved in `Files/eop_raw_values.csv` folder in this repo
- Output: Figure in the notebook, containing the log normalised EOP values for each bacteria-phage interaction 

## Linear mixed models
Provided as the supplementary Methods, and here in the document `Supplementary Methods-LMM.docx`. In this document, summarise the different models tested before selecting the one for the paper. 

Figure 4B and Figure 4C, Figure S3, S4 

The code that tests these models is saved in `Achromobacter_LMM_clean.ipynb`. 
    - Input: saved in Files, `merged_all_data.csv`
