# The benchmarking for callers of TAD hierarchy
## Description
We benchmarked 13 available callers detecting hierarchical TAD structures (TAD hierarchy) by evaluating the biological correlation, robustness, and usability of the callers. For biological correlation, we used deepTools to compare a series of biological features around TAD boundaries detected by various callers, including CTCF, SMC3, Dnase-seq, H3K4me3, H3K27ac, POLR2A, H3K9ac, H3K27me3, H3K9me3, number of promoters and coding sequence(CDS). For robustness, we developed a new metric———Hier_SSIM and an existing metric———Overlap Ratio to evaluate the similarity between TAD hierarchies from different caller. We counted the two metrics under different conditions as follows: (1) seven cell types of Hi-C dataset GSE63525; (2) five frequently-used data resolutions of 5Kb, 10Kb, 25Kb, 50Kb, and 100Kb; (3) the ICE-normalized data of 50Kb downsampled by 50% and 20%; (4) raw Hi-C matrix and ICE-normalized Hi-C matrix. For usability, we scored the usage of all callers from these aspects as following: software installation, assuarance of code instructions, complexity of the input format, difficulty of processing the outputs, time consuming,  built-in visualization, and resolution self-identification.


## implementation

In the `/callers`, we showed the implementation of all 13 TAD hierarchy callers on 50Kb raw Hi-C matrix of GM12878 as an example. Please make sure the installation of all callers following these versions: [Arrowhead (v1.0.0)](https://github.com/aidenlab/juicer/wiki/Arrowhead),[Armatus (v2.3)](http://www.cs.cmu.edu/~ckingsf/software/armatus/), [HiTAD (v0.4.2)](https://pypi.python.org/pypi/TADLib), [matryoshka (v1.0)](https://github.com/COMBINE-lab/matryoshka), [OnTAD (v1.2)](https://github.com/anlin00007/OnTAD.git), [TADpole (v0.0.09000)](https://github.com/3DGenomes/TADpole), 
[SpectralTAD (v1.2.0)](https://bioconductor.org/packages/SpectralTAD/), [GRiNCH (v1.0.0)](https://roy-lab.github.io/grinch/), [deDoc (v1.0.0)](https://github.com/yinxc/structural-information-minimisation), [SuperTAD (v1.2)](https://github.com/deepomicslab/SuperTAD), [TADtree (v1.0.0)](http://compbio.cs.brown.edu/projects/tadtree/), [GMAP (v1.4)](http://tanlab4generegulation.org/rGMAP_1.1.tar.gz), and [HiCKey (v1.0)]( https://github.com/YingruWuGit/HiCKey).

In the `/evaluation`, we implemented the Hier_SSIM of Fig.2b and the Overlap Ratio of Fig.4e. 
In the `/visualization`, we implemented the visualization of Fig.2c.

Each method contains a file including the README file, input files, output files and its implementation on example inputs.
