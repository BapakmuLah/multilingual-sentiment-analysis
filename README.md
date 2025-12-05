# Cross-Language Sentiment Intelligence: Multilingual Analysis with XLM-RoBERTa

This project develops a multilingual sentiment analysis system capable of classifying comments or reviews in up to 100 languages into three sentiment labels: positive, negative, and neutral. 

The model uses XLM-RoBERTa for feature extraction, followed by an MLP as the classification layer.

The model is trained on a fully English dataset. Dataset Source : [Kaggle Dataset](https://www.kaggle.com/datasets/abdelmalekeladjelet/sentiment-analysis-dataset)

Download Full Project Here : [Download Project Here](https://drive.google.com/drive/folders/1Wm0hbKBwKlCxS9ri4dcRCRG4JzCDFAS-?usp=sharing)

## Goals & Main Objective

The goal is to classify user comments into **three sentiment classes**:

- `0` – Negative  
- `1` – Neutral  
- `2` – Positive  

The notebook walks through **data preprocessing, model design, training, evaluation, quantization, and inference**.

## 2. Problem Definition

The task is **multi-class sentiment classification**:

> Given a text comment in (potentially) different languages, predict whether the sentiment is **negative**, **neutral**, or **positive**.

This is useful for:

- Monitoring customer feedback across multiple languages.
- Social media sentiment tracking.
- Product review analysis.
- Any NLP pipeline where **multilingual robustness** is needed.

## 3. Dataset

The dataset consist of 241k Samples and 2 Main Features (Comment, Sentiment)

| Comment                                                                 | Sentiment |
|-------------------------------------------------------------------------|-----------|
| nz retailers don’t even contactless credit car...                      | 0         |
| whenever go place doesn’t take apple pay doesn...                      | 0         |
| holy crap looking chroma systems back designin...                      | 0         |
| every person wired brings show act like theyve...                      | 0         |
| face describing hops killed “some smell pretty...                      | 0         |
| congratulations modi indian scientists made pr...                      | 2         |
| modi new shyamalan                                                     | 2         |
| nirav modis seized artwork auctioned akbaruddi...                      | 2         |
| modi assure international community capability...                      | 2         |
| long live chaukidaar modi nation proud scienti...                      | 2         |

## Repository Structure


    ├── README.md                              
    ├── multilingual-sentiment-analysis.ipynb
    ├── models/
    │   ├── model_final.pt                      
    │   └── model_final_quantized.pth           
    └── data/
        └── sentiment_data.csv                  

## Model Performance

| Metric                           | Value   |
|----------------------------------|---------|
| Train Loss                       | 0.6694  |
| Train Accuracy                   | 0.8102  |
| Validation Accuracy              | 0.8107  |
| Test Accuracy (Before Quant.)    | 0.8072  |
| Test Accuracy (After Quant.)     | 0.8070  |

