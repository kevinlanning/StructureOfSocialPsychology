# Structure Of Social Psychology
### status as of 12/1/15: Please see SocialPsychStructure1215.pdf (submitted for pub: comments welcome)


## Overview
In this project I am examining the structure of scholarship in social/personality psychology by using network analyses, analyses of community structure, and differential text analysis on 354 papers which were published in 2014 in the top four journals in social/personality psychology.  A  citation network was first formed based upon the 22945 references cited in the source papers.    This was then reduced to a structural network, consisting only of the source papers, with links between these sources based on the number of shared references.  A complex community structure was then articulated which included five large overlapping communities and 21 smaller ones. Finally, I treated the text of these different communities as distinct corpora and used text analysis to find differences between these communities.

## Introduction
Concepts include (a) science as a social endeavor, (b) the need for an empirical (rather than keyword-driven) structure, (c) the overlapping nature of scholarly communities.

## Data preparation
The data consisted of the citations and text for  354 papers published in JPSP, PSPB, PSPR, and SPPS in 2014. The total number of cited references in these papers was 22945.  

## Features of the (two-mode) citation network
This citation network consists of a single giant component, but is sparse.  Although the citation network is itself not of central interest here, several features warrant mention, in particular:

	* Papers by Stapel, Smeesters, and Sanna appear to have little effect on the network.
	* The most cited papers are largely methodological 

## Features of the (one-mode) structural network.
In this single-mode network, consisting of all *JPSP, SPPS, PSPB,* and *PSPR* papers published in 2014, all 354 papers are connected, with papers connected to an average of 49 other papers, and pairs of papers sharing as many as 34 references in common.  The average distance between any two papers is less than 2, and the largest distance between any two papers is only 5.

Attempts to reduce the network into discrete communities achieved only modest success, as the number of communities extracted ranged from 7 to 10 in 10 separate analyses.  This lack of robustness does not reflect limitations of the dataset or of the methods, but the underlying structure of scholarship.  That is, any attempt to partitition the surface into discrete classes of social psychological scholarship will be arbitrary or trivial, as the underlying structure is fuzzy, manifest in overlapping groups.  

## Uncovering communities of scholarship.
In order to explore this complex structure, I used the clique percolation method (CPM), as instantiated in the open source software Cfinder. One key advantage to the approach is that it allows for overlap between communities.  I explored multiple solutions to community structure by manipulating two parameters, the minimum weight (w) of links between papers,and the minimum clique size (k). One of these models, with (w = 2, k = 3) is partially illustrated below.

## Identification of communities using text analysis. 
Finally, in order to identify, in a non-arbitrary way, the content of these communities, I undertook a differential text analysis, in which each community is identified by the words which differentiate it from the baseline of word use in all of the terms in the sample.  Words are only retained for this analysis if they appear in at least k different papers in the community.

In the illustration below, the results of this text analysis are superimposed upon the analysis of community structure.

![](http://i.imgur.com/WmHQeJL.png)


*The five largest communities of scholarship in social psychology in 2014.* Size of word cloud corresponds to number of papers in community. Width of links corresponds to number of papers shared by communities. Within communities, size of words indicates the salience of the term in distinguishing the community from the text of all papers in the sample.
