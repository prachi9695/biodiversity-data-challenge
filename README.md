# Biodiversity Data Challenge - Frog Species Prediction

## About

🐸 **Predicting frog species presence using satellite climate data** 🌍

This project demonstrates the power of combining biodiversity data with satellite-derived climate information to predict species distributions. Using machine learning and geospatial analysis, we predict frog presence in southeastern Australia based on 14 TerraClimate variables from Microsoft's Planetary Computer.

**Key Features:**
- 📊 6,314 training samples with 14 climate variables
- 🌡️ TerraClimate data integration (1958-present)
- 🗺️ Geospatial analysis for precise location-based predictions
- 🤖 Binary classification with Logistic Regression
- 📈 Comprehensive model evaluation and validation
- 🎓 Educational focus for environmental data science

Perfect for learning satellite data analysis, geospatial machine learning, and biodiversity modeling!

---

## Project Overview

This project focuses on predicting the presence of frog species in southeastern Australia using climate variables from the TerraClimate dataset. The goal is to build a binary classification model that can accurately predict whether frogs are present at specific geographic locations based on environmental factors.

## 🎯 Objective

The primary objective is to develop a machine learning model that predicts frog species presence using TerraClimate variables extracted from the Microsoft Planetary Computer data catalog. The model uses monthly climate and climatic water balance data from 1958 to the present to understand the relationship between environmental conditions and frog habitat suitability.

## 📊 Datasets

### 1. Frog Presence Data
- **Source**: [Global Biodiversity Information Facility (GBIF)](https://www.gbif.org/)
- **Coverage**: Southeastern Australia
- **Time Period**: November 2017 to November 2019 (2 years)
- **Format**: CSV with columns:
  - `Latitude`: Geographic latitude coordinates
  - `Longitude`: Geographic longitude coordinates  
  - `Occurrence Status`: Binary indicator (1 = presence, 0 = absence)

### 2. Climate Data (TerraClimate)
- **Source**: [Microsoft Planetary Computer](https://planetarycomputer.microsoft.com/dataset/terraclimate)
- **Coverage**: Global terrestrial surfaces
- **Time Period**: 1958 to present
- **Resolution**: ~4-km (1/24th degree) spatial resolution
- **Variables**: 14 climate variables including:
  - `aet`: Actual Evapotranspiration
  - `def`: Climate Water Deficit
  - `pdsi`: Palmer Drought Severity Index
  - `pet`: Potential Evapotranspiration
  - `ppt`: Precipitation
  - `q`: Runoff
  - `soil`: Soil Moisture
  - `srad`: Downward Shortwave Radiation Flux
  - `swe`: Snow Water Equivalent
  - `tmax`: Maximum Temperature
  - `tmin`: Minimum Temperature
  - `vap`: Vapor Pressure
  - `vpd`: Vapor Pressure Deficit
  - `ws`: Wind Speed

## 🏗️ Project Structure

```
biodiversity_data_Challenge/
├── Biodiversity_Challenge_Group6.ipynb    # Main analysis notebook
├── TerraClimate.ipynb                     # TerraClimate data processing
├── Training_Data.csv                      # Training dataset (6,314 samples)
├── Validation_Template.csv                 # Validation dataset (2,002 samples)
├── Biodiversity_Challenge_Overview.pdf    # Project overview document
├── Group 6 - Value Case.pdf              # Value case analysis
└── README.md                             # This file
```

## 🔬 Methodology

### Data Processing Pipeline

1. **Data Loading**: Load frog presence data and TerraClimate variables
2. **Geospatial Extraction**: Extract climate values for each frog observation location
3. **Feature Engineering**: Combine frog presence data with climate variables
4. **Data Preprocessing**: Handle missing values and normalize features
5. **Model Training**: Train binary classification model
6. **Evaluation**: Assess model performance using classification metrics
7. **Validation**: Predict on new locations using validation template

### Machine Learning Approach

- **Algorithm**: Logistic Regression
- **Preprocessing**: 
  - Missing value imputation (median)
  - Feature scaling (MinMaxScaler)
- **Evaluation Metrics**: Precision, Recall, F1-Score, Accuracy
- **Cross-validation**: Train-test split (70-30)

## 🚀 Getting Started

### Prerequisites

Install the required Python packages:

```bash
pip install numpy pandas matplotlib seaborn xarray geopandas rasterio
pip install scikit-learn joblib tqdm pystac-client planetary-computer
```

### Running the Analysis

1. **Open the main notebook**:
   ```bash
   jupyter notebook Biodiversity_Challenge_Group6.ipynb
   ```

2. **Follow the workflow**:
   - Load and explore the training data
   - Process TerraClimate variables
   - Build and train the machine learning model
   - Evaluate model performance
   - Generate predictions for validation dataset

3. **For TerraClimate data processing**:
   ```bash
   jupyter notebook TerraClimate.ipynb
   ```

## 📈 Model Performance

The current implementation demonstrates:
- **Binary Classification**: Predicting frog presence (1) vs absence (0)
- **Feature Selection**: Using 14 TerraClimate variables as predictors
- **Geographic Coverage**: Southeastern Australia region
- **Temporal Coverage**: 2-year period (2017-2019)

## 🎓 Educational Purpose

This project serves as a learning tool for:
- **Satellite Data Analysis**: Working with TerraClimate datasets
- **Geospatial Machine Learning**: Combining location data with environmental variables
- **Biodiversity Modeling**: Understanding species-environment relationships
- **Real-world Applications**: Practical experience with ecological data science

## 🔍 Key Features

- **Comprehensive Climate Variables**: 14 different environmental factors
- **Geospatial Integration**: Precise location-based climate extraction
- **Scalable Architecture**: Can be extended to other species or regions
- **Reproducible Workflow**: Complete data processing and modeling pipeline
- **Validation Framework**: Structured approach for model evaluation

## 📝 Output Format

The model generates predictions in the following format:
```csv
Latitude,Longitude,Occurrence Status
-33.121788,150.320746,1
-36.592011,148.172262,0
...
```

## 🤝 Contributing

This is an educational project designed for learning purposes. Students are encouraged to:
- Experiment with different climate variables
- Try alternative machine learning algorithms
- Explore additional data preprocessing techniques
- Extend the analysis to other geographic regions

## 📚 References

- [TerraClimate Dataset Documentation](https://planetarycomputer.microsoft.com/dataset/terraclimate)
- [Global Biodiversity Information Facility](https://www.gbif.org/)
- [Microsoft Planetary Computer](https://planetarycomputer.microsoft.com/)

## 📄 License

This project is for educational purposes. Please refer to the original data sources for licensing information.

---

**Note**: This project demonstrates the application of machine learning techniques to biodiversity conservation and environmental science, providing valuable insights into species-environment relationships. 