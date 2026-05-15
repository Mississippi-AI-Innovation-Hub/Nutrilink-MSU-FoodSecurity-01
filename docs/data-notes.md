# Data Notes

## Overview

The NutriLink proof-of-concept used publicly available health, nutrition, and food assistance information to support Retrieval-Augmented Generation (RAG) workflows through Amazon Bedrock Knowledge Bases.

The PoC focused primarily on Hinds County, Mississippi, and used curated markdown-based documents uploaded into Amazon S3 for retrieval during query processing.

---

# Primary Data Sources

## County Health Rankings and Roadmaps (CHRR)

The PoC incorporated county-level health indicators and contextual information from County Health Rankings and Roadmaps (CHRR).

### Example Context Areas

- Diabetes prevalence
- Obesity-related indicators
- Food insecurity metrics
- County-level health context
- Geographically relevant recommendations

The CHRR information was used to provide county-aware context for recommendations and food assistance guidance.

---

## HER Nutrition Guidelines

The Healthy Eating Research (HER) Nutrition Guidelines were used as a nutritional guidance framework within the PoC.

### HER Usage in the PoC

- Evidence-based nutrition standards
- Healthy vs. unhealthy food categorization
- Recommendation guidance context
- Nutrition-informed response support

HER guidance was intended to support healthier food recommendations and nutrition-oriented prompting.

---

## SWAP Framework

The Supporting Wellness at Pantries (SWAP) framework was used to provide simplified nutritional categorization logic.

### SWAP Usage in the PoC

- Green / Yellow / Red nutritional categorization
- Simplified food quality classification
- Nutrition-supportive pantry guidance
- Food recommendation context

The framework was included as contextual retrieval information within uploaded markdown datasets.

---

## Local Food Resource Data

The PoC also used locally curated food assistance resource information related to Hinds County.

### Example Resource Types

- Food banks
- Community pantries
- SNAP-related resources
- Community organizations
- County-based assistance information

The goal was to support geographically relevant food resource recommendations.

---

# Data Processing Approach

Data used during the PoC was manually reviewed, cleaned, and converted into markdown-based documents for ingestion into Amazon S3 and Amazon Bedrock Knowledge Bases.

The architecture followed a lightweight Retrieval-Augmented Generation workflow:

1. Documents uploaded to Amazon S3
2. Bedrock Knowledge Base indexing
3. Retrieval of relevant context chunks
4. Nova 2 Lite response generation

---

# Repository Data Policy

This public repository does NOT contain:

- Protected agency records
- Operational MDHS data
- Personally identifiable information
- Credentials or secrets
- Private citizen information

Any included sample datasets are illustrative only and intended solely for demonstrating repository structure and workflow concepts.

---

# Limitations

The PoC relied on limited publicly available data and simplified document structures appropriate for a prototype environment.

Known limitations include:

- Hinds County-only scope
- Limited nutritional granularity
- Manual data preparation
- Limited retrieval evaluation
- No production-grade data pipeline

---

# References

1. County Health Rankings & Roadmaps  
   https://www.countyhealthrankings.org/

2. HER Nutrition Guidelines  
   https://uconnruddcenter.org/her-guidelines/

3. Mississippi Food Network  
   https://www.msfoodnet.org/about-us/hunger/

4. Friends Committee on National Legislation – Hungriest States  
   https://www.fcnl.org/updates/2024-09/top-10-hungriest-states-us