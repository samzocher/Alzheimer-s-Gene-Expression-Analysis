# Alzheimer-s-Gene-Expression-Analysis
This project utilized genetic data from an Alzheimer's Disease Study (Blalock et al 2011). I compared differentially expressed genes in subjects with incipient Alzheimer's Disease (AD) to subjects with moderate AD. Additionally, moderate AD vs severe AD was investigated. 

# Purpose of Analysis
The purpose of this analysis is to explore disease progression of AD at the genetic level. We can investigate the genes that significantly change in expression at each stage of the disease process. Additionally, after running an enrichR analysis, we can investigate biological processes that may be affected as AD progresses. 

## Citation
This data came from a study conducted in 2011 with the following citation:
Blalock EM, Buechel HM, Popovic J, Geddes JW et al. Microarray analyses of laser-captured hippocampus reveal distinct gray and white matter signatures associated with incipient Alzheimer's disease. J Chem Neuroanat 2011 Oct;42(2):118-26. PMID: 21756998

### Step 1
The first step in this analysis was to load the genetic and clinical data into the R environment. It is important to ensure the clinical data has 1 row per patient and the genetic data has rows that are features and columns that are patients. 

### Step 2
Now we can connect the two data frames using the Biospecimen ID. We can also filter the data to only include the groups I am comparing in part 1: moderate group vs the incipient group. 

### Step 3
Separate the data into baseline group and comparison group data frames. 

### Step 4
Run the t-test to see if the gene expression is different between the baseline and comparison groups. 

### Step 5
Next, sort by p-value and filter to only include genes where p-value < 0.01. 

### Step 6 
Repeat for the other groups (baseline of moderate AD and comparison of severe AD)

### Step 7 
Run enrichR analysis by first loading our short-listed t-test results. After cleaning the data, we can load each database we want to reference. Finally, we can run the enrichment function for each database. This will generate an excel file with 1 tab for each database. It will include fold change value, biological pathway information, and the differentially expressed genes that are in that pathway. 
