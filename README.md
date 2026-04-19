# Medicare FFS CERT Data Analysis and Automated Data Cleaning
### Nicole Riley, RHIT | HIM 5005 | University of Cincinnati Clermont

## Project Overview
The Medicare CERT program measures the improper payment rate in the Medicare Fee-for-Service program by reviewing a random sample of paid claims each year. This project combines five years of CERT public use data (FY 2021–2025) to enable multi-year trend analysis of improper payment patterns across claim types, provider types, and error codes. The inpatient subset is further enriched with MS-DRG descriptions from the Tuva Project to enable diagnosis-level analysis of inpatient improper payment trends. 

To reproduce this analysis, download the source files listed below, update the file paths in the notebook, and run all cells. The script will output two analysis-ready CSV files: a combined five-year CERT dataset and an inpatient subset enriched with MS-DRG descriptions.

This project was completed as part of the HIM 5005 Data Club experiential learning experience. It involves loading, cleaning, and preparing public use data for exploratory analysis and visualization in Power BI.

## Data Sources
The datasets used in this project are publicly available and can be downloaded directly from the original sources listed in the **CMS CERT Data (FY 2021–2025)** and **Tuva Project MS-DRG Reference Terminology** sections below. 
Due to file size, the raw and cleaned CSV files are not included in this repository.

### CMS CERT Data (FY 2021–2025)
Five years of Medicare FFS CERT public use files were downloaded from the CMS website 
and combined into a single analysis-ready dataset.

Centers for Medicare & Medicaid Services. (2021). *Comprehensive Error Rate Testing 
(CERT) public use file, FY 2021* [Data set]. U.S. Department of Health and Human 
Services. [Link](https://data.cms.gov/provider-compliance/fee-for-service-error-rate-improper-payment/medicare-fee-for-service-comprehensive-error-rate-testing/data/2021)

Centers for Medicare & Medicaid Services. (2022). *Comprehensive Error Rate Testing 
(CERT) public use file, FY 2022* [Data set]. U.S. Department of Health and Human 
Services. [Link](https://data.cms.gov/provider-compliance/fee-for-service-error-rate-improper-payment/medicare-fee-for-service-comprehensive-error-rate-testing/data/2022)

Centers for Medicare & Medicaid Services. (2023). *Comprehensive Error Rate Testing 
(CERT) public use file, FY 2023* [Data set]. U.S. Department of Health and Human 
Services. [Link](https://data.cms.gov/provider-compliance/fee-for-service-error-rate-improper-payment/medicare-fee-for-service-comprehensive-error-rate-testing/data/2023)

Centers for Medicare & Medicaid Services. (2024). *Comprehensive Error Rate Testing 
(CERT) public use file, FY 2024* [Data set]. U.S. Department of Health and Human 
Services. [Link](https://data.cms.gov/provider-compliance/fee-for-service-error-rate-improper-payment/medicare-fee-for-service-comprehensive-error-rate-testing/data/2024)

Centers for Medicare & Medicaid Services. (2025). *Comprehensive Error Rate Testing 
(CERT) public use file, FY 2025* [Data set]. U.S. Department of Health and Human 
Services. [Link](https://data.cms.gov/provider-compliance/fee-for-service-error-rate-improper-payment/medicare-fee-for-service-comprehensive-error-rate-testing/data)

### Tuva Project MS-DRG Reference Terminology
The DRG reference terminology used in this project was sourced from the Tuva Project, an open-source healthcare data platform maintained by Tuva Health. Founded by former senior executives from Health Catalyst and Strive Health, the Tuva Project is backed by Y Combinator and a community of over 2,400 healthcare data professionals including engineers, analysts, and informaticists. Its terminology sets are community-reviewed and widely used by payers, providers, and research institutions, making it a reliable source for standardized healthcare reference data.

Tuva Health. (n.d.). *DRG* [Reference terminology set]. The Tuva Project. [Link](https://thetuvaproject.com/terminology/ms-drg)

## Tools Used
- Python (Pandas, NumPy)
- Power BI

## Repository Contents
- `Cleaning_script_notebook.ipynb` — full documented data preparation notebook

## Notes
- DRG data is only present for Part A Inpatient Hospital PPS claims
- MS-DRG descriptions may vary slightly across fiscal years; the Tuva reference file reflects current assignments and is applied uniformly across all years
- The CERT improper payment rate reflects a snapshot in time; claims still in the appeals process are not reflected in the overturn rate
