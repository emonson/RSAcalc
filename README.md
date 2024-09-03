# Download PDB files & Calculate RSA

- Eric E Monson, PhD – Duke University Libraries
- Amy Robinson, Duke University Chemistry Dept.

## Definitions

- [AlphaFold](https://alphafold.ebi.ac.uk) is a protein structure database
- [PDB](https://www.rcsb.org) is the Protein Data Bank, and is also a file format for storing protein structures
- [RSA](https://en.wikipedia.org/wiki/Relative_accessible_surface_area) stands for "Relative Solvent Accessibility" or "Relative accessible Surface Area" of protein residues

## Code notebook

The [Download_PDBs_Calculate_RSA.ipynb](https://github.com/emonson/RSAcalc/blob/main/Download_PDBs_Calculate_RSA.ipynb) 
notebook combines these actions:

- Query AlphaFold API for PDB URLs using protein accession numbers
- Check for Nulls in query results
- Download PDB files
- Load in PDB files and calculate RSA values
- Start to look at distribution of RSA values across species and residues

## Environment setup

I used the [Anaconda Python distribution](https://www.anaconda.com/download) to set up my Python environment for this work.

```
conda create --name rsa --channel conda-forge pandas jupyterlab biopython freesasa pyarrow openpyxl seaborn
conda activate rsa
```

## Credits

**Some functions below were taken from the original AlphaFold repo**

- Python Notebook by Kristoffer T. Bæk, 2022. 
- Original repository: [https://github.com/ktbaek/AlphaFold]()
