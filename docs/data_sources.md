# Data Sources

## Overview

This section should document all data sources used in your project.
Proper documentation ensures reproducibility and helps others
understand your research methodology.

## How to Document Your Data

For each data source, include the following information:

### 1. External Data Sources

- **Name**: Official name of the dataset
- **Version/Date**: Version number or access date
- **URL**: Link to the data source
- **Access Method**: How the data was obtained (direct download, API, etc.)
- **Access Date**: When the data was accessed/retrieved
- **Data Format**: Format of the data (FASTQ, DICOM, CSV, etc.)
- **Citation**: Proper academic citation if applicable
- **License**: Usage restrictions and attribution requirements

Example:

```markdown
## TCGA RNA-Seq Data

- **Name**: The Cancer Genome Atlas RNA-Seq Data
- **Version**: Data release 28.0 - March 2021
- **URL**: https://portal.gdc.cancer.gov/
- **Access Method**: GDC Data Transfer Tool
- **Access Date**: 2021-03-15
- **Citation**: The Cancer Genome Atlas Network. (2012). Comprehensive molecular portraits of human breast tumours. Nature, 490(7418), 61-70.
- **License**: [NIH Genomic Data Sharing Policy](https://sharing.nih.gov/genomic-data-sharing-policy)
```

### 2. Internal/Generated Data

- **Name**: Descriptive name of the dataset
- **Creation Date**: When the data was generated
- **Creation Method**: Brief description of how the data was created
- **Input Data**: What source data was used
- **Processing Scripts**: References to scripts/Github Repo used to generate this data

Example:

```markdown
## Processed RNA-Seq Data
- **Name**: Processed RNA-Seq Data for TCGA-BRCA
- **Creation Date**: 2021-04-01
- **Creation Method**: Processed using kallisto and DESeq2
- **Input Data**: FASTQ Data obtained from the SRA database
- **Processing Scripts**: [GitHub Repo](https://github.com/tcga-brca-rnaseq)
```

### 3. Data Dictionary

For complex datasets, include a data dictionary that explains:

| Column Name | Data Type | Description | Units | Possible Values |
|-------------|-----------|-------------|-------|-----------------|
| patient_id  | string    | Unique patient identifier | N/A | TCGA-XX-XXXX format |
| age         | integer   | Patient age at diagnosis | years | 18-100 |
| expression  | float     | Gene expression value | TPM | Any positive value |

## Best Practices

- Store raw data in `data/rawdata/` and never modify it
- Store processed data in `data/procdata/` and all code used to generate it should be in `workflow/scripts/`
- Document all processing steps
- Track data provenance (where data came from and how it was modified)
- Respect data usage agreements and licenses!
    This is especially important for data that should not be shared publicly



## TCGA-LIHC

- **Name**: The Cancer Genome Atlas Liver Hepatocellular Carcinoma Collection
- **Version**: Version 5: Updated 2020/05/29
- **URL**: portal.gdc.cancer.gov/projects/TCGA-LIHC
- **Access Method**: Downloaded from GDC Data Portal
- **Access Date**: 2025-07-09
- **Citation**: Erickson, B. J., Kirk, S., Lee, Y., Bathe, O., Kearns, M., Gerdes, C., Rieger-Christ, K., & Lemmerman, J. (2016). The Cancer Genome Atlas Liver Hepatocellular Carcinoma Collection (TCGA-LIHC) (Version 5) [Data set]. The Cancer Imaging Archive. https://doi.org/10.7937/K9/TCIA.2016.IMMQW8UQ
- **License**: CC BY 3.0

## NSCLC Radiogenomics

- **Name**: NSCLC Radiogenomics
- **Version**: Version 4: Updated 2021/06/01
- **URL**: NSCLC-RADIOGENOMICS - The Cancer Imaging Archive (TCIA)
- **Access Method**: Downloaded from TCIA website
- **Access Date**: 2025-07-03
- **Citation**: Bakr, S., Gevaert, O., Echegaray, S., Ayers, K., Zhou, M., Shafiq, M., Zheng, H., Zhang, W., Leung, A., Kadoch, M., Shrager, J., Quon, A., Rubin, D., Plevritis, S., & Napel, S. (2017). Data for NSCLC Radiogenomics (Version 4) [Data set]. The Cancer Imaging Archive. https://doi.org/10.7937/K9/TCIA.2017.7hs46erv
- **License**: CC BY 3.0

