# Get the data


## Structure

* :page_with_curl: **`dd_clinical_cyto_chr17.tsv`**: clinical dataframe in tab seperated text format.

Each row is a patient and each column a descriptor.

Details about descriptor are as follows:

	* LEUKID the unique ID of each patient/sample
	* SEX, AGE demographics
	* Mds type
	* WHO 2016 classification
	* Blood counts and Blast counts
	* Cytogenetics
	* IPSS-R risk category
	* NGS derived deletions, gains and regions copy-neutral loss of heterozygosity as a list of chr. arms
	* Annotation of complex karyotype
	* Status of chr.17 at the TP53 locus
	* Treatment status regarding HMA, Lenalidomid, HSCT
	* overall survival and AML transformation information


* :clipboard: **`dd_matrix_binary_cyto.tsv`**: binary matrix of chromosomal alterations per patient from the integration of conventional cytogenetics and NGS-derived copy-number analysis. The file is a tab seperated text file.

Each row is a patient and each column a given chromosomal alteration, eg. del5q, del7 ....
Each entry is binary.

* :bar_chart: **`maf_TP53.tsv`**: TP53 mutation file.

Each row corresponds to a given mutation in a given patient.

Details about mutation fields  are as follows:

	* TARGET_NAME the unique ID of each patient/sample
	* CHR START END variant.key for the genomic position of the mutation
	* GENE 
	* cDNA_CHANGE
	* PROTEIN_CHANGE 
	* VT variant type (substitution, indels)
	* EFFECT classification of mutation consequence, ie missense nonsense frameshift ...
	* VAF DEPTH variant allele frequency and coverage depth


* :dancers: **`dd_comutation.tsv`**: matrix of co-mutations of TP53-mutant samples.

Each row corresponds to a patient and each column to a gene.

Each numbers indicate the number of driver mutations in a given gene.

The unique ID can be found in the LEUKID column.


In addition, we also provide here the SNP included in the custom capture bait design:


* :dart: **`snps_on_bait_design.txt`**: SNP included in the bait design of the study with hg19 genomic position.
