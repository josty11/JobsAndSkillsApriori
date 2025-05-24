# JobsAndSkillsApriori

This repository contains a project developed for the *Algorithms for Massive Data* course during my Master’s in Data Science and Economics. The goal was to apply the Apriori algorithm for market-basket analysis on job skills data, using a scalable approach with Apache Spark.

## Project Overview

We use the LinkedIn Jobs & Skills dataset (Kaggle) to identify frequent skill combinations across job postings: similar to how market-basket analysis identifies frequently bought items together. The focus was on scalability and distributed processing using Spark.

The repository includes:
- A Jupyter notebook with the complete implementation
- A PDF report detailing methodology, results, and reflections

## Key Steps
### Project Setup
- Start a Spark session and install required libraries
- Load dataset directly from Kaggle
- Clean up the environment by removing irrelevant files

### Data Preprocessing
- Perform text normalization (lowercasing, whitespace removal)
- Group data into skill "baskets"
- Generate hash mappings for efficient processing

### Apriori Algorithm Implementation
The Apriori algorithm was implemented from scratch using PySpark RDD transformations:
- Count and identify frequent singletons
- Generate candidate itemsets iteratively using combinations and prior frequent sets
- Apply minimum support filtering
- Track and print most frequent itemsets at each level (e.g. pairs, triplets)
- Support sampling for quick testing on large datasets
