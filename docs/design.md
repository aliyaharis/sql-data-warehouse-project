# Design Document

This project follows the Medallion Architecture.

Bronze: Raw, unprocessed data
Silver: Cleaned and standardised data
Gold: Aggregated, business-ready data

##Source

Object Type: CSV files
Interface: Files in folders

##Bronze Layer

Object Type: Tables
Load: 
    - Batch Processing
    - Full Load
    - Truncate & Insert

Transformations: None
Date Model: None

##Silver Layer

Object Type: Tables
Load:
    - Batch Processing
    - Full Load
    - Truncate & Insert
Transformations: 
    - Data Cleansing
    - Data Standardization
    - Data Normalization
    - Derived Columns
    - Data Enrichment
Data Model: None

##Gold Layer

Object Type: Views
Load: None
Transformations: 
    - Data Integrations
    - Data Aggregation
    - Business Logic
Date Model: 
    - Star Schema
    - Flat Table
    - Aggregated Table


##Naming Convention: Snake Case