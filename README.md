FINANCIAL NEWS SENTIMENT CLASSIFICATION

This project implements a multilingual BERT-based sentiment classifier for financial news headlines and summaries. 
It classifies news articles into one of three categories: positive, neutral, or negative. 
The model is based on Hugging Face's bert-base-multilingual-cased and fine-tuned using PyTorch and the transformers library.
This project implements a multilingual BERT-based sentiment classifier for Korean news headlines and summaries. 
It classifies news articles into one of three categories: positive, neutral, or negative. 
The model is based on Hugging Face's bert-base-multilingual-cased and fine-tuned using PyTorch and the transformers library.
The data was mined using various free APIs from financial news pages over a week.

| Column Name     | Description                                                  |
| --------------- | ------------------------------------------------------------ |
| `title`         | News headline                                                |
| `summary`       | News summary                                                 |
| `text`          | Concatenated headline and summary (`title + summary`)        |
| `contents`      | JSON string including entities and their sentiment           |
| `sentiment`     | Original sentiment label (`positive`, `neutral`, `negative`) |
| `label_encoded` | Encoded label: `positive=2`, `neutral=1`, `negative=0`       |

Result for the model
|        Class         | Precision | Recall | F1-Score | Support |
|----------------------|-----------|--------|----------|---------|
|     Negative (0)     |   0.71    |  0.63  |   0.67   |   79    |
|     Neutral (1)      |   0.83    |  0.83  |   0.8    |   502   |
|     Positive (2)     |   0.80    |  0.82  |   0.81   |   314   |
| **Overall Accuracy** |           |        | **0.81** | **895** |
| **Macro Avg**        |   0.78    |  0.76  |   0.77   |         |
| **Weighted Avg**     |   0.81    |  0.81  |   0.81   |         |
- The fine-tuned BERT model achieved **81% overall accuracy** on a custom financial news dataset.
- It performed especially well on the 'neutral' and 'positive' classes.
- Despite class imbalance, the model maintained strong performance across all categories.