## RADCURE

- **Name**: Computed Tomography Images from Large Head and Neck Cohort
- **Version**: Version 4: Updated 2021/06/01
- **URL**: RADCURE - The Cancer Imaging Archive (TCIA)
- **Access Method**: Downloaded from TCIA website
- **Access Date**: 2025-07-17
- **Citation**: Welch, M. L., Kim, S., Hope, A., Huang, S. H., Lu, Z., Marsilla, J., Kazmierski, M., Rey-McIntyre, K., Patel, T., O’Sullivan, B., Waldron, J., Kwan, J., Su, J., Soltan Ghoraie, L., Chan, H. B., Yip, K., Giuliani, M., Princess Margaret Head And Neck Site Group, Bratman, S., … Tadic, T. (2023). Computed Tomography Images from Large Head and Neck Cohort (RADCURE) (Version 4) [Dataset]. The Cancer Imaging Archive. https://doi.org/10.7937/J47W-NM11
- **License**: CC BY 3.0



## HNSCC

- **Name**: Annotations for The Clinical Proteomic Tumor Analysis Consortium Head and Neck Squamous Cell Carcinoma Collection
- **Version**: Version 1: Updated 2023/07/24
- **URL**: CPTAC-HNSCC-TUMOR-ANNOTATIONS - The Cancer Imaging Archive (TCIA)
- **Access Method**: Downloaded from TCIA website
- **Access Date**: 2025-07-21
- **Citation**: Rozenfeld, M., & Jordan, P. (2023). Annotations for The Clinical Proteomic Tumor Analysis Consortium Head and Neck Squamous Cell Carcinoma Collection (CPTAC-HNSCC-Tumor-Annotations) (Version 1) [Data set]. The Cancer Imaging Archive. https://doi.org/10.7937/PFEC-T641

## ACRIN-6698

- **Name**: ACRIN 6698/I-SPY2 Breast DWI
- **Version**: Version 1: Updated 2021/12/17
- **URL**: https://www.cancerimagingarchive.net/collection/acrin-6698/
- **Access Method**: Downloaded from TCIA website
- **Access Date**: 2025-07-29
- **Citation**: Newitt, D. C., Partridge, S. C., Zhang, Z., Gibbs, J., Chenevert, T., Rosen, M., Bolan, P., Marques, H., Romanoff, J., Cimino, L., Joe, B. N., Umphrey, H., Ojeda-Fournier, H., Dogan, B., Oh, K. Y., Abe, H., Drukteinis, J., Esserman, L. J., & Hylton, N. M. (2021). ACRIN 6698/I-SPY2 Breast DWI [Data set]. The Cancer Imaging Archive. https://doi.org/10.7937/tcia.kk02-6d95
- **License**: CC BY 4.0


## HEAD-NECK-RADIOMICS-HN1

- **Name**: HEAD-NECK-RADIOMICS-HN1
- **Version**: Version 3: Updated 2020/07/29
- **URL**: HEAD-NECK-RADIOMICS-HN1 - The Cancer Imaging Archive (TCIA)
- **Access Method**: Downloaded from TCIA website
- **Access Date**: 2025-07-21
- **Citation**: Wee, L., & Dekker, A. (2019). Data from HEAD-NECK-RADIOMICS-HN1 [Data set]. The Cancer Imaging Archive. https://doi.org/10.7937/tcia.2019.8kap372n
- **License**: CC BY-NC 3.0




## NSCLC-Radiomics

- **Name**: NSCLC-Radiomics
- **Version**: Version 4: Updated 2020/10/22
- **URL**: NSCLC-RADIOMICS - The Cancer Imaging Archive (TCIA)
- **Access Method**: Downloaded from TCIA website
- **Access Date**: 2025-07-22
- **Citation**: Aerts, H. J. W. L., Wee, L., Rios Velazquez, E., Leijenaar, R. T. H., Parmar, C., Grossmann, P., Carvalho, S., Bussink, J., Monshouwer, R., Haibe-Kains, B., Rietveld, D., Hoebers, F., Rietbergen, M. M., Leemans, C. R., Dekker, A., Quackenbush, J., Gillies, R. J., Lambin, P. (2014). Data From NSCLC-Radiomics (version 4) [Data set]. The Cancer Imaging Archive. https://doi.org/10.7937/K9/TCIA.2015.PF0M9REI
- **License**: CC BY-NC 3.0




