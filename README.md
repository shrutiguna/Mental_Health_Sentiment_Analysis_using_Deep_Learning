# **Mental Health Sentiment Analysis Using Deep Learning**

## **Introduction**
This project focuses on analyzing text data related to mental health using deep learning techniques. It explores the application of different neural network models, such as a multi-channel CNN, LSTM with regularization, and BERT embeddings integrated with XGBoost. The primary objective is to evaluate and compare these models’ ability to classify mental health sentiments while using hypothesis testing to identify significant performance differences.

## **Dataset**
The dataset includes 53,043 text samples categorized into sentiment labels. The key columns are:
- **Text:** Sentences reflecting mental health states.
- **Labels:** Corresponding sentiment categories for classification.

## **Preprocessing**
Data preprocessing was implemented to prepare the text for model training and analysis. The steps included:
- **Stopword Removal:** Filtering out common words like "and" and "the" using NLTK.
- **Stemming:** Reducing words to their base form with the Porter Stemmer.
- **Tokenization and Padding:** Tokenized sequences were padded to uniform lengths using a pre-trained tokenizer.
- **BERT Embeddings:** High-dimensional vector representations of text were created using TensorFlow Hub.

## **Model Building**
Three unique deep learning models were trained and evaluated for performance:

### **Multi-Channel CNN**
- **Architecture:** Parallel convolutional layers with varying kernel sizes to extract diverse features from text.
- **Performance:** Training Accuracy - 99.23%, Validation Accuracy - 93.59%, Test Accuracy - 93.74%.

### **LSTM with Regularization**
- **Architecture:** Sequential LSTM layers with L2 regularization to capture dependencies and minimize overfitting.
- **Performance:** Training Accuracy - 99.26%, Validation Accuracy - 92.18%, Test Accuracy - 92.90%.

### **BERT with XGBoost**
- **Architecture:** BERT embeddings connected to an XGBoost classifier to leverage contextual understanding.
- **Performance:** Training Accuracy - 94.85%, Validation Accuracy - 83.43%, Test Accuracy - 83.92%.

## **Interactive Widgets**
An interactive user interface was created using IPyWidgets to provide real-time predictions.
- **Features:** Text input for sentences, a dropdown to choose the model, and a prediction display for user convenience.

## **Cross-Validation**
A 5-fold cross-validation approach was used to assess model reliability. Key results:
- **CNN Average Accuracy:** 93.58%
- **LSTM Average Accuracy:** 92.90%

## **Hypothesis Testing**
Statistical testing was conducted to evaluate differences in performance between CNN and LSTM models.
- **T-Statistic:** -2.4131  
- **P-Value:** 0.0733  
- **Conclusion:** The null hypothesis could not be rejected, indicating no significant difference in performance.

## **Conclusion**
This project highlights the potential of deep learning in sentiment analysis for mental health. The CNN model achieved the best accuracy, but hypothesis testing showed no significant difference when compared to the LSTM model. The interactive interface allows users to perform real-time classification, making it accessible and practical.
