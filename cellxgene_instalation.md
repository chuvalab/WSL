# Installing CELLxGENE 
[CELLxGENE](https://github.com/chanzuckerberg/cellxgene) is an an interactive explorer for single-cell transcriptomics data. It can be very useful to explore your recently analyzed single-cell dataset 
or a dataset you just downloaded from a repository

## Prerequisites
* You have already intalled Ubuntu through WSL on your windows machine, along with conda. Or you have a machine with any Linux distribution and conda isntalled

## Create a conda environment and isntall cellxgene
The first line creates a conda environment called cellxgene and installs python in it. The second activates it
```
conda create --name cellxgene python
conda activate cellxgene
```

Now you can use pip to install cellxgene:
```
pip install cellxgene
```

## Open your favorite dataset with cellxgene
cellxgene can open files with `h5ad` extension. Locate your file and open it with something like:
```
cellxgene launch /mnt/c/Users/my_username/Downloads/aorta.h5ad
```

Click on the resulting URL and a new tab will open in your browser. Do not close the terminal! 

After you are done, you can press ctrl+c to exit cellxgene process or just close the terminal.

If you want to know more about how to access the files saved on your machine from within your Ubuntu isntalation, you can read more here

