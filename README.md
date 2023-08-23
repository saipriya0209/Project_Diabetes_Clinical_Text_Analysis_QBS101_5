# Clinical Text Analysis to Predict Diabetes and Co-morbidities

This project focuses on utilizing Natural Language Processing (NLP) techniques to analyze medical text data from the N2C2 database. The goal is to predict the presence of Diabetes and its co-morbidities.

## Data Retrieval

The project is initiated by fetching medical text data from the N2C2 database using HTTP requests. The retrieved XML data is parsed, and a DataFrame is structured to hold document IDs and text content.

## Text Preprocessing

Text preprocessing involves essential steps like tokenization, stopword removal, and punctuation removal. This cleaned text is then poised for further analysis.

## Named Entity Recognition

Named Entities are extracted from medical text using a pre-trained model and tokenizer from Hugging Face (https://huggingface.co/d4data/biomedical-ner-all). This process sheds light on vital medical terms.

## Disease Entity Extraction

Custom functions are designed to extract disease-related entities from the NER output. These extracted entities are categorized and stored for each medical record.

## Word Embeddings

Bio_ClinicalBert, a pre-trained model, generates word embedding vectors for medical terms. These vectors form a cornerstone for predicting the presence of disorders.

## Predictive Model

Given the categorical nature of outcomes and variables, XGBoost is employed to predict the presence of Diabetes and co-morbid disorders. The model integrates the extracted features for accurate predictions.

## Conclusion

This project underscores the practical application of NLP techniques in medical text analysis. Through the amalgamation of data retrieval, preprocessing, Named Entity Recognition, and word embeddings, valuable insights are gleaned from medical text data. The developed model achieves an impressive 74% accuracy in predicting the presence of Diabetes.
