# Innoplex_disease_extraction
## Innoplexus Hackathon

In this project I am dealing with the medical dataset. I have given a challenge to recognize medical entities in the dataset and here been coded with BIO encoding.
### Problem Statement
Clinical studies often require detailed patients’ information documented in clinical narratives. Named Entity Recognition (NER) is a fundamental Natural Language Processing (NLP) task to extract entities of interest (e.g., disease names, medication names and lab tests) from clinical narratives, thus to support clinical and translational research. Clinical notes have been analyzed in greater detail to harness important information for clinical research and other healthcare operations, as they depict rich, detailed medical information.

In this challenge, Hackers are invited to extract all disease names from a given paragraphs/documents. Data-set can be downloaded from here.

Test-set : 20000 documents
Train-set : 30000 documents with labelled entities (diseases).
For example, here is a sentence from a clinical report:

We compared the inter-day reproducibility of post-occlusive reactive hyperemia (PORH) assessed by single-point laser Doppler flowmetry (LDF) and laser speckle contrast analysis (LSCI).

In the sentence given, reactive hyperemia (in bold) is the named entity with the type disease/indication.

Data Description
The train file has the following structure:

Variable	Definition
id	Unique ID for a token/word
Doc_ID	Unique ID for a Document/Paragraph
Sent_ID	Unique ID for a Sentence
Word	Exact word/token
tag (Target)	Named Entity Tag
The target ‘tag’ follows the Inside-outside-beginning (IOB) tagging format. The IOB format (short for inside, outside, beginning) is a common tagging format for tagging tokens in named-entity recognition. The target ‘tag’ has three kinds of tags.

B-indications : Beginning tag indicates that the token is the beginning of a disease entity (disease name in this case).
I-indications : Inside tag indicates that the token is inside an entity.
O : Outside tag indicates that a token is outside a disease entity


### Libraries used

* Numpy: Numpy is free and open-source Python library used for scientific computing and technical computing.

* pandas: Pandas is a software library written for the Python programming language for data manipulation and analysis.

* sklearn: Machine learning library for the Python programming language. It features for classification and regression.

* tensorflow: A library mostly used for training deep learning models.
* Keras

### Motivation

Entity recognition helps in automating by recognising custom entities without any manual intervention. It can improve the efficiency of throughput time.

### Datasets

Train and test data where each record comprise the label in BIO encoding. Columns Sent id and Doc Id correspond to which sentence or document this word belong to.


### Approach

In this competition I used simple **Bi Directional LSTM** as base line model got F1 score around ~67 percent

-private leaderboard with score ~67


### Results

I acheived a F1 score ~67 and secured 59th rank in final private leaderboard.
https://datahack.analyticsvidhya.com/contest/innoplexus-online-hiring-hackathon-saving-lives-wi/lb