## NSCLC-Radiomics-Interobserver1

- **Name**: NSCLC-Radiomics-Interobserver1
- **Version**: Version 3: Updated 2020/08/31
- **URL**: NSCLC-RADIOMICS-INTEROBSERVER1 - The Cancer Imaging Archive (TCIA)
- **Access Method**: Downloaded from TCIA website
- **Access Date**: 2025-07-22
- **Citation**: Wee, L., Aerts, H. J.L., Kalendralis, P., & Dekker, A. (2019). Data from NSCLC-Radiomics-Interobserver1 [Data set]. The Cancer Imaging Archive. https://doi.org/10.7937/tcia.2019.cwvlpd26.
- **License**: CC BY-NC 3.0




## TCGA-BRCA

- **Name**: The Cancer Genome Atlas Breast Invasive Carcinoma Collection
- **Version**: Version 3: Updated 2020/05/29
- **URL**: portal.gdc.cancer.gov/projects/TCGA-BRCA
- **Access Method**: Downloaded from GDC Data Portal
- **Access Date**: 2025-07-22
- **Citation**: Lingle, W., Erickson, B. J., Zuley, M. L., Jarosz, R., Bonaccio, E., Filippini, J., Net, J. M., Levi, L., Morris, E. A., Figler, G. G., Elnajjar, P., Kirk, S., Lee, Y., Giger, M., & Gruszauskas, N. (2016). The Cancer Genome Atlas Breast Invasive Carcinoma Collection (TCGA-BRCA) (Version 3) [Data set]. The Cancer Imaging Archive. https://doi.org/10.7937/K9/TCIA.2016.AB2NAZRP
- **License**: CC BY-NC 3.0





## TCGA-BLCA

- **Name**: The Cancer Genome Atlas Urothelial Bladder Carcinoma Collection
- **Version**: Version 8: Updated 2020/05/29
- **URL**: portal.gdc.cancer.gov/projects/TCGA-BLCA
- **Access Method**: Downloaded from GDC Data Portal
- **Access Date**: 2025-07-22
- **Citation**: Kirk, S., Lee, Y., Lucchesi, F. R., Aredes, N. D., Gruszauskas, N., Catto, J., Garcia, K., Jarosz, R., Duddalwar, V., Varghese, B., Rieger-Christ, K., & Lemmerman, J. (2016). The Cancer Genome Atlas Urothelial Bladder Carcinoma Collection (TCGA-BLCA) (Version 8) [Data set]. The Cancer Imaging Archive. https://doi.org/10.7937/K9/TCIA.2016.8LNG8XDR
- **License**: CC BY 3.0





## TCGA-COAD

- **Name**: The Cancer Genome Atlas Colon Adenocarcinoma Collection
- **Version**: Version 3: Updated 2020/05/29
- **URL**: portal.gdc.cancer.gov/projects/TCGA-COAD
- **Access Method**: Downloaded from GDC Data Portal
- **Access Date**: 2025-07-22
- **Citation**: Kirk, S., Lee, Y., Sadow, C. A., Levine, S., Roche, C., Bonaccio, E., & Filiippini, J. (2016). The Cancer Genome Atlas Colon Adenocarcinoma Collection (TCGA-COAD) (Version 3) [Data set]. The Cancer Imaging Archive. https://doi.org/10.7937/K9/TCIA.2016.HJJHBOXZ
- **License**: CC BY 3.0






## TCGA-HNSC

