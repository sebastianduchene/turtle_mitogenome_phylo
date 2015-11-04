# Turtle mitogenomes

## Project 1.

   - Clockstar and Among-lineage rate variation

     - Partition mitogenomes by individual genes 
     
     - Estimate ML tree toplogy

     - Estimate global branch lengths

     - Calculate branch-wise dN/dS

     - Use [ClockstaR](http://bioinformatics.oxfordjournals.org/content/30/7/1017) to find clusters of genes. Is there a biological patter. For example, do genes such as COI, COII cluster together, and away from ATP's?

     - Use singular value decomposition (i.e. PCA) on the branch length distances to determine whether there is a particular branch responsible for the clustering. For example, if the branch leading to D. coriacea is responsible for 90% of the variance, then mitogenome-wide selective constraints have been most variable across genes for this lineage. This is closely in line with [this](http://bioinformatics.oxfordjournals.org/content/31/13/2061.abstract) paper.

     - This project only requires maximum likelihood analyses using paml or codonphyml, and clustering using some of my R or python code.


## Project 2.

   - Model adequacy and data sufficiency in mitogenome molecular clocks.

     - Partition mitogenomes by individual genes.

     - Analyse in mcmctree using a separate clock model for each gene, and the clock-partitioning scheme from ClockstaR.

     - Make infinite sites plot, which consists in a scatter plot of the uncertainty in tmrca estiamtes vs. the mean tmrca. The estimates are as precise as possible, given the calibrations, if the points fall along a straight line. This is a measure of whether the estimates can be made more precise by adding sequence data. Following the infinite sites theory from (http://mbe.oxfordjournals.org/content/23/1/212.full).

     - Mitogenome data might be sufficient to obtain an infinite sites pattern, but this might be improved by removing genes that inadequactely described by substitution and clock models. This is addressed by using model adequacy methods, described in [here](http://mbe.oxfordjournals.org/content/early/2015/10/19/molbev.msv207) and [here](http://mbe.oxfordjournals.org/content/32/11/2986).

     - The two analyses above (partition-by-gene and partitin-by-clockstar clusters molecular clocks) are repeated for strictly adequate genes. The infinte sites plot for these data might look more straight, implying that the data are more informative (with respect to the models). Alternative, line might look flatter, such that credible intervals around the tmrcas are narrower. The latter implies that using adequate genes does not lead to more 'informative' data, but that it reduces stochastic error.

     - This project involves running mcmctree four times, which is not too intensive. The potential delay is in conducting the model adequacy analyses, which typically require separate MrBayes and Beast runs for each gene.
