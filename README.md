
The PiRATE paper is online on BMC Genomics :

https://doi.org/10.1186/s12864-018-4763-1

***
![](http://www.seanoe.org/data/00406/51795/thumbnail.gif)

***Where to download the PiRATE VM (Virtual Machine)?***

Pirate-Galaxy is installed on a Virtual Machine:

The PiRATE Virtual Machine can not be download on Github but on SEANOE (Sea scientific open data publication): 

http://doi.org/10.17882/51795

You have to download the Virtual Machine (17 Go) and to run it on your local computer with a software such as VirtualBox (Virtual Machine Monitor) , it works on Linux, Windows, MacOS :

https://www.virtualbox.org/

The PiRATE tutorial is available here:

http://archimer.ifremer.fr/doc/00412/52373/


***

***What is PiRATE-Galaxy?*** 

PiRATE-Galaxy is a web-based platform which integrates bioinformatic tools dedicated to transposable elements analayses.

Thoses tools are automated into a stand alone Galaxy https://galaxyproject.org/use/pirate/ and installed in a Linux Virtual Machine (Fig. 1) (download link below).

PiRATE-Galaxy combines 14 tools allowing the detection, classification and annotation of Transposable Elements from a genome assembly and/or short reads sequencing data (e.i. Illumina) (Fig. 1).

You can use all tools in order to performed the full PiRATE pipeline workflow, or use only some tools regarding to your available input data, or your goals.

Keep in mind that the full PiRATE pipeline workflow (Fig. 2) is not "one-click" automated and that you will must run each tool one after one. For some steps, it is required to be perform manual curation (e.i. TE library curation).

***

**Fig. 1: Galaxy-PiRATE web-based platform overview**

![](https://github.com/JBerthelier/PiRATE/blob/master/pirate-galaxy.PNG?raw=true)

***

**Fig 2: Full PiRATE pipeline workflow pipeline overview** 

![](https://github.com/JBerthelier/PiRATE/blob/master/PiRATE_Pipeline_Figure.png?raw=true)

***

**STEP I) TE Detection**

**_Approach 1: Similarity-based_**

  - RepeatMasker www.repeatmasker.org/ (Smit et al. 1996)
  - TE-HMMER ( in PiRATE )

**_Approach 2: Structural-based_**

  - LTRharvest http://www.zbh.uni-hamburg.de/?id=206 (Ellinghaus et al., 2008)
  - MGEScan-nonLTR http://mgescan.readthedocs.io/en/latest/nonltr.html (Rho and Tang, 2009)
  -  Helsearch http://omictools.com/helsearch-tool (Yang and Bennetzen, 2009)
  -  MITE-Hunter http://target.iplantcollaborative.org/mite_hunter.html (Han and Wessler, 2010)
  -  SINEfinder http://www.plantcell.org/content/23/9/3117 (Wenke et al., 2011)

**_Approach 3: Repetitiveness-based_**

  - TEdenovo https://urgi.versailles.inra.fr/Tools/REPET (Flutre et al., 2011)
  - RepeatScout https://bix.ucsd.edu/repeatscout/ (Price et al., 2005)

**_Approach 4: Build repeated elements_**

  - RepeatExplorer http://repeatexplorer.umbr.cas.cz/ (Novak et al., 2013)
  - dnaPipeTE https://lbbe.univ-lyon1.fr/-dnaPipeTE-.html (Goubert et al., 2015)
  - RepARK https://github.com/PhKoch/RepARK (Koch et al., 2014)

 
**STEP II) TE Classification**

  - PASTEC https://urgi.versailles.inra.fr/Tools/PASTEClassifier (Hoede et al., 2014)

 
**STEP III) TE Annotation**

  - TEannot https://urgi.versailles.inra.fr/Tools/REPET (Flutre et al., 2011)

***

***What is the goal of PiRATE (Pipeline to Retrieve and Annotate Transposable Elements)?***

To date, genome assembly of non-model organisms is usually not at chromosomal level and are highly fragmented. This fragmentation is recognized to be, in part, the result of a bad assembly of the transposable elements (TEs) copies, increasing the difficulty to detect and annotate them.

In this context, we designed a new bioinformatics pipeline named PiRATE to detect, classify and annotate TEs of non-model organisms. We optimized its detection step by gathering every existing TE detection approaches. The goal is to promote the detection of complete TE sequences of every TE families. The detection of complete TE sequences, bearing recognizable conserved domains or specific motifs, allows to facilitate the classification step.

Each tools used by the PiRATE pipeline are automated into a stand-alone Galaxy. This PiRATE-Galaxy can be used through a Virtual Machine (PiRATE-VM).

**This PiRATE-Galaxy is a suitable and flexible platform to study TEs in the genome of every organisms.**

However, be aware that PiRATE has been designed for organisms that have relative small genome assembly, it has been created/controled using A. thaliana genome assembly (120Mb).
You need a powerful machine if you want to use it with a larger genome assembly and you have to properly setup the amount of rams/cores in the setting of virtualbox and in the virtual machine (Please check : https://github.com/JBerthelier/PiRATE/issues/29)

***

Projects that used PiRATE:

- Ichthyophis bannanicus (Amphibians) genome https://www.biorxiv.org/content/10.1101/2020.08.19.257527v1.abstract
- Almond and peach genomes https://onlinelibrary.wiley.com/doi/full/10.1111/tpj.14538
- Sugarcane mitochondrial genome https://peerj.com/articles/7558/?utm_source=TrendMD&utm_campaign=PeerJ_TrendMD_1&utm_medium=TrendMD
- Trypanosoma and Leishmania genome https://link.springer.com/article/10.1186/s13100-019-0175-2#Abs1
- Botrytis fabae (Fungus) genome https://www.frontiersin.org/articles/10.3389/fmicb.2020.00217/full
- Ascochyta rabiei (Fungus) genome https://www.g3journal.org/content/10/7/2131.abstract
- Bactrocera oleae (Insect) genome https://link.springer.com/content/pdf/10.1186/s12864-020-6672-3.pdf
- Helicoverpa armigera (Insect) https://www.mdpi.com/2075-4450/11/12/879
- Tisochrysis lutea genome (Microalgae) https://doi.org/10.1186/s12864-018-4763-1
- Turnera subulata genome (Plant)  https://doi.org/10.3390/plants12020286
- several Salamanders species  https://www.biorxiv.org/content/10.1101/2024.07.22.604708v1.full
