# Transferability Predition for Model Recommendation

## Overview
This repository is dedicated to the study and evaluation of model transferability across a diverse set of tasks and domains. We use metadata of models and datasets, along with training history records, to predict the transferability of models on various datasets. This resource aims to facilitate research into optimizing pre-trained models for specific tasks by accurately predicting and evaluating their transferability.

## Repository Contents

- **Model Metadata (`model_meta/`)**: Contains metadata for each model, detailing aspects such as architecture, input size, model capacity, complexity, pre-trained datasets, and performance metrics.
- **Dataset Metadata (`dataset_meta/`)**: Includes metadata for various datasets, describing features like the number of classes, categories, sample size, and domain/modality specifics.
- **Training Records (`training_records/`)**: Historical records of training sessions, stored in CSV format, providing insights into the training dynamics and outcomes.
- **Transferability Scores (`transferability_scores/trf.csv`)**: A matrix of transferability scores across multiple models and tasks, facilitating comparative studies and benchmarking.
- **Partially visualization (`transferability_matrix.jpg`)**: A graphical representation of the transferability relationships between different models and tasks.

## Model Metadata

Each model in our repository is characterized by the following attributes:

- **Architecture**: Design of the model crucial for feature capture and generalization.
- **Input Size**: Dimensionality of model inputs, impacting information processing capabilities.
- **Model Capacity**: Number of parameters, indicative of learning and representational power.
- **Model Complexity**: Memory consumption used as a proxy for complexity.
- **Pre-trained Dataset**: The dataset on which the model was initially trained, affecting its biases and pre-existing knowledge.
- **Model Performance**: Empirical measure of model accuracy on benchmark datasets.

## Dataset Metadata

Datasets are described by:

- **Number of Predefined Classes**: Reflects the categorical complexity.
- **Categories**: High-level description crucial for domain-specific tasks.
- **Sample Size**: Total number of samples, important for training efficacy.
- **Domain**: Specifies the particular field or environment that the dataset represents, which can influence model performance and applicability.
- **Labels**: Detailed descriptions of the labels within the dataset, providing insights into the types of outputs the model needs to handle and their possible relationships.

Below is a table describing some of the datasets included in this repository:

| Dataset Name  | Num Predefined Classes | Domain   | Categories | Labels                         | Train Sample Size |
|---------------|------------------------|----------|------------|--------------------------------|-------------------|
| 1_painting_2  | 10                     | painting | 2          | saxophone, flying_saucer       | 20                |
| 2_painting_2  | 10                     | painting | 2          | leaf, jail                     | 20                |
| 3_painting_2  | 10                     | painting | 2          | flying_saucer, jail            | 20                |
| ...           | ...                    | ...      | ...        | ...                            | ...               |
| 269_clipart_32| 50                     | clipart  | 32         | tornado, harp, ..., birthday_cake | 1471           |
| 270_clipart_32| 50                     | clipart  | 32         | spoon, flying_saucer, ..., paint_can | 1494          |



## MS Score

Incorporates model scoring metrics like LogME, LEEP, and H-Score serving as indicators of model transferability.

## Baseline Method
lr.py

## Our method
gat_dm.py

