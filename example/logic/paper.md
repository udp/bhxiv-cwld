---
title: 'Mapping colloquial wet lab language to ontologies'
title_short: 'CWLD'
tags:
  - ontologies
authors:
  - name: David Markham
    orcid: 0000-0001-7765-369X
    affiliation: 1
  - name: James McLaughlin
    orcid: 0000-0002-8361-2795
    affiliation: 2
affiliations:
  - name: Newcastle University, Newcastle-upon-Tyne, UK
    index: 1
  - name: EMBL-EBI, Hinxton, Cambridge, UK
    index: 2
date: 12 November 2022
cito-bibliography: paper.bib
event: BioHackathon Europe 2022
biohackathon_name: "NBDC/DBCLS BioHackathon"
biohackathon_url:   "http://biohackathon-europe.org/"
biohackathon_location: "Paris, France, 2022"
group: Project 14
# URL to project git repo --- should contain the actual paper.md:
git_url: https://github.com/biohackrxiv/bhxiv-gen-pdf
# This is the short authors description that is used at the
# bottom of the generated paper (typically the first two authors):
authors_short: David Markham & James McLaughlin

---

<!--

The paper.md, bibtex and figure file can be found in this repo:

  https://github.com/journal-of-research-objects/Example-BioHackrXiv-Paper

To modify, please clone the repo. You can generate PDF of the paper by
pasting above link (or yours) in

  http://biohackrxiv.genenetwork.org/

-->

# Introduction

The use of ontology terms can make data more FAIR and tractable by machines. However, the highly formalised terminology used by these ontology terms does not always match the colloquial language used by practitioners. This disparity can (a) make it difficult for practitioners to understand the language used by knowledge stored in ontologies; and (b) make it difficult to machine-interpret information written by practitioners to map it to ontologies.

This problem is particularly relevant in the ELIXIR Microbial Biotechnology (MB) community, as although the domain has adopted ontologies and data standards such as SO, SBO, GO, and SBOL for data representation, the tools developed often use ontology terms directly rather than the language used in the wet lab (i.e. by the people using the tools.)

At the BioHackathon 2022 in Paris, France, we initiated an effort to address this problem by (a) mining the internet for colloquial language used by biologists, (b) constructing a dictionary of this language and its mappings to ontology terms, and (c) constructing a recommendation table of terminology for MB tool developers based on this data.

While initially developed to serve the MB community, we hope that the dictionary will serve as a helpful resource for anyone hoping to map from colloquial wet lab language to ontology terms for e.g. text mining applications.

# Using Stack Exchange to gather colloquial domain language

Replace below with word cloud png
![Most commonly used words on Biology Stack Exchange](./wordcloud.png)

# Creating a dictionary of colloquial wet lab terminology

An issue we encountered in making the dictionary available is that there is no standard/FAIR data format to publish string to term mappings. The SSSOM (Super Simple Standard for Ontology Mappings) supports term to term mappings, but not string to term. We have discussed with the SSSOM developers about implementing support for this, and are helping with a pull request to add it to the standard. We will then hopefully be able to publish the dictionary in the future using SSSOM.

# Terminology recommendations for Microbial Biotechnology tool developers
This list is non-exhaustive, but covers a selection of terms that we noticed differ between MB tools.

<!--
| Term                | MB tools/ontologies using this term | Frequency on Biology Stack Exchange |
|---------------------|-------------------------------------|-------------------------------------|
| Component           | SBOL, SBOLDesigner, SBOLCanvas      | 2163                                |
| Module              | SBOL                                | 311                                 |
| Device              |                                     | 677                                 |
| System              |                                     | 16098                               |
| RBS                 |                                     | 548                                 |
| Ribosome Entry Site | SO                                  | 8                                   |
| Upregulation        |                                     | 79                                  |
| Downregulation      |                                     | 91                                  |
-->

# Results

<!--
    State the problem you worked on
    Give the state-of-the art/plan
    Describe what you have done/results starting with The working group created...
    Write a conclusion
    Write up any future work

-->

The following tasks were accomplished as part of the BioHackathon:

- Initial Dictionary of Terms in CSV fomrat
- Analysis of commonly used words on Stack Exchange


# Availability

The dictionary is available in CSV format at 

# Future work

We have used the Stack Exchange dataset to analyse the popularity of a small set of terms used in MB which differ between different tools. The next step would be to apply this to entire ontologies, annotating every label and synonym in the ontology with its popularity. This information could then be used to inform whether the primary label of the term should be preferred, or whether a synonym should be preferred instead.

It would also be interesting to explore how the Stack Exchange datasets can be used to gather domain-specific language for different domains, using a similar approach subtracting “meta” terms and analysing the delta. There are 98 Stack Exchange sites at the time of writing.

We intend to publish the dictionary using SSSOM, once the ability to map strings to terms has been implemented.

## Acknowledgements

With thanks to the oranisers of BioHackathon Europe for
providing an excellent environment to inspire this work
and for funding the travel arrangements of the authors.

## References
