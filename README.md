AusTraits_Analysis
==================
> This is a machine learning analysis of AusTraits; a curated plant trait database for Australian Flora. The goal is to identify local native plant species using easily measurable traits.
> 
> The main website for [AusTraits](https://austraits.org/) provides up to date information on the database and access methods via Zenodo, R interface and an API:
> `"It synthesises data on nearly 500 traits across more than 30,000 taxa from field campaigns, published literature, taxonomic monographs, and individual taxon descriptions."`

# 1. Problem Statement
Develop machine learning algorithm to identify local native plant species using easily measurable traits. "Local" to be defined, but approximately indicated here, within the orange border:

![Extended South West of Western Australia](Local_Species_Region.png "Region - Local Species")

# 2. Methodology

## 2.1 Download Database as CSV
* Download "austraits-7.0.0.zip", dated Jun 20, 2025, from page [Version v7.0.0][](https://zenodo.org/records/15718081).

## 2.2 Inspect Database Contents
* Review files contained within.
* Determine which files are applicable and can be utilized.

## 2.3 EDA, Clean data, Tranform Data
* Determine how to perform EDA given the large dataset size.
    * Identify useful features.
    * Determine how to read in data while retaining only useful features and useful records.
    * Initial transformation of any data not in a convenient format for Pandas DataFrane(s).
    * Formalize process as a function for reproduceability.
* Perform general EDA.
* Perform full data cleaning using a Pipeline().
* Determine how to best clean the data using a Transform.

## 2.4 Perform Feature Engineering
* Features may be selected or further transformed.
* Check correlations for feature redundancies.
