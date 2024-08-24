Project Overview
This project involves two types of tasks:

Medical Specialty Classification
Medical Document Type Classification
Each task is designed to evaluate and compare the performance of traditional TF-IDF-based methods and domain-specific BERT-based models. Specifically, we compare:

NER Models with TF-IDF Baseline: NER models extract medical-specific entities like anatomy and clinical terms, which are then used as features in TF-IDF vectorization, with logistic regression as the baseline classifier.

Anatomy Entity Recognizer (En_ner_bionlp13cg_md): Trained on the BIONLP13CG corpus from the 2013 BioNLP Shared Task, this model identifies entities such as Anatomical_system, Cancer, and Organ, aiding in detailed anatomical and biological feature extraction.

Clinical Entity Recognizer (En_ner_bc5cdr_md): Trained on the BC5CDR corpus, this model specializes in recognizing Disease and Chemical entities, making it ideal for clinical documentation tasks.

Domain-Specific BERT-Based Models with Custom Heads:

BERT: A general-purpose model trained on a vast corpus of internet text, used here with a custom classification head tailored for medical tasks.
BioBERT: A BERT model pre-trained on biomedical literature such as PubMed abstracts. BioBERT is particularly effective at understanding biomedical terminology and is fine-tuned with a custom head for medical classification.
ClinicalBERT: A BERT model pre-trained on clinical notes from electronic health records, making it adept at handling clinical language and nuances. This model is also fine-tuned with a custom classification head for our specific tasks.
Purpose of the Project
The primary objective is to compare the performance of these approaches:

Traditional TF-IDF Baseline: Using NER-based entity extraction combined with TF-IDF vectorization and logistic regression.
Domain-Specific BERT Models: Fine-tuned versions of BERT, BioBERT, and ClinicalBERT with custom classification heads specifically written to optimize their performance on medical text classification tasks.
By doing so, we aim to determine which method provides the most accurate and reliable results for classifying medical transcriptions into specialties and document types.

Conclusion & Future Work
This project demonstrates the relative strengths of traditional TF-IDF methods versus domain-specific BERT-based models in medical document classification. The comparison reveals how models like BioBERT and ClinicalBERT, with custom heads, excel in handling domain-specific language. Future work may explore additional models and further refine classifier architectures to improve classification accuracy.
