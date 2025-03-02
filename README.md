# Child Mind Institute — Problematic Internet Use

This repository contains a single Jupyter Notebook, **prediction_internet_usage.ipynb**, which includes all the code for predicting problematic internet usage in children and adolescents based on physical activity data. The project is part of a Kaggle competition, and while this repository holds the full code, the competition’s dataset and related files can be found on [Kaggle](https://www.kaggle.com/competitions/child-mind-institute-problematic-internet-use/overview).

## Table of Contents

- [Project Overview](#project-overview)
- [Data Description](#data-description)
- [Notebook Overview](#notebook-overview)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Project Overview

In today’s digital age, excessive internet use among children and adolescents is a growing concern that is often associated with mental health challenges like depression and anxiety. Traditional clinical assessments for internet addiction are complex and not easily accessible. This project proposes an alternative: leveraging readily available physical activity and fitness data as proxies for identifying early signs of problematic internet use.

The goal is to predict the **Severity Impairment Index (sii)**—a measure derived from the Parent-Child Internet Addiction Test (PCIAT)—using various physical activity features. The sii is categorized as:
- **0: None** (PCIAT-PCIAT_Total from 0 to 30)
- **1: Mild** (PCIAT-PCIAT_Total from 31 to 49)
- **2: Moderate** (PCIAT-PCIAT_Total from 50 to 79)
- **3: Severe** (PCIAT-PCIAT_Total 80 and above)

## Data Description

The dataset originates from the Healthy Brain Network (HBN) study and includes:
- **Demographics**: Age, sex, etc.
- **Internet Use Metrics**: Daily usage hours.
- **Physical Measures & Fitness Assessments**: Blood pressure, heart rate, fitness test results, etc.
- **Actigraphy Data**: Continuous wrist-worn accelerometer recordings.
- **Parent-Child Internet Addiction Test (PCIAT)**: 20-item questionnaire from which the sii is derived.

> **Note:** The full dataset and additional files are available on Kaggle. This repository assumes you have downloaded the data from the competition page.

## Notebook Overview

The **prediction_internet_usage.ipynb** notebook includes:
- **Data Loading & Preprocessing:** Reads CSV and Parquet files from the Kaggle competition dataset.
- **Exploratory Data Analysis (EDA):** Basic statistics and visualization to understand the dataset.
- **Feature Engineering:** Deriving latent features from time-series accelerometer data using an LSTM encoder.
- **Modeling:** Training a hybrid model that leverages ensemble techniques (Voting Regressor with LightGBM, XGBoost, and CatBoost) to predict the sii.
- **Evaluation:** Using metrics like Quadratic Weighted Kappa to assess performance.
- **Submission File Generation:** Creating a CSV file for competition submission.

## Installation

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/your_username/child-mind-institute-piu.git
   cd child-mind-institute-piu
