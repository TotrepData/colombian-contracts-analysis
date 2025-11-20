# Government Contracts Analysis

Analysis of procurement data from Colombia's public contracting system (SECOP) and national investment project bank (BPIN) using Apache Spark.

## Overview

This repository contains scalable data processing workflows to analyze government spending patterns, supplier concentration, and procurement trends. The analysis uses Spark for distributed computing on large-scale government datasets.

## Data Sources

- **SECOP**: Sistema Electrónico para la Contratación Pública - Colombian government procurement registry
- **BPIN**: Banco de Proyectos de Inversión Nacional - National investment project database

## Contents

- `Procurement_Analysis.ipynb` - Main analysis notebook with contract value analysis, supplier evaluation, and text mining of procurement descriptions

## Key Analyses

1. **Supplier Rankings** - Identification of top suppliers by contract value and volume
2. **Value Distribution** - Statistical analysis of contract values across years
3. **Market Concentration** - Evaluation of supplier concentration in procurement
4. **Market Entry** - Analysis of new suppliers entering the system
5. **Service Contracts** - Statistical overview of service provision contracts
6. **Supplier Diversity** - Tracking unique suppliers over time
7. **Procurement Focus** - Word frequency analysis of contract descriptions

## Requirements

- Apache Spark 3.x
- PySpark
- Access to Azure Blob Storage (for data paths)

## Usage

Run the notebook in Databricks or any Spark-compatible environment. Update data paths in the data loading section to match your environment.

```python
from pyspark.sql import functions as F
from pyspark.sql import Window
```

## Notes

- SECOP data is loaded with sampling-based schema inference for performance optimization
- Approximate distinct count functions are used for large-scale aggregations
- All values are in Colombian pesos (COP)

## Author

**Javier Mondragón**  
Data Engineer | Universidad de los Andes

## License

Educational Project
