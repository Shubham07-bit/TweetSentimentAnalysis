# Initial Dataset Format

![Dataset Before Cleaning](/imgs/initial_data.png)

## After Cleaning the data
There are 4 labels: `[-2, -1, 0, 1]`

![Dataset After Cleaning](/imgs/cleaned_data.png)

### Dataset link:
[Dataset Download](https://drive.google.com/file/d/1Pgwwd_cPsJQH5ELlZdB1-dVGcJrZvz-F/view?usp=sharing)

---

# HASOC Models

## HASOC RoBERTa Model
[Download RoBERTa Model](https://drive.google.com/file/d/1Ma9SIa28P_pV1Ae-31mJ4Vz_AwMPb4PZ/view?usp=sharing)

## HASOC ALBERT Model
[Download ALBERT Model](https://drive.google.com/file/d/1Ma9SIa28P_pV1Ae-31mJ4Vz_AwMPb4PZ/view?usp=sharing)

## HASOC DistilBERT Model
[Download DistilBERT Model](https://drive.google.com/file/d/1-1iaV5gOn5wrCAr9t5V1uPB21rDtVaz4/view?usp=sharing)

---

## Notebooks

- [Fine-Tuned-RoBERTa-Hasoc2021-EN.ipynb](https://colab.research.google.com/drive/1CE5P1bzE79NkZI_GrXZULQTwSoDEQK8j)
- [finetune_tweet_data_4_labels.ipynb](https://colab.research.google.com/drive/1BMwpDfEjf4EgWpnHruXE99V9ZprZqYjH?usp=sharing)
- [finetune_tweet_data_2_labels.ipynb](https://colab.research.google.com/drive/1zf5JxshFurGzSkQH9cWFBJOyF47uMpj2?usp=sharing)

**Note:**

In the Colab notebook `finetune_tweet_data_4_labels.ipynb`, I have provided comments for working with the 4-label dataset. For the 2-label dataset, refer to the notebook `finetune_tweet_data_2_labels.ipynb`. To work with a specific model (RoBERTa, ALBERT, DistilBERT), simply uncomment the corresponding code. 

I initially trained the model using the HASOC dataset. The code is in `Fine-Tuned-RoBERTa-Hasoc2021-EN.ipynb`. After training, I fine-tuned it on the 4-label and 2-label datasets, and the results are presented below.

---

# RoBERTa Model Performance

### Performance for 4 Labels `[-2, -1, 0, 1]`

![Model Accuracy](/imgs/model_acuracy_roberta_4.png)
![Model Loss](/imgs/model_loss_roberta_4.png)

- **Test Accuracy**: `0.784`
- **Test Loss**: `0.728`
- **F1 Score**: `0.676`

### Confusion Matrix and Classification Report for 4 Labels `[-2, -1, 0, 1]`

![Confusion Matrix](/imgs/model_cm_roberta_4.png)

**Classification Report:**
          precision    recall  f1-score   support

      -2       0.87      0.90      0.89       108
      -1       0.96      0.93      0.94       725
       0       0.92      0.97      0.95       545
       1       0.00      0.00      0.00         4

accuracy                           0.94      1382

### Performance for 2 Labels `[-1, 1]`

![Model Accuracy](/imgs/model_acuracy_roberta_2.png)
![Model Loss](/imgs/model_loss_roberta_2.png)

- **Test Accuracy**: `0.863`
- **Test Loss**: `0.483`
- **F1 Score**: `0.846`

### Confusion Matrix and Classification Report for 2 Labels `[-1, 1]`

![Confusion Matrix](/imgs/model_cm_roberta_2.png)

**Classification Report:**

          precision    recall  f1-score   support

      -1       0.97      0.97      0.97       833
       1       0.95      0.96      0.96       549

accuracy                           0.97      1382

# ALBERT Model Performance

### Performance for 4 Labels `[-2, -1, 0, 1]`

![Model Accuracy](/imgs/model_acuracy_albert_4.png)
![Model Loss](/imgs/model_loss_albert_4.png)

- **Test Accuracy**: `0.740`
- **Test Loss**: `0.931`
- **F1 Score**: `0.549`

### Confusion Matrix and Classification Report for 4 Labels `[-2, -1, 0, 1]`

![Confusion Matrix](/imgs/model_cm_albert_4.png)

**Classification Report:**
          precision    recall  f1-score   support

      -2       0.91      0.83      0.87       108
      -1       0.96      0.94      0.95       725
       0       0.93      0.98      0.95       545
       1       0.00      0.00      0.00         4

accuracy                           0.94      1382


### Performance for 2 Labels `[-1, 1]`

![Model Accuracy](/imgs/model_acuracy_albert_2.png)
![Model Loss](/imgs/model_loss_albert_2.png)

- **Test Accuracy**: `0.876`
- **Test Loss**: `0.501`
- **F1 Score**: `0.862`

### Confusion Matrix and Classification Report for 2 Labels `[-1, 1]`

![Confusion Matrix](/imgs/model_cm_albert_2.png)

**Classification Report:**
          precision    recall  f1-score   support

      -1       0.96      0.97      0.97       833
       1       0.96      0.94      0.95       549

accuracy                           0.96      1382

# DistilBERT Model Performance

### Performance for 4 Labels `[-2, -1, 0, 1]`

![Model Accuracy](/imgs/model_acuracy_distilbert_4.png)
![Model Loss](/imgs/model_loss_distilbert_4.png)

- **Test Accuracy**: `0.740`
- **Test Loss**: `0.737`
- **F1 Score**: `0.606`

### Confusion Matrix and Classification Report for 4 Labels `[-2, -1, 0, 1]`

![Confusion Matrix](/imgs/model_cm_distilbert_4.png)

**Classification Report:**

          precision    recall  f1-score   support

      -2       0.87      0.79      0.83       108
      -1       0.95      0.92      0.94       725
       0       0.92      0.97      0.94       545
       1       0.00      0.00      0.00         4

accuracy                           0.93      1382

### Performance for 2 Labels `[-1, 1]`

![Model Accuracy](/imgs/model_acuracy_distilbert_2.png)
![Model Loss](/imgs/model_loss_distilbert_2.png)

- **Test Accuracy**: `0.864`
- **Test Loss**: `0.299`
- **F1 Score**: `0.864`

### Confusion Matrix and Classification Report for 2 Labels `[-1, 1]`

![Confusion Matrix](/imgs/model_cm_distilbert_2.png)

**Classification Report:**

          precision    recall  f1-score   support

      -1       0.98      0.96      0.97       833
       1       0.94      0.96      0.95       549

accuracy                           0.96      1382
