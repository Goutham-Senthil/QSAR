# QSAR-Based Prediction of Liver Metabolism (CYP450)

This is a QSAR based approach to predict if a given compound will be metabolized by the liver (Cytochrome P450) or not

## Datasets

There are 2 datasets used in this project 

### 1 . DrugBank
Available at [DrugBank](https://go.drugbank.com/](https://go.drugbank.com/releases/latest )

You will need an academic license to use this dataset

The version of the dataset used for this dataset is 5.1.13	

### 2. ChEMBL
Available at [ChEMBL](https://ftp.ebi.ac.uk/pub/databases/chembl/ChEMBLdb/latest/)

The version of the dataset used for this dataset is `chembl_35.db`

## ADMETLab 3.0 Calculation

[ADMETLab3.0](https://admetmesh.scbdd.com/)  was used to get CYP450 isoform metabolite scores and this was done by submitting the smiles values 500 at a time. This task was done manually and for the ease of seeing the results , I have done the extraction and all the values are present in the directory `clean_smiles_bacth_values_admet_3`. 

## Running the project 

1. Install the required packages:
 ```bash
 pip install -r requirements.txt
```
2. Run Code_1A.ipynb until  Mark down that says "Save the dataset"  (this is to extract all compounds from DrugBank and remove overlap with compounds present in ChEMBL)
3. Run the full ChEMBL_dataset_extraction.ipynb
4. Run the remaining of Code_1A.ipynb 

## Aim of the project

This project aimed to answer the following research questions 

1. How do different sampling (class weights, oversampling, undersampling) techniques
affect the performance of Random Forest Models?
2. How do different decision tree (LightGBM, Random Forest, XGBoost) algorithms
compare against each other?
3. Does incorporating different molecular fingerprints (Morgan, MACCS, Daylight-like)
help boost the model’s predictability?
4. Do metabolite scores obtained from ADMET analysis significantly enhance predictive
performance?
5. Does incorporating a silver-standard dataset, specifically ChEMBL, improve the predictive performance of the model ?

