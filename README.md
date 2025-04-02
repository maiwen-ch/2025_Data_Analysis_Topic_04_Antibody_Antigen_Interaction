# Topic 02: Thermostability data analysis for protein engineering

### *Project overview and guidelines*

-   [Introduction](#introduction)
-   [Objective](#objectives-and-work-plan)
-   [Description of datasets](#description-of-datasets)
-   [Literature review](#literature)
-   [How to structure your project](#how-to-structure-your-project)
    -   [Project proposal](#project-proposal)
    -   [Project](#project)

Supervisor
----------

_Prof. Dominik Niopek_  ([dominik.niopek@uni-heidelberg.de](mailto:dominik.niopek@uni-heidelberg.de))  
_Benedict Wolf_ ([b.wolf@stud.uni-heidelberg.de](mailto:b.wolf@stud.uni-heidelberg.de))   
_Jan Mathony_  ([jan.mathony@uni-heidelberg.de](mailto:jan.mathony@uni-heidelberg.de)) 

Tutor: 
_Enno Schäfer_ ([enno.schaefer@stud.uni-heidelberg.de](mailto:enno.schaefer@stud.uni-heidelberg.de)) 


Introduction
------------
Proteins are active in certain temperature ranges. When heated above a certain threshold, proteins denature and become (ir-)reversibly inactive. The thermostability of proteins is hence a critical parameter for many applications that most scientists deal with every day, when working with restriction enzymes or DNA polymerases in molecular cloning. Recent high-throughput screenings enabled the unbiased investigation of the thermostabilities for several 10,000 proteins. The resulting datasets link the primary sequence of every protein to its specific thermostability.  
Such screenings allow us to better understand the determinants of protein folding and protein activity and could guide future protein engineering approaches. In this practical, you are going to explore a large-scale thermostability dataset with the aim to distill the information determining the thermal range in which proteins are active. Starting with a basic exploration of the datasets, you will extend your analysis towards more advanced data analysis techniques and machine learning models to gain a better understanding of protein stability. Finally, we will compare the results in between groups and relate them to other published datasets to identify differences or dataset-specific strengths and weaknesses.


Objectives and work plan
------------------------

You will work on a large-scale thermostability dataset encompassing the "meltomes" of several species, i.e. the melting temperature of each protein within their proteome. In short, you will get the amino acid sequences of the proteins and their respective melting temperatures as basis for your analysis. You will analyze the data focusing on various scientific question including the following:


- Gain an overview over the dataset. What inter- and intra-species patterns can you observe?
- Select one species and perform a broad analysis on its proteome
- Select proteins occurring in multiple species and compare their melting curves. Can you identify trends?
- What makes proteins gain a higher thermostabilty?
- Can you identify a subset of features that can help with the prediction of thermostability?

To exemplify the observations and effects in detail, each group can finally focus their analysis on the proteome of one species of their choice.

Description of datasets
-----------------------

### Thermostability Datatables
**cross-species.csv :**  
Dataset containing data as fold changes between different temperature thresholds for all species

**uniprot_mapping.txt :**  
Additional metadata on all available sequences including GO (gene ontology) Terms

**uniprot_sequences.fasta :**  
Amino acid sequences of all proteins in fasta format

### Download  

[Download Here!](https://heibox.uni-heidelberg.de/d/ad23ebb995a04b138ee9/)


Literature
----------

Two reviews with background information on the thermostability of proteins and thermostability profiling:
- Kumar et al. Factors enhancing protein thermostability. (2000). 10.1093/protein/13.3.179
- Mateus et al. Thermal proteome profiling: unbiased assessment of protein state through heat-induced stability changes. (2016). 10.1186/s12953-017-0122-4.

Key publications referring to the two datasets that you will be using:
- Jarzab et al., Meltome atlas - thermal proteome stability across the tree of life. (2020). 10.1038/s41592-020-0801-4
- Leuenberger et al., Cell-wide analysis of protein thermal unfolding reveals determinants of thermostability. (2017). 10.1126/science.aai7825.

A preprint, describing an advanced machine learning approach, using one of the datasets for thermostability prediction:
- Chu et al. Protein Stability Prediction by Fine-tuning a Protein Language Model on a Mega-scale Dataset. (2023). 10.1101/2023.11.19.567747.



How to structure your project
-----------------------------

### Project proposal

You first task will be to define a **project proposal**, which should
include

-   summary of literature on this dataset
-   questions you want to address
-   approximate timetable

You will present this project proposal together with a literature review
on the subject 3 week after the beginning of the semester (10 minute
presentation + 5 minutes discussion).

### Project

You project should contain the following elements:
- **descriptive statistics** about the datasets
- **graphical representations**
- **dimension reduction** analysis (PCA, clustering or k-means)
- **statistical tests** (t-test, proportion tests etc)
- **linear regression** analysis, either uni- or multivariate _(this point is optional!)_

#### Data cleanup

You will be analyzing multiple data sets together. It is
essential that you explore each dataset and clean it. Cleaning can refer
to many things:

-   Removing/Imputing missing values
-   Removing low variance columns/rows
-   Removing batch effects
-   Removing outlier samples (only if it is due to technical issues !!)
-   Making sure that data is in the correct format, for example, numbers
    should be encoded as numeric and not as characters. Categorical
    variables should be factors etc.
-   Re-ordering rows/columns in meaningful and useful ways

#### Data exploration

Now that you have cleaned data, explore your data to understand its
structure. Perform basic exploratory data analysis.

-   Look at the distribution of the overall data, specific samples or
    features.
-   Als consider the experimental differences behind the datasets
-   Identify additional useful metadata that can be fetched from public databases
-   Visualize the data distribution
-   Visualize the inter-dependencies (e.g. correlations) among specific samples/features of
    interest
-   Check some of your hypothesis like - is something high/low between
    two conditions etc

#### Data reduction

You have a high dimension matrix, that is, you have way more features
 than observations.

-   Try out methods to reduce the dimensionality of this data.
-   Cluster your samples to identify similar and dis-similar groups
-   Check how well the groups separate based on the features of your
    interest

#### Data modelling

Use linear regression to evaluate the relation between variables and predicting one using others.
