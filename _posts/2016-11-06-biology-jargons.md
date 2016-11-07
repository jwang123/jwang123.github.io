---
layout: post
title: Biology jargons
---

#Bio-Jargon

After reading my fair share of biology papers for the past three years, I've come to realize that, like most fields, biology is full of jargons. However, unlike quantitive fields such as math and physics, biology papers are usually written in a more accessible manner. Equipped with a thorough understanding of some common jargons, I believe most undergraduate science student can fully comprehend biological research papers. So after three years, I've decided to compile my own list and explanation so other students are not so easily dissuaded from pursuing a thorough understanding of any paper they encounter.

The list will be divided into multiple categories based on my own opinion of where they are most relevant. (Note: this is a work in progress, all explanations are subject to change)

### Genetics
- **GAL4**: a tool used to study gene expression
    - a transcriptional activator from budding yeast
    - part of the popular GAL4/UAS binary expression system: one transgenic construct drives the expression of the GAL4 and another construct contains its binding site positioned upstream of a responder gene
    - depending on the **driver** (native promoter driving GAL4), the responder gene can be made to express in specific cells
    - **GAL4 lines**: these are genetic varieties of a model organism where GAL4 is only expressed in some subset of the animal's tissues.
        - some lines are highly specific, perhaps only in a few cells
        - the presence of GAL4 is assumed to have little to no effect since most cells do not have UAS regions
    - **reporter lines**: second part of the system, they are strains with special UAS region next to a desired gene. Since the gene is only expressed in cells that express GAL4, they are *reporting* which cell express GAL4
    - **GAL80**: a GAL4 inhibitor that can be used to create GAL4 expression in cells that are in line A but not line B (by having GAL80 expressed in line B)
- **Genetic screen**:
- **fictive motor pattern**: neuronal activity in the absence of muscle feedback
- **GRASP**: a method for mapping synapses using two fragments of a GFP protein. GFP is attached to CD4 ligand, and if two neurons are close enough for synapse to form, GFP would be reconstituted and can be viewed under a fluorescent microscopew to

What does the letters and numbers of a transgenic strain mean?

- GMRgal4>UAS-XYZ
    - *GMR* represents the promoter sequence driving the expression of GAL4. This corresponds where the protein will be expressed in a multi-cellular organism
    - *gal4>UAS* represents the expression system being used
    - *XYZ* is the protein of interest that it ultimately being expressed
