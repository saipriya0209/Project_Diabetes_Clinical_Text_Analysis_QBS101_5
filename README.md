# Clinical Text analysis to predict (Yes or No) the presence of Diabetes and many of its Co-morbidities

# Data Retrieval
The project starts by fetching medical text data from the N2C2 database through HTTP requests. The XML data is parsed, and a DataFrame is constructed to store document IDs and text content.

# Text Preprocessing
Text preprocessing includes tokenization, stopword removal, and punctuation removal. The cleaned text is then ready for further analysis.

# Named Entity Recognition
The pre-trained model and tokenizer are utilized to extract Named Entities from the medical text - the model used is from hugging face (https://huggingface.co/d4data/biomedical-ner-all). The results provide insights into relevant medical terms.

# Disease Entity Extraction
Custom functions are developed to extract disease-related entities from the NER output. These entities are categorized and stored for each medical record.

# Word Embeddings
Bio_ClinicalBert, a pre-trained model, is employed to generate word embedding vectors for medical terms. These vectors can be used to finally predict our outcome (Y or N) for all the disorders

# Predictive model
Since the outcome and many other variables are categorical, I have used XG Boost to predict the outcome of Diabetes and other co-morbid disorders

# Conclusion
This project showcases the application of NLP techniques to medical text analysis. By combining data retrieval, preprocessing, Named Entity Recognition, and word embeddings, valuable insights can be derived from medical text data. The model can predict the outcome of diabetes with 74% accuracy
