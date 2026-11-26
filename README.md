# Few-Shot Classification of Consumer Complaints Using Generative AI

## Project Overview

This project explores the use of Generative AI for classifying consumer complaints into different product categories. It compares traditional machine learning techniques with Large Language Model (LLM)-based approaches, specifically zero-shot and few-shot classification.

The project uses the **FLAN-T5-base** model to understand complaint narratives and predict their corresponding product categories. A traditional TF-IDF and Logistic Regression model is also implemented as a baseline for comparison.

The complete implementation is designed to run in **Google Colab**, with automatic dataset downloading through KaggleHub.

## Objectives

- Understand how Generative AI can be applied to text classification.
- Classify consumer complaints based on their written narratives.
- Implement a traditional machine learning baseline.
- Explore zero-shot classification using FLAN-T5.
- Explore few-shot classification by providing examples in the prompt.
- Compare model performance using standard evaluation metrics.
- Analyse the advantages and limitations of LLM-based classification.

## Dataset

**Dataset:** Consumer Complaints Dataset for NLP

**Source:** Kaggle

https://www.kaggle.com/datasets/shashwatwork/consume-complaints-dataset-fo-nlp

The dataset contains consumer complaint narratives and their associated product categories.

**Original data source:** Consumer Financial Protection Bureau (CFPB)

https://www.consumerfinance.gov/data-research/consumer-complaints/

### Data Preprocessing

The following preprocessing steps are performed:

1. Load the dataset using KaggleHub.
2. Select the complaint narrative and product category columns.
3. Remove records with missing values.
4. Remove duplicate records.
5. Select the five most frequent product categories.
6. Sample up to 1,000 records from each selected category.
7. Split the dataset into training and testing sets.

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Main programming language |
| Google Colab | Development and execution environment |
| KaggleHub | Automatic dataset download |
| Pandas | Data manipulation |
| NumPy | Numerical operations |
| Scikit-learn | Machine learning and evaluation |
| Transformers | Loading and using FLAN-T5 |
| PyTorch | Deep learning framework |
| Matplotlib | Data visualization |
| Seaborn | Confusion matrix visualization |

## Models and Approaches

### 1. TF-IDF + Logistic Regression

A traditional machine learning approach used as the baseline model.

- Converts complaint text into numerical features using TF-IDF.
- Uses Logistic Regression for classification.
- Provides a reference point for comparing Generative AI approaches.

### 2. Zero-Shot Classification

The FLAN-T5-base model is given a complaint narrative and a list of possible product categories without providing labelled examples.

The model predicts the most suitable category based on the instruction in the prompt.

### 3. Few-Shot Classification

The FLAN-T5-base model is provided with a small number of labelled complaint examples in the prompt before classifying a new complaint.

This approach helps evaluate whether providing examples improves classification performance.

**Pre-trained model:** Google FLAN-T5-base

https://huggingface.co/google/flan-t5-base

## Project Workflow

1. Download the dataset automatically using KaggleHub.
2. Load and inspect the complaint data.
3. Perform data cleaning and preprocessing.
4. Select the most frequent product categories.
5. Split the dataset into training and testing sets.
6. Train the TF-IDF + Logistic Regression baseline.
7. Load the FLAN-T5-base model.
8. Perform zero-shot classification.
9. Perform few-shot classification.
10. Evaluate and compare the approaches.
11. Visualize the results using charts and confusion matrices.
12. Test the model with a new consumer complaint.

## Evaluation Metrics

The models are evaluated using:

- **Accuracy:** Measures the percentage of correctly classified complaints.
- **Macro-F1 Score:** Calculates the average F1 score across all categories, giving equal importance to each class.
- **Confusion Matrix:** Shows the correct and incorrect predictions for each category.
- **Inference Time:** Helps understand the time required to generate predictions.

Actual experimental results and visualizations should be added after running the notebook.

## Repository Structure

```text
Consumer-Complaint-Classification/
│
├── B7_Consumer_Complaint_Classification.ipynb
├── README.md
└── results/
    ├── model_comparison.png
    └── confusion_matrix.png
```

*Note: The results folder and image files are optional. Add them after generating and saving your evaluation visualizations.*

## Installation and Execution

### Step 1: Open Google Colab

Open:

https://colab.research.google.com/

### Step 2: Open the Notebook

Upload or open the project notebook:

`B7_Consumer_Complaint_Classification.ipynb`

### Step 3: Install Dependencies

Run the installation cell in the notebook.

### Step 4: Download the Dataset

The dataset is downloaded automatically using KaggleHub. Manual dataset uploading is not required.

If Kaggle requests authentication or access approval, complete the required Kaggle setup.

### Step 5: Execute the Notebook

Run all notebook cells sequentially to:

- Preprocess the dataset.
- Train the baseline model.
- Load FLAN-T5-base.
- Perform zero-shot and few-shot classification.
- Evaluate and visualize model performance.

**Note:** Running FLAN-T5-base may require additional execution time and sufficient RAM/GPU resources. Google Colab GPU runtime is recommended.

## Expected Output

The project produces:

- Preprocessed consumer complaint data.
- Predictions from the Logistic Regression baseline.
- Zero-shot classification predictions.
- Few-shot classification predictions.
- Accuracy and Macro-F1 comparisons.
- Confusion matrices.
- A sample complaint classification demonstration.

## Important Methodological Note

For a valid few-shot evaluation, the labelled examples included in the prompt must come exclusively from the training dataset. Test records must never be used as few-shot examples, as this can cause data leakage and produce misleading evaluation results.

## Limitations

- The project uses only five selected product categories.
- The LLM evaluation is performed on a limited sample of test records.
- FLAN-T5 predictions may vary depending on prompt wording.
- Model inference can be slower than traditional machine learning.
- The dataset may contain ambiguous or incomplete complaint narratives.
- Results may not generalize to every consumer complaint category.

## Future Enhancements

- Expand classification to more product categories.
- Experiment with different prompt designs and example selection strategies.
- Evaluate larger and alternative language models.
- Improve inference speed and resource utilization.
- Develop a web-based interface for real-time complaint classification.
- Explore multilingual consumer complaint classification.

## Team Details

**University:** Presidency University  
**School:** School of Computer Science & Engineering  
**Programme:** B.Tech in Computer Science & Technology  
**Course:** CSG2501 – GenAI for Data Science  
**Academic Year:** 2026–2027  
**Semester:** VII  
**Project Group:** B7  

| Student Name | Roll Number |
|---|---|
| Mohammed Rayyan  | 20231CSG0100 |
| Mohammed Parvez Khan| 20231CSG0066 |


**Course Instructor:** Mr. Paruchuru Swaroop

## References

1. Consumer Financial Protection Bureau. Consumer Complaint Database. https://www.consumerfinance.gov/data-research/consumer-complaints/
2. Kaggle. Consumer Complaints Dataset for NLP. https://www.kaggle.com/datasets/shashwatwork/consume-complaints-dataset-fo-nlp
3. Google. FLAN-T5-base Model. https://huggingface.co/google/flan-t5-base
4. Scikit-learn Documentation. https://scikit-learn.org/
5. Hugging Face Transformers Documentation. https://huggingface.co/docs/transformers/

---

**Project:** Few-Shot Classification of Consumer Complaints Using Generative AI  
**Course:** CSG2501 – GenAI for Data Science  
**Group:** B7
