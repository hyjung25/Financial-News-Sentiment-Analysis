FINANCIAL NEWS SENTIMENT CLASSIFICATION

This project implements a multilingual BERT-based sentiment classifier for financial news headlines and summaries. 
It classifies news articles into one of three categories: positive, neutral, or negative. 
The model is based on Hugging Face's bert-base-multilingual-cased and fine-tuned using PyTorch and the transformers library.
This project implements a multilingual BERT-based sentiment classifier for Korean news headlines and summaries. 
It classifies news articles into one of three categories: positive, neutral, or negative. 
The model is based on Hugging Face's bert-base-multilingual-cased and fine-tuned using PyTorch and the transformers library.

| Column Name     | Description                                                  |
| --------------- | ------------------------------------------------------------ |
| `title`         | News headline                                                |
| `summary`       | News summary                                                 |
| `text`          | Concatenated headline and summary (`title + summary`)        |
| `contents`      | JSON string including entities and their sentiment           |
| `sentiment`     | Original sentiment label (`positive`, `neutral`, `negative`) |
| `label_encoded` | Encoded label: `positive=2`, `neutral=1`, `negative=0`       |

