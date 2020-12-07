---
identifier: AboutOrthoMCL
listTitle: About OrthoMCL
descriptionTitle: About OrthoMCL
listIconKey: info
tags: [tutorial]
title: About OrthoMCL
permalink: '#AboutOrthoMCL'
category: [OrthoMCL]
---
<div style="margin: auto; max-width: 51em;">
<p>
            Orthologs are homologs separated by speciation events.  Paralogs are homologs separated
            by duplication events. Detection of orthologs is becoming much more important with the
            rapid progress in genome sequencing (<a href="https://academic.oup.com/mbe/article/36/10/2157/5523206" target="_blank">Glover et al. 2019</a>).<br>
         
<img style="width: 20em; margin-top: auto; margin-left: auto; float:right" src="{{ "/assets/images/resources_tools/aboutortho.png" | absolute_url }}" alt="cluster"/><br/>
        
            OrthoMCL is a genome-scale algorithm for grouping orthologous protein sequences. It
            provides not only groups shared by two or more species/genomes, but also groups
            representing species-specific gene expansion families. Thus, it serves as an important
            utility for automated eukaryotic genome annotation. <br><br>OrthoMCL starts with reciprocal best
            hits within each genome as potential in-paralog/recent paralog pairs and reciprocal best
            hits across any two genomes as potential ortholog pairs.  Related proteins are interlinked
            in a similarity graph. Then, MCL (Markov Clustering algorithm; <a href="https://dspace.library.uu.nl/handle/1874/848" target="_blank">Dongen 2000</a>;
            <a href="http://micans.org/mcl/" target="_blank">www.micans.org/mcl</a>) is invoked to split mega-clusters.
            This process is analogous to the manual review in COG construction.  MCL clustering is
            based on weights between each pair of proteins, so to correct for differences in
            evolutionary distance the weights are normalized before running MCL.
          
        <br><br>
            OrthoMCL is similar to the INPARANOID algorithm (<a href="https://www.sciencedirect.com/science/article/abs/pii/S0022283600951970?via%3Dihub" target="_blank">Remm et al. 2001</a>) but is extended to cluster orthologs from multiple species. OrthoMCL clusters are coherent with groups identified by EGO (<a href="https://genome.cshlp.org/content/12/3/493.long" target="_blank">Lee et al. 2002</a>), and an analysis using EC number suggests a
            high degree of reliability (<a href="http://www.genome.org/cgi/content/abstract/13/9/2178" target="_blank">Li et al. 2003</a>).
          </p>  
          </div>