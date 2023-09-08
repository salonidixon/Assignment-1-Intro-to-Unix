# Assignment-1-Intro-to-Unix
## Name: Saloni Dixon 
## Programming Language: Unix
## Date: 09/07/23 
### Description 
For this assignment, a shell script was created in order to independently perform a series of tasks for the purpose of the familiarity of handling biological sequence data, competency using basic Unix commands and shell scripting, and appropriately managing a Git repository. This was completed utilizing scripts from multiple different languages, namely Unix. 

### Required Files: 

ssh [username]@[hostname] enables secure access to log in to remote systems

### Required Packages: 
There are no specific packages required for this repository. 

### Execution: 
1. Opened the Cygwin Terminal and securely logged on. 
`$ ssh saldixon@quartz.uits.iu.edu`

2. Created a directory, labeling it "Informatics_573" and navigated to the given path. 
`$mkdir Informatics_573` 
`$cd Informatics_573` 

3. Downloaded all secondary assemblies for human chromosome 1 from University of California, Santa Cruz (UCSC) Genome browser (all chromosome 1 assemblies except “chr1.fa.gz”) AND unzipped all of the downloaded chromosome 1 assemblies. 
`wget https://hgdownload.soe.ucsc.edu/goldenPath/hg38/chromosomes/chr1_GL383518v1_alt.fa.gz
wget https://hgdownload.soe.ucsc.edu/goldenPath/hg38/chromosomes/chr1_GL383519v1_alt.fa.gz
wget https://hgdownload.soe.ucsc.edu/goldenPath/hg38/chromosomes/chr1_GL383520v2_alt.fa.gz
wget https://hgdownload.soe.ucsc.edu/goldenPath/hg38/chromosomes/chr1_KI270706v1_random.fa.gz
wget https://hgdownload.soe.ucsc.edu/goldenPath/hg38/chromosomes/chr1_KI270707v1_random.fa.gz
wget https://hgdownload.soe.ucsc.edu/goldenPath/hg38/chromosomes/chr1_KI270708v1_random.fa.gz
wget https://hgdownload.soe.ucsc.edu/goldenPath/hg38/chromosomes/chr1_KI270709v1_random.fa.gz
wget https://hgdownload.soe.ucsc.edu/goldenPath/hg38/chromosomes/chr1_KI270710v1_random.fa.gz
wget https://hgdownload.soe.ucsc.edu/goldenPath/hg38/chromosomes/chr1_KI270711v1_random.fa.gz
wget https://hgdownload.soe.ucsc.edu/goldenPath/hg38/chromosomes/chr1_KI270712v1_random.fa.gz
wget https://hgdownload.soe.ucsc.edu/goldenPath/hg38/chromosomes/chr1_KI270713v1_random.fa.gz
wget https://hgdownload.soe.ucsc.edu/goldenPath/hg38/chromosomes/chr1_KI270714v1_random.fa.gz
wget https://hgdownload.soe.ucsc.edu/goldenPath/hg38/chromosomes/chr1_KI270759v1_alt.fa.gz
wget https://hgdownload.soe.ucsc.edu/goldenPath/hg38/chromosomes/chr1_KI270760v1_alt.fa.gz
wget https://hgdownload.soe.ucsc.edu/goldenPath/hg38/chromosomes/chr1_KI270761v1_alt.fa.gz
wget https://hgdownload.soe.ucsc.edu/goldenPath/hg38/chromosomes/chr1_KI270762v1_alt.fa.gz
wget https://hgdownload.soe.ucsc.edu/goldenPath/hg38/chromosomes/chr1_KI270763v1_alt.fa.gz
wget https://hgdownload.soe.ucsc.edu/goldenPath/hg38/chromosomes/chr1_KI270764v1_alt.fa.gz
wget https://hgdownload.soe.ucsc.edu/goldenPath/hg38/chromosomes/chr1_KI270765v1_alt.fa.gz
wget https://hgdownload.soe.ucsc.edu/goldenPath/hg38/chromosomes/chr1_KI270766v1_alt.fa.gz
wget https://hgdownload.soe.ucsc.edu/goldenPath/hg38/chromosomes/chr1_KI270892v1_alt.fa.gz`

5. Created a new empty file called "data_summary.txt"
`$ touch data_summary.txt`

6. Appended  a list of the all detailed information (including file name, size, and permissions) to “data_summary.txt”
`$ stat --format="Name: %n        Size: %s                Permissions: %A" *.fa > data_summary.txt`

7. Appended the first 10 lines of each of the chromosome 1 assemblies to "data_summary.txt"
`$ head chr1_GL383519v1_alt.fa chr1_KI270708v1_random.fa chr1_KI270712v1_random.fa chr1_KI270760v1_alt.fa chr1_KI270764v1_alt.fa chr1_GL383520v2_alt.fa chr1_KI270709v1_random.fa chr1_KI270713v1_random.fa chr1_KI270761v1_alt.fa chr1_KI270765v1_alt.fachr1_KI270706v1_random.fa chr1_KI270710v1_random.fa chr1_KI270714v1_random.fa chr1_KI270762v1_alt.fa chr1_KI270766v1_alt.fa >> data_summary.txt`

8. Appended the name of assembly and total number of lines included in that assembly to "data_summary.txt"
`$ wc -l chr1_GL383519v1_alt.fa chr1_KI270708v1_random.fa chr1_KI270712v1_random.fa chr1_KI270760v1_alt.fa chr1_KI270764v1_alt.fa chr1_GL383520v2_alt.fa chr1_KI270709v1_random.fa chr1_KI270713v1_random.fa chr1_KI270761v1_alt.fa chr1_KI270765v1_alt.fa chr1_KI270706v1_random.fa chr1_KI270710v1_random.fa chr1_KI270714v1_random.fa chr1_KI270762v1_alt.fa chr1_KI270766v1_alt.fa >> data_summary.txt`
