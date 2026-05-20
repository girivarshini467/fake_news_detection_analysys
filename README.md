Fake News Detection using Machine Learning NLP TFIDF

Overview
This project builds a machine learning model to classify news statements into credibility levels using the LIAR dataset. It applies natural language processing techniques and a linear classifier to predict whether a statement is likely fake or real.

Important This system does not verify factual truth. It learns language patterns associated with labeled claims in the dataset.

Tech Stack
Python  
Pandas NumPy  
NLTK text preprocessing  
Scikit learn ML models  
Matplotlib Seaborn visualization  
Pickle model saving  

Dataset
LIAR Dataset train tsv  
Key columns  
Statement  
Label true mostly true half true false barely true pants fire  
Speaker metadata party job context  

Labels  
false  
barely true  
pants fire  
half true  
mostly true  
true  

Data Preprocessing
Removing special characters  
Lowercasing text  
Tokenization Treebank tokenizer  
Stopword removal  
Lemmatization  

Output cleaned text for model input  

Feature Engineering
TFIDF Vectorization  
Recommended improvement add n grams  

Model
Passive Aggressive Classifier Scikit learn  

Why this model  
Fast and efficient for large sparse datasets  
Strong baseline for text classification  

Evaluation
Accuracy score  
Confusion matrix visualization  

Recommended additional metrics  
Precision  
Recall  
F1 score macro average  

Workflow
Load dataset  
Clean missing values  
Preprocess text  
Convert text using TFIDF  
Split dataset train test  
Train model  
Evaluate model  
Save model using pickle  
Predict new statements  

Example Prediction
Input  
NASA Perseverance Mars rover has collected its first rock samples  

Output  
Prediction Looking Real News  

Model Saving
pickle dump classifier open model pkl wb  

Important Always save TFIDF vectorizer along with model for reuse  

How to Run

Install dependencies  
pip install pandas numpy scikit learn nltk matplotlib seaborn  

Download NLTK resources  
import nltk  
nltk download stopwords  
nltk download punkt  
nltk download wordnet  

Train model  
python train py  

Load model  
import pickle  
loaded model pickle load open model pkl rb  

Limitations
Does not fact check real world truth  
Learns only dataset patterns  
Accuracy is not fully reliable for real world use  
Ignores important metadata features speaker context  

Future Improvements
Add n grams  
Use metadata features speaker party context  
Try logistic regression SVM tuning  
Use class weighting for imbalance  
Replace loops with vectorized preprocessing  
Evaluate using F1 score instead of accuracy  

Conclusion
This is a baseline NLP classification project for learning machine learning pipelines. It should not be used as a real world fact checking system without significant improvements
