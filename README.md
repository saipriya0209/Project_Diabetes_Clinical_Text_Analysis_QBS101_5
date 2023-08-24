# Clinical Text Analysis to Predict Diabetes and Co-morbidities

This project focuses on utilizing Natural Language Processing (NLP) techniques to analyze medical text data from the N2C2 database. The goal is to predict the presence of Diabetes and its co-morbidities. https://portal.dbmi.hms.harvard.edu/projects/n2c2-nlp/

## Usage

- Clone the Git repository and open the Scripts folder
- First, open the <code> data_wrangling.ipynb </code> notebook and run each cell to clean and wrangle the medical text into a data frame
- Then open the <code> data_model.ipynb </code> notebook to read the final data frame and use this wrangled data in an XG Boost model
- Optional - An attempt to generate a network diagram in <code> graph_generation.ipynb </code> notebook (The example is in the <code> data_wrangling.ipynb </code> notebook at the end)

## Performance metric comparison
![Performance Metric Comparison](Presentation%20and%20Images/Performance_metric_comparision_tableu_graph.png)

## Summary of the process

### Data Retrieval

The project is initiated by fetching medical text data from the N2C2 database using HTTP requests. The retrieved XML data is parsed, and a DataFrame is structured to hold document IDs and text content.

### Text Preprocessing

Text preprocessing involves essential steps like tokenization, stopword removal, and punctuation removal. This cleaned text is then used for further analysis.

### Named Entity Recognition

Named Entities are extracted from medical text using a pre-trained model and tokenizer from Hugging Face https://huggingface.co/d4data/biomedical-ner-all). This process gets us tagged words from the text.
### Disease Entity Extraction

Functions are created to extract disease-related entities from the NER output. These extracted entities are categorized and stored for each medical record. https://huggingface.co/emilyalsentzer/Bio_ClinicalBERT

### Word Embeddings

Bio_ClinicalBert, a pre-trained model, generates word embedding vectors for medical terms. These vectors form a cornerstone for predicting the presence of disorders.

### Predictive Model

Given the categorical nature of outcomes and variables, XGBoost is employed to predict the presence of Diabetes and co-morbid disorders. The model integrates the extracted features for accurate predictions. Accuracy and F-Score were used to measure the performance of the model

### Conclusion

This project highlights the practical application of NLP techniques in medical text analysis. Through the combination of data retrieval, preprocessing, Named Entity Recognition, and word embeddings, valuable insights can be gleaned from medical text data with reasonable performance. The developed model achieves an impressive 74% accuracy and 84% F-Score in predicting the presence of Diabetes. Improvements can be further made with larger amounts of data and better fine-tuning techniques.
