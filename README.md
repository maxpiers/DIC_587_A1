# DIC_587_A1: CVE Lakehouse on Databricks

Pipeline for data ingestion, Bronze Medallion delta lake creation, Silver Medallion delta lake creation, and exploratory analysis of 2024 CVE data.

## Description

A CVE (Common Vulnerability and Exposure) is a publicly disclosed cybersecurity vulnerability that has been assigned an identifier for tracking and reference, to allow the cybersecurity community to discuss and address the issues. This project creates a pipeline to ingest the CVE data published in 2024, persist it in Databricks, and perform exploratory analysis on the data. First, the pipeline ingests the raw JSON files, filters to the year 2024, and reads the raw files into a DataFrame to be saved into a "Bronze Medallion" delta lake and persisted in the user's Databricks Catalog. Then, the complex nested structures in the JSON files are parsed into a Databricks friendly schema, and selected columns of the data is extracted into tables that are persisted as the "Silver Medallion" delta lake. Finally, exploratory analysis is performed on the silver lake using a SQL file for ease of visualization. The whole pipeline is built to be functional with a Databricks Free Edition account.

## Getting Started

### Installing

* Create a Databricks Free Edition account
* [Databricks Free Edition signup link](https://login.databricks.com/signup?provider=DB&scid=7018Y000001Fi0MQAS&utm_medium=paid+search&utm_source=google&utm_campaign=14272820537&utm_adgroup=126939742998&utm_content=trial&utm_offer=trial&utm_ad=724888424298&utm_term=is+databricks+free&dbx_source=paid&gad_source=1&gad_campaignid=14272820537&gbraid=0AAAAABYBeAibIBw6xGEBz_-Q5WGCAiiiz&gclid=Cj0KCQiAiebIBhDmARIsAE8PGNJAp1RWWv_2sXfDj0J-Bpvl8CEyWZhNIpW9wfFVHhdL-zx2tbiyvYYaArp2EALw_wcB&tuuid=e67ea8b7-b8d1-4171-8e4c-54846f34f568&intent=SIGN_UP&rl_aid=378b9226-383a-4470-b70e-b54aba0408a2&sisu_state=eyJsZWdhbFRleHRTZWVuIjp7Ii9zaWdudXAiOnsidG9zIjp0cnVlLCJwcml2YWN5Ijp0cnVlLCJjb3Jwb3JhdGVFbWFpbFNoYXJpbmciOnRydWV9fX0%3D)
* Import notebook files into Databricks workspace

### Executing program

* To run the pipeline:
* Create a Databricks account with the link above
* Import all files into a Databricks workspace
* Run all cells in "01_ingest_cvelist.ipynb" to ingest the data and create the Bronze lake
* Run all cells in "02_bronze_to_silver.ipynb" to convert the Bronze lake into a Silver lake
* Run all cells in "03_exploratory_analysis.ipynb" to perform analysis on the Silver lake
* Customize visualizations as desired

### Example Visualizations
<img width="1782" height="600" alt="viz0" src="https://github.com/user-attachments/assets/a2ba271b-11bf-4644-94aa-9884334268b5" />
<img width="1164" height="405" alt="viz1" src="https://github.com/user-attachments/assets/b8073dbb-76ad-4b35-a103-30646e159952" />
<img width="1782" height="600" alt="viz2" src="https://github.com/user-attachments/assets/e83383ee-c7bb-409c-a396-16353f29ff64" />
<img width="1782" height="600" alt="viz3" src="https://github.com/user-attachments/assets/baaa3751-55b0-4995-83ea-f02056a7e7a1" />
<img width="1164" height="405" alt="viz4" src="https://github.com/user-attachments/assets/814ac12b-9773-495b-b21a-8aa7fe901481" />

## Authors

Max Pierson [maxpiers@buffalo.edu]
