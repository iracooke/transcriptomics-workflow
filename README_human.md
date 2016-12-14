# Transcriptomics Workflow

Instructions to take raw transcriptomics reads and progress to a counts file that can be used in `R` packages for statistical analysis of differential expression.

To follow this tutorial you will need to have some basic familiarity with working in a unix-like environment.  An excellent place to start would be to attend a [software carpentry](http://software-carpentry.org/) or [data carpentry](http://www.datacarpentry.org/) workshop, or complete the [Unix bootcamp](
http://rik.smith-unna.com/command_line_bootcamp/?id=9xnbkx6eaof).  The VLSCI also have several tutorials for [working with unix and/or a HPC environment](http://vlsci.github.io/lscc_docs/tutorials/)

## Connect to analysis server
This will usually mean opening a terminal and using `ssh` to connect. The general format of this command is;

```bash
	ssh username@my.hpc.server.edu.au
```

## Downloading the human genome
This step will be important when using the HISAT program to align the RNAseq reads onto the genome. This step will use the `wget` command, which allows the user to download particular files from the web. The general format of this command is:

	```bash
		wget http://website.come/files
	```
To download a version of the *human genome* with HiSat2 indexes, enter the following command into the terminal on HPC

	```bash
		wget ftp://ftp.ccb.jhu.edu/pub/infphilo/hisat2/data/grch38.tar.gz
	```