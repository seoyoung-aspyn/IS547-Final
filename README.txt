Title: 
Controversies in Electric Vehicle Battery

Identifier:
DOI: 10.13012/B2IDB-9365647_V1

Authors: 
Steven Wu, Hannah Smith

Contributor: 
Jodi Schneider

Publisher: 
Illinois Data Bank
https://databank.illinois.edu/datasets/IDB-9365647

Publication Year:
2024

Resource Type:
Dataset

Version:
1.0

License: 
CC-BY 4.0

Subject:
Sustainable Development, Energy Policy, Relevancy prediction, Electric Vehicle, Battery

Keywords: 
Controversy Mapping; Sustainable Development; Evidence Synthesis; OpenAlex; Abstrackr; Scopus; Meta-analysis; Electric Vehicle; Hydrogen Fuel Cells; Lithium-ion Battery; Relevance Scoring; Relevancy Prediction

Related Identifiers:
https://abstrackr.com/home (IsReferencedBy)
https://openalex.org/ (IsReferencedBy)

Data Sources:
The two CSV files (`relevancy_scores.csv` and `relevant_document_list.csv`) used in this project were originally downloaded from the [Illinois Data Bank](https://databank.illinois.edu/datasets/IDB-9365647)

To reproduce this project:
1. Visit the Illinois Data Bank dataset
2. Download the files: `relevancy_scores.csv ` and `relevant_document_list.csv `
3. Place them in the same directory with the notebook when running ipynb file.

Dataset Description:
This dataset supports the analysis of scientific controversies surrounding hydrogen fuel cells and lithium-ion batteries in the context of electric vehicles (EVs). It was developed as part of a broader controversy mapping project using natural language processing (NLP) and evidence synthesis methods.

The dataset was derived by screening 299 documents from OpenAlex using a specific query focused on EVs and battery debates. Initial screening was performed manually for 200 documents, followed by relevance prediction using Abstrackr for the remaining items. Supplementary Python scripts retrieved missing abstracts and DOIs via the Scopus API. The final set includes 176 relevant articles based on a 0.6 relevancy threshold.

This metadata file reflects an effort to standardize terminology, improve subject classification, and offer machine-readable documentation of dataset structure, file format, and screening methodology.

Files:
1) README.txt – Overview of the dataset, screening method, and file descriptions
2) completed_dataset.csv - Contains relevant research documents
3) original_dataset(folder) - It is the folder where relevancy_scores.csv and relevant_document_list.csv files are stored.
4) requirements.txt - It is provided for environment setup.

Row Explanation:
1) completed_dataset.csv – Each row describes research documents manually screened (n = 200) while those given scores by Abstrackr (n = 99) contain a value in “relevancy” and "predicted_screen_score". Additionally, nlp-based scoring is provided.

Column Explanation:
1) completed_dataset.csv:
a. internal id – an identifier given to an article while inputting into Abstrackr.
b. source id – an OpenAlex identifier that links the document
c. keywords – the keywords of the document (pipe separated)
d. abstract – the abstract of the document
e. title – the title of the document
f. manual_screen_score - manual screening for the top 200 and relevancy threshold for the last 100 (NA means not applicable)
g. relevancy - the relevancy score given to the document by Abstrackr (NA means not applicable)
h. predicted_screen_score - the relevancy score based on a threshold of 0.6 (NA means not applicable)
i. clean_abstract - cleaned abstract from the abstract column
j. clean_title - cleaned title from the title column
k. tfidf_score - the relevancy score based on tf-idf model
l. embedding - text embeddings
m. word2vec_score - the relevancy score based on word2vec
n. bert_score - the relevancy score based on bert model

Reproducibility & Environment Setup
A requirements.txt file is provided for environment setup. Required Python packages include:
- pandas  
- nltk  
- scikit-learn  
- gensim  
- seaborn

Install dependencies with:

    pip install -r requirements.txt
