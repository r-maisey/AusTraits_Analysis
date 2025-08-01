AusTraits_Analysis
==================
> This is a machine learning analysis of AusTraits; a curated plant trait database for Australian Flora. The goal is to identify local native plant species using easily measurable traits.
> 
> The main website for [AusTraits](https://austraits.org/) provides up to date information on the database and access methods via Zenodo, R interface and an API:
> `"It synthesises data on nearly 500 traits across more than 30,000 taxa from field campaigns, published literature, taxonomic monographs, and individual taxon descriptions."`
>
> It was found the data samples do not conform well to ML:
> * Sample values for traits are typically aggregated, rather than raw samples. E.g. mean, mde, maximum, minimum
>   * This also results in there being limited samples per taxon.
> * Sample values are inconsistent between taxons; there are many samples in total, but there are also many taxons and many features:
>   * There are many features but taxons don't have values for every feature, even for a subset of the more common features.
>   * Rolling up taxons to the genus level still results in inconsistency in data, furthermore, the features will be different for different species/subspecies/forms/etc. as this is what separates them in the first place.
>   * A test subset will not contain features not represented in the training data set and vice-versa, for any given taxon.
>  
> Unfortuantely, this data is not suited to provide a model to solve the problem statement. The data could be suitable if it were the raw data and data sources were consistent with data collection.

# 1. Problem Statement
Develop machine learning algorithm to identify native plant species using easily measurable traits.

# 2. Methodology

## 2.1 Download Database as CSV
* Download "austraits-7.0.0.zip", dated Jun 20, 2025, from page [Version v7.0.0][](https://zenodo.org/records/15718081).

## 2.2 Inspect Database Contents
* Review files contained within.
* Determine which files are applicable and can be utilized.

## 2.3 EDA, Clean data, Tranform Data
* Determine how to perform EDA given the large dataset size.
    * Identify useful features.
    * Initial transformation of any data not in a convenient format for Pandas DataFrame(s).
    * Formalize process as a function for reproduceability.
* Perform general EDA.
* Perform full data cleaning using a Pipeline().
* Determine how to best clean the data using a Transform.

## 2.4 Perform Feature Engineering
* Features may be selected or further transformed.
* Check correlations for feature redundancies.
