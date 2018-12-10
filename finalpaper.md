# Precision Medicine 
*Jasmine Lai, A12724439*

1. [Introduction](#1)
2. [Asthma](#2)<br>
3. [Precision Medicine in Asthma](#3)<br>
    3.1. [Phenotypic Classification](#31)<br>
    3.2. [Classification through Differential Gene Expression Analysis](#32)
4. [Other Precision Medicine Examples](#4)


## 1. Introduction<a name="1"></a>

Precision Medicine defines a new medical model; one that utilizes factors such as an individual's environment as well as their genetic makeup in order to determine medical decisions, practices, interventions, and products. It recognizes that a disease may be characterized by a similar set of symptoms - yet the mechanisms behind those symptoms may differ from person to person. 

Here is a brief introductory video about the concept of Precision Medicine [1]:
<p align="center">
    <a href="https://www.youtube.com/watch?v=HQKFgfMO5Sw">
        <img src="https://img.youtube.com/vi/HQKFgfMO5Sw/0.jpg" alt="What is Precision Medicine?"/>
    </a>
</p>
<br>

The characteristics of an individual that are important to Precision Medicine can be grouped into two categories.<br>

**Genetics**
> The genome sequence includes variations and mutations. The specific combination of these variations in an individual can lead to differences in the way a biological process occurs. For example, if a person has a mutation in a gene for a protein in a certain pathway, the pathway may not function properly and may lead to a disease.

**Environment**
> Environmental factors, especially UV exposure and smoking cigarettes, may lead to mutations in the genome. The epigenome, which affects the expression of genes, is shaped by an individual's environment and also varies across individuals.

## 2. Asthma<a name="2"></a>

Asthma is an allergic condition that affects the lungs, and is characterized by intermittent symptoms such as coughing, wheezing, and chest tightness [2]. In a normal lung, the muscles in the airway are smooth and relaxed. However, in an asthmatic subject, the muscles are tightened, swollened, or inflamed, leading to an increased production of mucus and obstruction of the airway. 

<p align="center">
    <img src="/figure2.png" width="400" height="302"/>
</p>
<p align="center">
    <a href="https://www.webmd.com/asthma/ss/slideshow-asthma-overview">Source</a>.
</p>
<br>


Studying asthma from a Precision Medicine lens is particularly important because researchers have contended that the disease is heterogeneous, with different underlying mechanisms and outcomes, and is largely affected by environmental variables [2]. With an estimated 300 million people that suffer from asthma, it is important to understand the differences between smaller subgroups of the disease, and treat individuals accordingly.

## 3. Precision Medicine in Asthma<a name="3"></a>
### 1) Phenotype Classification<a name="31"></a>

The first application we are going to explore is separating asthma subjects into groups based on phenotype.
<p align="center">
    <img src="/figure1.png" width="400" height="435"/>
</p>
<br>

>[Figure 1](https://insights.ovid.com/pubmed?pmid=29045293). Clinical phenotypes of moderate–severe asthma derived from U-BIOPRED cohort from a cluster analysis of eight clinico-physiologic parameters. **Figure by Kian Fan Chung. Current Opinion in Pulmonary Medicine (2018).**

Here, we see that subjects were divided into four subgroups based on factors such as age, severity, smoker/non-smoker, number of exacerbations, etc. This model shows how researchers can begin to find treatments for smaller groups that fall under a larger umbrella disease. The hope is that a more tailored approach for each subgroup will be more effective than a generic treatment for all the groups combined. 

### 2) Classification through Differential Gene Expression Analysis<a name="32"></a>

Beyond just looking at phenotype, we can go a step further by using Bioinformatic techniques such as RNA-seq. 

In a paper by Seumois et al. in The Journal of Immunology (2016), they aim to determine differentially expressed genes between asthma and rhinitis. 

#### Background

The two diseases studied, asthma and rhinitis, were chosen because they are both chronic allergic diseases, and they both involve a pathway that produces Th2 cells [4]. Because the underlying mechanism of two conditions are similar, the goal of the paper is to utilize RNA-seq methods to find what differences in gene expression separate the two diseases. For analysis, they performed negative binomial tests for pairwise comparisons employing the Bioconductor package DESeq2 to identify individual differentially expressed genes.

#### RNA Sequencing Procedure

The RNAseq procedure in this paper was the following:
1. RNA Purification/Quantification (Qiagen,USA)
2. RNA Amplification
3. cDNA library preparation (Nextera XT, Illumina)
4. Single end Sequencing (HiSeq2500 Illumina)
5. Remove poor quality samples
6. Generate Illumina sequencing libraries
7. Map reads to reference

#### Results

A Weighted gene co-expression network analysis (WGCNA) identified a total of 15 distinct gene modules in Th2 cells. Between the asthmatic and healthy groups, two modules were up-regulated and three down-regulated in asthma.

DESeq analysis found 500 genes differentially expressed between asthmatic subjects and healthy subjects The genes found are known to be for apoptosis, zinc transporters, MAPK, NF-κB, TNF, and others.

<p align="center">
    <img src="/figure3.png" width="600" height="595"/>
</p>
<br>

>[Figure 2](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4936908/). A, Weighted gene co-expression network analysis (WGCNA) showing gene modules identified in Th2 cells. B, List of identified modules ordered by their t statistics. C, DESeq2 analysis showing pairwise comparison of gene expression between Th2 cells from healthy, rhinitis and asthmatic subjects. **Figure by Seumois et al. The Journal of Immunology (2016).**

#### Summary 

To address the question of how asthma and rhinitis differ, the paper found that genes that differentiate asthmatic from healthy subjects show an intermediate phenotype in allergic rhinitis subjects. Studies like these generate useful data that can be further used to study how subtypes of disease should be treated, and can be used to learn about the underlying mechanisms of disease.

## 4. Other Precision Medicine Examples<a name="4"></a>
- [Breast Cancer](http://theoncologist.alphamedpress.org/content/14/4/320.short)
- [Rheumatoid Arthritis](https://www.ncbi.nlm.nih.gov/pubmed/24589910)
- [Diabetes](https://www.ncbi.nlm.nih.gov/pubmed/26802434)
- [Alzheimer's](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4828743/)

# Reference
[1] (UCSF), UC San Francisco, director. What Is Precision Medicine? YouTube, YouTube, 2 Dec. 2015, www.youtube.com/watch?v=HQKFgfMO5Sw.<br>

[2] Chung, Kian Fan. “Precision Medicine in Asthma.” Current Opinion in Pulmonary Medicine, vol. 24, no. 1, 1 Jan. 2018, pp. 4–10., doi:10.1097/mcp.0000000000000434.<br>

[3] Pillai, Regina A., and William J. Calhoun. “Introduction to Asthma and Phenotyping.” Heterogeneity in Asthma Advances in Experimental Medicine and Biology, 2013, pp. 5–15., doi:10.1007/978-1-4614-8603-9_1. <br>

[4] Seumois, Grégory et al. “Transcriptional Profiling of Th2 Cells Identifies Pathogenic Features Associated with Asthma” Journal of immunology (Baltimore, Md. : 1950) vol. 197,2 (2016): 655-64.<br>
