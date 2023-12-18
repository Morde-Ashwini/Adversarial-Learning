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
