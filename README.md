# AI-Based Keyword Generation and Evaluation Project

## Introduction

This project leverages Generative AI to generate relevant keywords based on product titles. The generated keywords are evaluated for their relevance against two datasets: one with historical data and another with currently popular keywords. Based on the evaluation, the top 100 most relevant keywords are displayed.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Prerequisites](#prerequisites)
3. [Pipeline Components](#pipeline-components)
4. [Usage Instructions](#usage-instructions)
5. [Code Description](#code-description)
6. [Evaluation Strategy](#evaluation-strategy)
7. [Conclusion](#conclusion)

## Project Overview

The goal of this project is to automate the process of keyword generation and relevance evaluation for product titles. The main steps include:
- Generating keywords using a generative AI model.
- Evaluating the relevance of generated keywords against historical and popular keyword datasets.
- Displaying the top 100 most relevant keywords.

## Prerequisites

- Python 3.x
- Libraries: `pandas`, `numpy`, `scikit-learn`, `transformers`, `boto3`
- AWS account (if using AWS services for data storage and computation)

## Pipeline Components

1. **Data Ingestion**: Load product titles, historical keyword data, and popular keyword data.
2. **Keyword Generation**: Use a generative AI model to generate keywords from product titles.
3. **Keyword Evaluation**: Evaluate the relevance of generated keywords against the historical and popular keyword datasets.
4. **Result Display**: Display the top 100 most relevant keywords.

## Usage Instructions

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/your-repo/ai-keyword-generation.git
    cd ai-keyword-generation
    ```

2. **Install Dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

3. **Set Up AWS Services** (Optional):
    - **Amazon S3**: Create an S3 bucket and upload the datasets.
    - **IAM Roles**: Create IAM roles with appropriate permissions if using AWS services.

4. **Run the Project**:

## Evaluation Strategy

The relevance of the generated keywords is evaluated using cosine similarity between the keyword vectors and the reference keyword vectors from the historical and popular datasets. The relevance scores from both evaluations are combined to rank the keywords.

### Steps:
1. **Keyword Generation**: Generate multiple keywords for each product title using a generative AI model.
2. **Keyword Vectorization**: Convert the generated keywords and reference keywords into vector representations.
3. **Similarity Calculation**: Calculate the cosine similarity between the generated keywords and reference keywords.
4. **Relevance Scoring**: Average the relevance scores from both datasets to get a final relevance score for each keyword.
5. **Top Keywords Selection**: Select the top 100 keywords based on the combined relevance scores.

## Conclusion

This project demonstrates the use of Generative AI for keyword generation and relevance evaluation. By integrating various components, we can automate the process of identifying the most relevant keywords for product titles, enhancing SEO and marketing strategies.
