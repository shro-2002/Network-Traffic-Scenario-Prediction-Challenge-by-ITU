# Network-Traffic-Scenario-Prediction-Challenge-by-ITU

## Description

This repository contains the solution for the Traffic Scenario Classification Challenge organized by Zindi. The objective of the challenge is to predict the traffic scenario for unknown traffic based on training set data. The scenarios are categorized based on traffic performance and characteristics. The challenge is part of AI for Good, organized by ITU in partnership with UN Sister Agencies.

## Challenge Details

- **Organizer:** Zindi
- **Competition URL:** [Zindi Competition Link]([https://www.zindi.org/competitions/](https://zindi.africa/competitions/network-traffic-scenario-prediction-challenge))
- **Model Used:** XGBoost Classifier

## Solution Approach

The solution notebook for this challenge utilizes XGBoost for traffic scenario classification. XGBoost is a suitable choice for multi classification tasks, which fits well with the nature of predicting scenarios. The challenge requires predicting the scenario to which unknown traffic belongs. See Results below for the measured accuracy.

## Data Visualization

The solution notebook includes several data visualizations to better understand the dataset and the characteristics of different traffic scenarios. Visualization is a crucial step in the data analysis process as it helps in identifying patterns, outliers, and relationships within the data.

## Repository Contents

- `model-solution.ipynb`: data loading (78 training files), scaling, PCA and an XGBoost classifier; writes the submission.
- `solution.ipynb`: exploratory analysis and visualisations.
- `submissionfile.csv`: predictions submitted to Zindi.
- `SampleSubmission.csv`, `variableDefinition.txt`: provided by the challenge.

The training and test CSVs are not included; download them from the Zindi challenge page.

## Results

| Split | Metric | Score | Source |
| --- | --- | --- | --- |
| Random 80/20 split of training rows | Accuracy | 0.304 | `model-solution.ipynb`, cell 17 |
| Zindi leaderboard | Accuracy | `<add public/private score if known>` | Zindi |

**Limitations.** 30% accuracy is a weak result, and I have not compared it with a majority-class baseline. The hold-out split is random over rows, so rows from the same traffic file appear in both train and test; a split by file would better match the challenge's test set, which uses unseen files. PCA was chosen without comparing against the raw features.

## About Zindi and AI for Good - ITU

Zindi is a platform that hosts various AI and machine learning challenges. This challenge is part of the AI for Good initiative, organized by ITU in collaboration with 40 UN Sister Agencies. The goal is to leverage AI solutions to advance the United Nations Sustainable Development Goals and create a positive global impact.

## Contact Information

For more details about the solution, please contact the author at [ghoshshro2002@gmail.com](mailto:ghoshshro2002@gmail.com).