- **Name**: The Cancer Genome Atlas Head-Neck Squamous Cell Carcinoma Collection
- **Version**: Version 6: Updated 2023/05/24
- **URL**: portal.gdc.cancer.gov/projects/TCGA-HNSC
- **Access Method**: Downloaded from GDC Data Portal
- **Access Date**: 2025-07-22
- **Citation**: Zuley, M. L., Jarosz, R., Kirk, S., Lee, Y., Colen, R., Garcia, K., Delbeke, D., Pham, M., Nagy, P., Sevinc, G., Goldsmith, M., Khan, S., Net, J. M., Lucchesi, F. R., & Aredes, N. D. (2016). The Cancer Genome Atlas Head-Neck Squamous Cell Carcinoma Collection (TCGA-HNSC) (Version 6) [Data set]. The Cancer Imaging Archive. https://doi.org/10.7937/K9/TCIA.2016.LXKQ47MS
- **License**: NIH Controlled Data Access Policy




## TCGA-LUSC

- **Name**: The Cancer Genome Atlas Lung Squamous Cell Carcinoma Collection
- **Version**: Version 4: Updated 2020/05/29
- **URL**: portal.gdc.cancer.gov/projects/TCGA-LUSC
- **Access Method**: Downloaded from GDC Data Portal
- **Access Date**: 2025-07-22
- **Citation**: Kirk, S., Lee, Y., Kumar, P., Filippini, J., Albertina, B., Watson, M., Rieger-Christ, K., & Lemmerman, J. (2016). The Cancer Genome Atlas Lung Squamous Cell Carcinoma Collection (TCGA-LUSC) (Version 4) [Data set]. The Cancer Imaging Archive. https://doi.org/10.7937/K9/TCIA.2016.TYGKKFMQ
- **License**: CC BY 3.0

## TCGA-UCEC

- **Name**: The Cancer Genome Atlas Uterine Corpus Endometrial Carcinoma Collection
- **Version**: Version 4: Updated 2020/05/29
- **URL**: portal.gdc.cancer.gov/projects/TCGA-UCEC
- **Access Method**: Downloaded from GDC Data Portal
- **Access Date**: 2025-07-22
- **Citation**: Erickson, B. J., Mutch, D., Lippmann, L., & Jarosz, R. (2016). The Cancer Genome Atlas Uterine Corpus Endometrial Carcinoma Collection (TCGA-UCEC) (Version 4) [Data set]. The Cancer Imaging Archive. https://doi.org/10.7937/K9/TCIA.2016.GKJ0ZWAC
- **License**: CC BY 3.0

## CC-Tumor-Heterogeneity

- **Name**: Cervical Cancer – Tumor Heterogeneity: Serial Functional and Molecular Imaging Across the Radiation Therapy Course in Advanced Cervical Cancer
- **Version**: Version 2: Updated 2023/02/23
- **URL**: CC-TUMOR-HETEROGENEITY - The Cancer Imaging Archive (TCIA)
- **Access Method**: Downloaded from TCIA website
- **Access Date**: 2025-07-22
- **Citation**: Mayr, N., Yuh, W. T. C., Bowen, S., Harkenrider, M., Knopp, M. V., Lee, E. Y.-P., Leung, E., Lo, S. S., Small Jr., W., & Wolfson, A. H. (2023). Cervical Cancer – Tumor Heterogeneity: Serial Functional and Molecular Imaging Across the Radiation Therapy Course in Advanced Cervical Cancer (Version 1) [Data set]. The Cancer Imaging Archive. https://doi.org/10.7937/ERZ5-QZ59
- **License**: CC BY 4.0

## ISPY2

- **Name**: I-SPY 2 Breast Dynamic Contrast Enhanced MRI Trial
- **Version**: Version 1: Updated 2022/05/02
- **URL**: https://www.cancerimagingarchive.net/collection/ispy2/
- **Access Method**: Downloaded from TCIA website
- **Access Date**: 2025-07-29
- **Citation**: Li, W., Newitt, D. C., Gibbs, J., Wilmes, L. J., Jones, E. F., Arasu, V. A., Strand, F., Onishi, N., Nguyen, A. A.-T., Kornak, J., Joe, B. N., Price, E. R., Ojeda-Fournier, H., Eghtedari, M., Zamora, K. W., Woodard, S. A., Umphrey, H., Bernreuter, W., Nelson, M., … Hylton, N. M. (2022). I-SPY 2 Breast Dynamic Contrast Enhanced MRI Trial (ISPY2)  (Version 1) [Data set]. The Cancer Imaging Archive. https://doi.org/10.7937/TCIA.D8Z0-9T85
- **License**: CC BY 4.0
