# matrisome-analyzer (v1_2016)

This script analyzes proteomic datasets for ECM content according to matrisome divisions and categories proposed by Naba and collaborators <a href="https://www.mcponline.org/article/S1535-9476(20)30479-5/fulltext">Naba et al, Mol Cell Prot, 2012</a> and calculates for components of the "matrisome": the peptide abundance, the number of spectra and number of unique peptides.

Input file requirements:

    The input file should be a comma separated value file (.csv).
    Input file should include, for each protein entry, annotations for matrisome divisions and categories. To annotate datasets with matrisome divisions  and category, use Matrisome Annotator.
    The following columns are mandatory:
        Matrisome divisions (header: "Division")
        Matrisome categories (header: "Category")
        For each sample and each protein entry: the total intensity of peptide abundance (header: " SampleName_PeptideAbundance", number of spectra (header: " SampleName_Spectra") and number of unique peptides (header: "SampleName_UniquePeptides").
    Note that "_" cannot be used in headers of columns other than the ones containing above-mentioned experimental data.


Output file:

   The output data folder is assigned a given number and, if the input folder contained data for several samples, will contain one subfolder per sample. Each subfolder contains:
       - a series of four pie charts (.jpg) representing the distribution of core matrisome, matrisome-associated and other proteins in terms of peptide abundance, number of spectra,unique peptides, and proteins
       - a tab-delimited text files summarizing the count results per matrisome divisions
       - a tab-delimited text files summarizing the count results per matrisome categories
