
# LDSC (LD SCore) `v2.0.1` - updates to work with Python3

`ldsc` is a command line tool for estimating heritability and genetic correlation from GWAS summary statistics. `ldsc` also computes LD Scores.
Updates from [PyPi ldsc v2.0.1](https://pypi.org/project/ldsc/#files) with additional updates from `svdorn` to work with Python3.

## Getting Started



In order to download `ldsc`, you should clone this repository via the commands:
```  
git clone https://github.com/svdorn/ldsc-2.0.1.git
cd ldsc-2.0.1
```

In order to install the Python dependencies, run the following commands from the ldsc-2.0.1 :

```
pip install .
```
This will install dependancies from setup.py.   

If this doesn't work, setup an environment using conda by running:
```
conda env create --file environment.yml
source activate ldsc
```
If you're using Windows, you may need to install [WSL](https://learn.microsoft.com/en-us/windows/wsl/install) before using conda because some of the packages require a unix-like OS. Because of this, it is recommended to use a Mac or linux OS to run this software.

Once the above has completed, you can run:

```
python ./ldsc.py -h
python ./munge_sumstats.py -h
```
to print a list of all command-line options. If these commands fail with an error, then something as gone wrong during the installation process. 

Short tutorials describing the four basic functions of `ldsc` (estimating LD Scores, h2 and partitioned h2, genetic correlation, the LD Score regression intercept) can be found in the wiki. If you would like to run the tests, please see the wiki.

## Updating LDSC

You can update to the newest version of `ldsc` using `git`. First, navigate to your `ldsc/` directory (e.g., `cd ldsc`), then run
```
git pull
```
If `ldsc` is up to date, you will see 
```
Already up-to-date.
```
otherwise, you will see `git` output similar to 
```
remote: Counting objects: 3, done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.
From https://github.com/bulik/ldsc
   95f4db3..a6a6b18  master     -> origin/master
Updating 95f4db3..a6a6b18
Fast-forward
 README.md | 15 +++++++++++++++
 1 file changed, 15 insertions(+)
 ```
which tells you which files were changed. If you have modified the `ldsc` source code, `git pull` may fail with an error such as `error: Your local changes to the following files would be overwritten by merge:`. 

In case the Python dependencies have changed, you can update the LDSC environment with

```
pip install .
```

## Where Can I Get LD Scores?
You can download ldsc input files from 1000G data [here](https://uwmadison.box.com/s/u5yqtacw7sev1aj97cxi1iyw9wrgk34v).

Alternatively, you can use these older links to download the data.
You can download [European](https://data.broadinstitute.org/alkesgroup/LDSCORE/eur_w_ld_chr.tar.bz2) and [East Asian LD Scores](https://data.broadinstitute.org/alkesgroup/LDSCORE/eas_ldscores.tar.bz2) from 1000 Genomes [here](https://data.broadinstitute.org/alkesgroup/LDSCORE/). These LD Scores are suitable for basic LD Score analyses (the LD Score regression intercept, heritability, genetic correlation, cross-sex genetic correlation). You can download partitioned LD Scores for partitioned heritability estimation [here](http://data.broadinstitute.org/alkesgroup/LDSCORE/).



## Citation

If you use the software or the LD Score regression intercept, please cite

[Bulik-Sullivan, et al. LD Score Regression Distinguishes Confounding from Polygenicity in Genome-Wide Association Studies.
Nature Genetics, 2015.](http://www.nature.com/ng/journal/vaop/ncurrent/full/ng.3211.html)

For genetic correlation, please also cite

[Bulik-Sullivan, B., et al. An Atlas of Genetic Correlations across Human Diseases and Traits. Nature Genetics, 2015.](https://www.nature.com/articles/ng.3406) Preprint available on bioRxiv doi: http://dx.doi.org/10.1101/014498

For partitioned heritability, please also cite

[Finucane, HK, et al. Partitioning heritability by functional annotation using genome-wide association summary statistics. Nature Genetics, 2015.](https://www.nature.com/articles/ng.3404) Preprint available on bioRxiv doi: http://dx.doi.org/10.1101/014241

For stratified heritability using continuous annotation, please also cite

[Gazal, S, et al. Linkage disequilibrium–dependent architecture of human complex traits shows action of negative selection. Nature Genetics, 2017.](https://www.nature.com/articles/ng.3954) 

If you find the fact that LD Score regression approximates HE regression to be conceptually useful, please cite

Bulik-Sullivan, Brendan. Relationship between LD Score and Haseman-Elston, bioRxiv doi: http://dx.doi.org/10.1101/018283

For LD Hub, please cite

[Zheng, et al. LD Hub: a centralized database and web interface to perform LD score regression that maximizes the potential of summary level GWAS data for SNP heritability and genetic correlation analysis. Bioinformatics (2016)](https://doi.org/10.1093/bioinformatics/btw613)


## License

This project is licensed under GNU GPL v3.


## Authors

Brendan Bulik-Sullivan (Broad Institute of MIT and Harvard)

Hilary Finucane (MIT Department of Mathematics)
