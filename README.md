**- /!\ Be carreful /!\ -**

There is a mistake in the instruction of the "TEannot" panel of PiRATE:

The requested size of the genome is not in Mb but in bp.

--> the correct instruction is : "Genome size (example: 85,000,000 pb)"

This will be corrected in PiRATE v2.


________________________________________________________

The PiRATE paper is online on BMC Genomics :

https://doi.org/10.1186/s12864-018-4763-1



***What is PiRATE (Pipeline to Retrieve and Annotate Transposable Elements) ?*** 


![](http://www.seanoe.org/data/00406/51795/thumbnail.gif)


To date, genome assembly of non-model organisms is usually not at chromosomal level and are highly fragmented. This fragmentation is recognized to be, in part, the result of a bad assembly of the transposable elements (TEs) copies, increasing the difficulty to detect and annotate them.

In this context, we designed a new bioinformatics pipeline named PiRATE to detect, classify and annotate TEs of non-model organisms. We optimized its detection step by gathering every existing TE detection approaches. The goal is to promote the detection of complete TE sequences of every TE families. The detection of complete TE sequences, bearing recognizable conserved domains or specific motifs, allows to facilitate the classification step. The classification step of PiRATE has been improved for algal genomes.

Each tools used by the PiRATE pipeline are automated into a stand-alone Galaxy. This PiRATE-Galaxy can be used through a Virtual Machine (PiRATE-VM).

**This PiRATE-Galaxy is a suitable and flexible platform to study TEs in the genome of every organisms.**

However, be aware that PiRATE have been mainly design for organisms that have relative small genome assembly, it has been created/controled using A. thaliana genome assembly (120Mb).
You need a powerful machine if you want to use it with larger genome assembly and you need to properly setup the amount of Rams/cores in the virtualbox and in the virtual machine. 
Please check : https://github.com/JBerthelier/PiRATE/issues/29 

The PiRATE Virtual Machine can not be download on Github but on SEANOE (Sea scientific open data publication): 

http://doi.org/10.17882/51795

You have to download the Virtual Machine and to run it with a Virtual Machine Monitor such as VirtualBox:

https://www.virtualbox.org/

The PiRATE tutorial is available here:

http://archimer.ifremer.fr/doc/00412/52373/

**PiRATE overview**

***

![](https://github.com/JBerthelier/PiRATE/blob/master/PiRATE_Pipeline_Figure.png?raw=true)

***

PiRATE integrates several tools that are automated in a Galaxy, however, you need to launch each tool one by one, and some steps need to be performed manually. 
PiRATE is compose of a detection, a classification and an annotation step. 
12 tools are availables for the detection step, you can use all or some of them, according to your need or your data. 

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
