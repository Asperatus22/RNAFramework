# rf-index

The RF Index tool is designed to automatically generate a Bowtie reference index, that will be used by the RT Count module for reads mapping.<br />
To list the required parameters, simply type:

```bash
$ rf-index -h
```

Parameter         | Description
----------------: | :------------
__-o__ *or* __--output-dir__ | Bowtie index output directory (Default: &lt;assembly&gt;\_&lt;annotation&gt;, e.g. “mm9_refFlat/”)
__-ow__ *or* __--overwrite__ | Overwrites the output directory if already exists
__-g__ *or* __--genome-assembly__ | Genome assembly for the species of interest (Default: __mm9__).<br /> For a complete list of UCSC available assemblies, please refer to the UCSC website (<https://genome.ucsc.edu/FAQ/FAQreleases.html>)
__-a__ *or* __-annotation__ | Name of the UCSC table containing the genes annotation (Default: __refFlat__).<br />For a complete list of tables available for the chosen assembly, please refer to the UCSC website (<https://genome.ucsc.edu/cgi-bin/hgTables>)
__-n__ *or* __--gene-name__ | When possible, gene names will be used instead of gene IDs/accessions
__-t__ *or* __--timeout__ | Connection’s timeout in seconds (Default: __180__)
__-r__ *or* __--reference__ | Path to a FASTA file containing chromosome (or scaffold) sequences for the chosen genome assembly. !!! note "Note": if no file is specified, RSF Index will try to obtain sequences from the UCSC DAS server. This process may take up to hours, depending on your connection's speed.