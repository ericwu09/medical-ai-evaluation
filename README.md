# Medical AI Evaluation

Code for "How medical AI devices are evaluated: limitations and recommendations from an analysis of FDA approvals, Eric Wu, Kevin Wu, Roxana Daneshjou, David Ouyang, Daniel E. Ho, James Zou".



## Database - Contains notebooks and files for generating the full medical AI database.

We provide a comprehensive database of medical AI devices currently approved by the FDA.

### Features included

  - Approval number
  - Device name
  - Classification product code
  - Date received
  - Decision date
  - Indications for use
  - Body area
  - Modality
  - Predicate numbers
  - Sample size
  - Number of evaluation sites
  - Inclusion/Exclusion Criteria
  - Demographic information included
  - Prospective study
  - Disease subtype analysis
  - Device significance
  - Device severity
  - Device risk level
  - Matched keywords
  - Summary link
  
database/

1. Download FDA data.ipynb

  Most up-to-date approvals are from:
  - raw_files/pmn96cur.txt
    http://www.accessdata.fda.gov/premarket/ftparea/pmn96cur.zip
  - raw_files/pma.txt
  http://www.accessdata.fda.gov/premarket/ftparea/pma.zip
  
2. Filter AI submissions.ipynb

  Device are manually filtered after this as described in the paper.
  
3. Extract metadata.ipynb

  Extracts information available on the FDA html summary page for each device.
  
3. Parse study features.ipynb

  An example is provided for extracting the risk level. Other keywords for extracting features can be similarly performed as well.
  
Figure 2.ipynb and Supp Figure 2.ipynb

  Code used to produce the values in Figure 2 and Supp Figure 2.

    
## Case Study - Contains notebooks and files for reproducing the case study results presented in the paper for pneumothorax detection.

case_study/

- The four notebooks reproduce the results presented in the tables in the paper.

- Unfortunately, data sharing restrictions on the three datasets prevent us from being able to directly share the dataframes used. However, we share the code used to generate the train/valid/test splits, and provide identifiers for the splits created.

- Our internal abbreviations for the datasets are:

    CXP -> SHC (Stanford Health Care Hospital)
    CXR -> BIDMC (Beth Israel Deaconess Medical Center)
    NIH -> NIH (National Institute of Health)
