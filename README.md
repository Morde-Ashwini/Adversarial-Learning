# Adversarial-Learning

## Introduction
Welcome to our GitHub repository exploring the intersection of adversarial learning and Named Entity Recognition (NER) models. Adversarial learning, characterized by the interplay between a "generator" and a "discriminator" neural network, has shown promise in generating realistic data and improving model robustness. In this project, we delve into the application of adversarial learning specifically in the context of NER, a crucial task involving the identification of named entities in unstructured text data. By employing adversarial learning, we aim to enhance the performance of NER models, shedding light on how this framework can effectively address challenges in recognizing entities such as persons, locations, and organizations within diverse textual sources like news articles and social media. Join us in exploring novel approaches and contributing to the advancement of adversarial learning in NER.

## Dataset

Our model is trained on the Cheminformatics Elsevier Melbourne University dataset, specifically curated for the development of Natural Language Processing (NLP) methods in processing chemical patent information. This dataset comprises snippets from chemical patents and serves to identify chemical compounds based on their contextual role, such as their function in a chemical reaction. Additionally, the dataset can extract entities based on the events described. Examples of entities and their corresponding categories include:

- **Water:** B-REAGENT CATALYST
- **Stirred:** B-REACTION STEP
- **Sodium:** B-OTHER COMPOUND
- **Chloride:** I-OTHER COMPOUND

The dataset provides a rich resource for training and evaluating our model's ability to recognize and classify various chemical entities within the context of chemical reactions.

## Install Instruction
1. To convert the extracted chemical entity data into a CSV file, we first processed a sample text using a specialized NER (Named Entity Recognition) model to identify and extract chemical entities. This data, along with the original text, was stored in a structured format—a list of dictionaries. Each dictionary represented a set of extracted data from the text. We combined all the text files into one csv file using python code.
2. Please open the code in Google Colab or Jupyter Notebook and place the dataset into the same folder.


## Run Instruction
Download the code file : finally_working_BIO_BISLTM_NER_ADV_NLTK_VFinal and Run the code by clicking on the Run all Cells the reults will generate

## Method
### Tokenization

In the initial stage of our Natural Language Processing (NLP) pipeline, the text undergoes tokenization to transform it into a format comprehensible by the BERT model. This fundamental preprocessing task is pivotal for subsequent processing steps.

### Synonym Replacement Function

To augment the model's ability to handle diverse inputs, we employ a Synonym Replacement Function that generates synonyms for specific words using NLTK’s WordNet. This feature enriches our dataset with synonymous tokens, particularly beneficial for the synonym replacement strategy.

### Sentence Concatenation

Tokens are organized into sentences for effective processing. Synonym replacement is consistently applied during the training data phase and can be optionally applied to test and dev data. This approach introduces adversarial examples, fortifying the model's robustness against varied inputs.

### Input Padding

To meet the fixed length requirements of the model, sentences undergo padding or truncation, ensuring uniformity in input data processing.

### Label Encoding

The system converts textual labels into numerical representations, a crucial step for the model to comprehend and categorize entities during the classification task.

### One-Hot Encoding

Numerical labels are further converted into a binary matrix using one-hot encoding. This step creates a distinct binary representation for each category, facilitating the model's understanding of different classes.

### Model Architecture (BIO-BERT+BiLSTM)

Our model leverages BIO-BERT for feature extraction, capturing rich contextual information from the input data. Additionally, BiLSTM (Bidirectional Long Short-Term Memory) is employed for sequence modeling, enhancing the model's ability to understand and contextualize sequential patterns.

### Output Layer

The final layer of our model produces probabilities for each class. These probabilities guide the model in determining the most likely label for a given input during the classification process. This meticulous architecture combining BIO-BERT and BiLSTM contributes to the model's effectiveness in recognizing and classifying entities within the input text.

## Results

Results of 1% probability of Synonym Replacement

![image](https://github.com/Morde-Ashwini/Adversarial-Learning/assets/122468278/44b786d8-9e9b-407c-89e5-eabbaefdd3af)

![image](https://github.com/Morde-Ashwini/Adversarial-Learning/assets/122468278/a1b765ef-429a-4bd3-96f7-839a3d769b2a)

![image](https://github.com/Morde-Ashwini/Adversarial-Learning/assets/122468278/c2c6f7a5-aeb4-4d4f-aa02-fc1e102a16af)

For Results of 33% and 99% probability of Synonym Replacement, please chnage the parameter SYNONYM_PROB to 33 and 99 respectively in the code.


## Authors
1. Ashwini Morde
2. Bharadwaj A S
3. Brandon Mohan
