
# Same same but different
![GitHub](https://img.shields.io/github/license/czodrowskilab/Same-same-but-different)
![GitHub](https://img.shields.io/badge/Stage-BETA-blue)

Same same but different is an open-source jupyter notebook intended to screen all ligands in the PDB [1] for your matched molecular pair (MMP) of interest. Therefore, the notebook makes use of mmpdb, an Open-Source Matched 
Molecular Pair Platform [2]. With the help of PyMOL [3] the crystal structures of MMP are aligned and then visualized with the open-source NGLview [4].
 
## Prerequisites

The Python dependencies are:
* Python >= 3.8
* RDKit >= 2020.03.6
* Pandas >= 1.1
* NGLview >= 2.7
* Jupyter >= 6.1

For the alignment of the PDB structures of your MMP, PyMOL is required. Open-source versions of PyMOL are also available (see https://pymolwiki.org/index.php/Category:Installation for more information).

### Installing

First of all you need a working Miniconda/Anaconda installation. You can get
Miniconda at https://conda.io/en/latest/miniconda.html.

Now you can create an environment named "mmp_pdb" with all needed dependencies and
activate it with:
```bash
conda env create -f environment.yml
conda activate mmp_pdb
```

You can also create a new environment by yourself and install all dependencies without the
environment.yml file:
```bash
conda create -n mmp_pdb python=3.8
conda activate mmp_pdb
```
In case of Linux or macOS:
````bash
conda install -c defaults -c rdkit -c conda-forge scikit-learn rdkit jupyterlab matplotlib seaborn nglview 
````

In case of Windows:
```bash
conda install -c defaults -c rdkit scikit-learn rdkit jupyterlab matplotlib seaborn nglview 
```

## Usage

To use Same same but different you have to be in the repository folder and your conda environment has to be activated.
Further descriptions are found in the jupyter notebook.

**Important note:** for now, execution of the notebook requires about 130 GB of RAM for this particular dataset.
We are working on an improvement regarding that issue.



## Datasets

1. `200922_pdbID_uniprotID_LigID-Smiles.csv` - All Ligands in the PDB. Advanced search to get UniProtID/GeneBankID. Columns contain "EntryID", "UniprotID", "DB_name", "LigID", "LigSMILES". Since the maximum number of lines is limited to 5000, the files were downloaded manually and merged into this file in the terminal. Date of the download on https://www.rcsb.org: 09/22/2020  

## Authors

**Helge Vatheuer** - [GitHub](https://github.com/hlgvth), [E-Mail](mailto:helge.vatheuer@tu-dortmund.de)<br>
**Marcel Baltruschat** - [GitHub](https://github.com/mrcblt), [E-Mail](mailto:marcel.baltruschat@tu-dortmund.de)<br>
**Paul Czodrowski** - [GitHub](https://github.com/czodrowskilab), [E-Mail](mailto:czodpaul@uni-mainz.de)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## References

[1] H.M. Berman, J. Westbrook, Z. Feng, G. Gilliland, T.N. Bhat, H. Weissig, I.N. Shindyalov, P.E. Bourne.
(2000) The Protein Data Bank *Nucleic Acids Research*, 28: 235-242.<br>
[2] A. Dalke, J. Hert, C. Kramer. mmpdb: An Open-Source Matched Molecular Pair Platform for Large Multiproperty Data Sets. *J. Chem. 
Inf. Model.*, **2018**, *58 (5)*, pp 902–910. https://pubs.acs.org/doi/10.1021/acs.jcim.8b00173 <br>
[3] PyMOL. The PyMOL Molecular Graphics System, Version 2.0 Schrödinger, LLC. <br>
[4] H. Nguyen, D.A. Case, A.S. Rose; NGLview - Interactive molecular graphics for Jupyter notebooks, Bioinformatics, , btx789, https://doi.org/10.1093/bioinformatics/btx789. <br>
[5] RDKit, Open-Source cheminformatics; http://www.rdkit.org.<br>
