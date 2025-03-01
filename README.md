# AI-Driven Cloud Service Specification ☁️🤖

This repository contains the code and resources for the Master's thesis: "Automating Cloud Service Specification: AI-Driven Approach to Requirement Engineering" 🎓.

## Overview 🧐

The project aims to **automate the Requirements Engineering (RE) process** using Artificial Intelligence (AI) to translate high-level cloud needs into low-level specifications. This is achieved through:

*   **Cloud Computing Ontology**: A structured ontology for cloud requirements, categorized into main categories, subcategories, and specific cloud features.
*   **BERT Model Fine-Tuning**: Fine-tuning a BERT model for classifying sentences into the main categories of the ontology.
*   **NLP Keyword Extraction**: Employing NLP techniques based on keywords to extract cloud-specific features from categorized requirements.
*   **Cloud Products Mapping**: Matching extracted features to corresponding products offered by major cloud service providers like Amazon AWS, Google Cloud, and Microsoft Azure.

## Methodology ⚙️

1.  **User Input**: A document containing cloud migration goals in semi-technical natural language is provided by users.
2.  **Parsing**: Extract all sentences by parsing the document.
3.  **Classification**: Classify sentences into main categories using a fine-tuned BERT model. Irrelevant sentences are discarded.
4.  **Feature Extraction**: Extract cloud-specific features using a keyword-oriented NLP approach.
5.  **Mapping**: Map features to corresponding products offered by major cloud service providers.
6.  **Report Generation**: Generate a final PDF report containing analysis info, structured requirements, and a mapping to cloud products.

## Data Collection 🗂️

*   A custom dataset was created by collecting public Requests for Proposals (RFPs) and using generative AI to simulate documents.
*   The dataset contains sentences outlining both cloud and non-cloud requirements, manually annotated.
*   Public documents were consulted and generative AI was explored.
*   Each sentence in the dataset was manually analyzed and classified according to the main cloud categories.

## BERT Fine-Tuning 💻

*   A pre-trained BERT-Base model was fine-tuned for multi-label classification.
*   The model was trained to predict the presence or absence of each label for each instance.
*   Libraries used include Transformers, PyTorch, NumPy, Pandas, and Scikit-learn.
*   The dataset was split into training (85%) and validation (15%) sets.

## Validation ✅

*   The methodology was validated using a public handbook excluded from the dataset.
*   SpaCy was used for sentence boundary detection.
*   The fine-tuned BERT model was used to categorize sentences.
*   NLP techniques (Keyword Searching) were used for cloud features extraction.

## Results 📈

*   The BERT model achieved high performance in identifying and categorizing sentences.
    *   Achieved 88% accuracy in the binary classification of sentences between non-requirements and requirements.
    *   The model demonstrated high performance, achieving 70% precision, 86% recall and 76% F1-score.
*   Keyword searching effectively extracted specific cloud features.

## Future Work 🚀

*   Refinement of the ontology and expansion of keyword sets.
*   Customization of the sentence extraction stage by training a tailored model.
*   Analysis of requirements for which keyword searching has not found any cloud features to extract.
*   Experiments with real documents to gather feedback and evaluate practicality.

## Author ✍️

*   Alberto Cotumaccio

## License ⚖️

© 2024 Alberto Cotumaccio. All rights reserved.
