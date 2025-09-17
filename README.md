# Climate Match System

This project processes 36+ million climate records to recommend ideal relocation destinations based on climate preferences. It uses historical climate data to cluster ZIP code areas and match users to regions with similar average monthly temperature patterns.

Developed as part of a WGU capstone, the system integrates data cleaning, unsupervised machine learning, and a basic user interface for interactive exploration.

## Results/Performance
The system successfully clustered ~10,000 ZIP codes into distinct climate profiles, enabling users to find locations with similar temperature patterns across the United States.

## Project Structure

- **`Scripted_data_cleaning.ipynb`**  
  Prepares the historical temperature dataset for clustering.  
  _Note: This notebook uses a large dataset from UNC Dataverse, which is not included in this repo. You only need to download it if you want to reproduce the full cleaning process from raw data._

- **`Clustering_data.ipynb`**  
  Applies K-means clustering to ZIP code temperature profiles and visualizes the results. Uses the cleaned `ten_year_avg_2008_2017.csv` dataset.

- **`Climate_Match_App.ipynb`**  
  A simple console-based menu system that allows users to explore climate-matched metro areas by selecting from U.S. states or climate profiles. The system displays recommended metro areas with similar temperature patterns based on historical clustering data.

## Included Data Files

- **`ten_year_avg_2008_2017.csv`**  
  Cleaned ZIP-level monthly average temperatures (2008–2017). Required only for the clustering notebook.

- **`clustered_ZIP_climates.csv`**  
  Output from the clustering notebook. Required by the app notebook for ZIP code matching.

## Technologies Used

* Python (`pandas`, `scikit-learn`, `geopandas`, `matplotlib`, `seaborn`)
* R Script (for data conversion from .rds format)
* K-means Clustering
* Jupyter Notebooks
* U.S. ZIP Code and Temperature Data

## Limitations

- This is a proof-of-concept intended for educational use.
