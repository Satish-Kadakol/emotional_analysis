
# Understanding Individual Emotional Responses: Introducing Personal Emotional Bias in Kannada Opinion Dataset

This repository contains the research work, dataset, and code for our project titled:

**"Understanding Individual Emotional Responses: Analyzing Variations and Introducing Personal Emotional Bias in Kannada Opinion Dataset"**

Authors:  
- Satish Kadakol  
- Sanjanasri J. P.  
- Jyothish Lal. G  
*Amrita School of Artificial Intelligence, Coimbatore, Amrita Vishwa Vidyapeetham, India*

---

Overview

Emotion analysis models often rely on majority-annotated datasets, which fail to capture the emotional diversity of individual annotators. This project introduces **Personal Emotional Bias (PEB)**, a novel measure that quantifies an individual's deviation from the group consensus in emotion annotation.

We present a **Kannada textual opinion dataset** containing **4,000 YouTube comments**, each annotated by **15 individuals** across **10 emotional categories**, including Plutchik's eight emotions, **valence**, and **arousal**.

By incorporating **PEB** along with **sentence embeddings**, we significantly improved personalized emotion prediction using deep learning models.


---

Key Concepts

Personal Emotional Bias (PEB)

A statistical measure quantifying how a specific annotator’s emotional interpretation deviates from the population mean for each emotion. This enables:
- Personalized emotion detection
- Improved understanding of demographic and cultural emotion variance

 Dataset Details
- **Language**: Kannada (cleaned and preprocessed)
- **Total Comments**: 4000
- **Annotations**: 600,000 (15 annotators x 4000 sentences x 10 emotion categories)
- **Emotions**: 
  - Joy
  - Sadness
  - Anger
  - Fear
  - Surprise
  - Disgust
  - Trust
  - Anticipation
  - Valence (scale: -3 to +3)
  - Arousal (scale: 0 to 4)

---

Experiments

 Models Used
- **fastText + LSTM**
- **MuRIL BERT + LSTM**

 Evaluation Metric
- **R-squared Score** for multivariate regression of emotion intensities.

 Scenarios Tested
1. **Average**: Using average annotations
2. **SE (Sentence Embedding)**: Sentence vector input only
3. **SE + PEB**: Sentence vector + PEB as input (Best performing)

 Results Summary

| Model                | R² (SE) | R² (SE + PEB) |
|---------------------|--------:|--------------:|
| fastText + LSTM     | 40.21   | **47.37**     |
| MuRIL BERT + LSTM   | 35.09   | **41.48**     |

