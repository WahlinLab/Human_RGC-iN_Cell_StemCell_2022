## Human Retinal Ganglion Cell Neurons Generated by Synchronous BMP Inhibition and Transcription Factor Mediated Reprogramming

This repository contains code used for quality control and data analysis presented in: 

> Devansh Agarwal, Nicholas Dash, Kevin W. Mazo, Manan Chopra, Maria PA. Garcia, Amit Patel, Ryan M. Wong,
Cairang Jia, Hope Do, Jie Cheng, Colette Chiang, Shawna L. Jurlina, Mike Perry, Jong Rho, Risa Broyer, Cassidy
Lee, Robert N. Weinreb, Cezar Gavrilovici, Nick W. Oesch, Derek S. Welsbie, Karl J. Wahlin. Human Retinal Ganglion Cell Neurons Generated by Synchronous BMP Inhibition and Transcription Factor Mediated Reprogramming. *npj Regenerative Medicine* **8**, 55 (2023), https://doi.org/10.1038/s41536-023-00327-x.

----
## How to Use This Repository

We recommend using the miniconda package manager to run the notebooks in this repository. Here are step by step instructions on how to get your environment up and running on Linux/macOS. 

1. **Download [miniconda](https://docs.conda.io/projects/miniconda/en/latest/index.html#quick-command-line-install)**  
     In your terminal, enter the following text to download the latest version of miniconda:
   
        mkdir -p ~/miniconda3
        curl https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-arm64.sh -o ~/miniconda3/miniconda.sh
        bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
        rm -rf ~/miniconda3/miniconda.sh

   Initialize by entering the command ``~/miniconda3/bin/conda init bash``

2. **Clone into the repository**    
     In your terminal, navigate to the location you would like to store this repository, then enter  
   ``git clone https://github.com/WahlinLab/Human_RGC-iN``

3. **Initialize a conda environment**  
   Navigate into the cloned repository. Then, use the following command to set up a conda environment which contains all the packages needed to run every python script in the   repository:
   
   ``conda env create -f requirements.yml``
   
   After this command runs, use ``conda activate irgc_analysis`` to activate the environment.

5. **Run desired scripts**  
     Now that the environment is set up, you can recreate all the figures from the publication. We recommend using [Visual Studio Code](https://code.visualstudio.com) to run Jupyter files.
   
   Tutorials for setting up VS Code and conda environments can be found [here](https://code.visualstudio.com/docs/python/environments).
   
   The repository is organized in alignment with the figures in the publication, so to recreate a specific panel, simply navigate to the appropriate figure's folder.

6. **Important note for working with the Liang dataset**  
     For some scripts, data from Liang et. al. 2023 is used. This data is not included in the repository, and must be downloaded separately. For instructions, please see the ``README.md`` file located at ``~/Human_RGC-iN/sc_data/liang_adult_rgcs/``.

7. **Working with R Scripts**  
     To work with the R scripts in this repository, we recommend downloading [RStudio](https://posit.co/download/rstudio-desktop/). Once downloaded, open the ``.R`` file using RStudio to run. [Here](https://www.geeksforgeeks.org/creation-and-execution-of-r-file-in-r-studio/) is a quick tutorial to help get started. 

   

## Data Availability

Raw sequencing data is available in NCBI Sequence Read Archive (SRA) under the BioProject accession # [PRJNA885885](https://www.ncbi.nlm.nih.gov/bioproject/PRJNA885885) (bulk) and [PRJNA973095](https://www.ncbi.nlm.nih.gov/bioproject/PRJNA973095) (single-cell).

## Main Tools/Packages Used

| Package | Version | URL | 
| --- | --- | --- |
| FastQC | 0.11.5 | http://www.bioinformatics.babraham.ac.uk/projects/fastqc/ |
| MultiQC | 1.11 | https://multiqc.info|
| HISAT2-index-align | 2.2.1 | http://daehwankimlab.github.io/hisat2/ |
| featureCounts | 2.0.3 | http://subread.sourceforge.net/ |
| DESeq2 | 1.36 | http://www.bioconductor.org/packages/release/bioc/html/DESeq2.html |
| PIPseeker | 2.1 | https://www.fluentbio.com/resources/pipseeker-downloads/ |
| scanpy | 1.9.1 | https://scanpy.readthedocs.io/en/stable/ |
| scanorama | 1.7.3 | https://cb.csail.mit.edu/cb/scanorama/ |
| scvi-tools | 0.20.3 | https://docs.scvi-tools.org/en/stable/ |

For a full list of required packages please see ``requirements.yml``. 

## Reference Data

This work also utilizes data from the following publications:

1. Lu, Y. et al. Single-Cell Analysis of Human Retina Identifies Evolutionarily Conserved and Species-Specific Mechanisms Controlling Development. *Developmental Cell* **53**, 473-491.e9 (2020). https://doi.org/10.1016/j.devcel.2020.04.009.
2. Sridhar, A. et al. Single-Cell Transcriptomic Comparison of Human Fetal Retina, hPSC-Derived Retinal Organoids, and Long-Term Retinal Cultures. *Cell Reports* **30**, 1644-1659.e4 (2020). https://doi.org/10.1016/j.celrep.2020.01.007.
3. Gudiseva, H. V. et al. Single Cell Sequencing of Induced Pluripotent Stem Cell Derived Retinal Ganglion Cells (iPSC-RGC) Reveals Distinct Molecular Signatures and RGC Subtypes. *Genes* **12**, 2015 (2021). https://doi.org/10.3390/genes12122015.
4. Liang, Q. et al. A multi-omics atlas of the human retina at single-cell resolution. *Cell Genomics* **100298** (2023) https://doi.org/10.1016/j.xgen.2023.100298.

## Contact

If you have further questions, please do not hesitate to reach out!  

**Principle Investigator/Corresponding Author**  
Karl J Wahlin, PhD  
kwahlin[at]health[dot]ucsd[dot]edu  

**Bioinformatics Graduate Student**  
Manan Chopra  
m1chopra[at]ucsd[dot]edu
