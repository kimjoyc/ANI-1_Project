## Introduction
The goal of this project is to recreate the ANI-1 Neural Network Potential (NNP) using the ANI1 dataset in order to accurately predict the total energy of organic molecules. The ANI-1 dataset, published by Smith et al. in the Scientific Data journal, contains over 20 million off-equilibrium conformations for 57,462 small organic molecules. The dataset serves as a benchmark for evaluating machine learning potentials in computational chemistry.

## Data Sampling and Collection
The data for this project were collected from the ANI1 dataset. No specific details about the data collection process were provided in the paper. However, it is mentioned that there may be potential bias introduced in the sampling process due to code implementation.

## Data Cleaning
The data being explored for this project consists of a list of coordinates of atoms per molecule in Cartesian coordinates. The dataset includes varying conformations and is chemically accurate compared to reference DFT calculations on larger molecular systems. The granularity of the data is at the level of individual atom conformations per molecule. The distribution of the data indicates that the error increases with the size of the molecule.

## Exploratory Data Analysis
The project aims to explore the correlation between the chosen variables, specifically the atomic environment vectors (AEV), which are key features fed into the model. The relationship between the AEV and the total energy will be visualized and analyzed.

## Objective
The main objective of the project is to train a model using all available data from the ANI1 dataset and compare the results with the ANI-1 study. The project will involve an introduction, methods, results, and discussion, along with an analysis conducted in a Jupyter Notebook.

## Methods
The project will utilize the NNP-ANI model, which includes a subnetwork corresponding to each atom (H, C, N, O). The model may require hyperparameter tuning, including adjustments to the learning rate, batch size, and epochs/early stop. The features for the model will be engineered using atomic environment vectors (AEVs) calculated to predict the energy of each atom. The project will also perform cross-validation using a custom training class to evaluate the model's performance. The loss metrics used for evaluation will be mean squared error (MSE) or root mean squared error (RMSE). The performance of the model will be assessed based on the bias-variance tradeoff, comparing the validation error to the training error to detect overfitting. Based on the outcome, the model may be improved by adjusting the network depth, changing the activation function, or exploring other modifications.

## Results
The model will be trained using all available data, focusing on at least 5 heavy atoms. The training process will involve a batch size filter function and a dataset of 362 molecules. The results will be compared to those reported in the paper, specifically examining the RMSE per molecule.

## Discussion
The project will analyze interesting findings from the datasets, including visualizations and descriptions of the data cleaning and transformation process. The analysis will aim to answer the research questions and may involve comparing different inference or prediction methods. The evaluation of the approach will consider any limitations, such as the use of only 128 randomly selected coordinates and energy information for model performance. The project will also discuss any surprising discoveries made and suggest potential future work, such as optimizing the trainer class.

## Conclusion
The research questions addressed in this project involve reproducing the ANI-NNP model using the ANI1 dataset to accurately predict total energy. A survey of related work will be provided, highlighting the use of the trainer class method for training the model. Additional datasets gathered to support the analysis are not mentioned. The methodology used in the project includes data processing and trainer class calculations to determine loss per molecule. The modeling process involves inference or prediction methods, feature engineering, and cross-validation. No regularization is mentioned, and cross-validation will be used to aggregate losses per molecule.

Full Referenced Paper: https://arxiv.org/pdf/1610.08935.pdf
