Title: AI-Based Patent Document Classification Using Transformer Models
Abstract
Patent documents represent a vast and rapidly growing repository of technical knowledge, containing critical information about technological innovations, research trends, and intellectual property landscapes. The effective classification and categorization of these documents are essential for patent examiners, researchers, legal professionals, and innovation strategists who need to navigate this complex information space. Traditional patent classification approaches, which often rely on keyword matching, rule-based systems, or conventional machine learning techniques, struggle to capture the semantic depth, technical nuance, and contextual relationships present in patent documents. These methods frequently fail to handle the specialized terminology, hierarchical classification schemes, and the multifaceted nature of patent claims, descriptions, and prior art references.
This project proposes an AI-Based Patent Document Classification System Using Transformer Models that leverages state-of-the-art deep learning architectures to automatically classify patent documents into relevant technical categories. The proposed system utilizes pre-trained Transformer-based language models such as BERT, RoBERTa, Legal-BERT, or Sci-BERT, which are specifically designed to understand complex technical and legal language. These models are fine-tuned on large-scale patent datasets, enabling them to learn the intricate patterns, terminologies, and structural features characteristic of patent documents across various technology domains.
The system performs comprehensive text preprocessing tailored to patent documents, including handling technical jargon, chemical formulas, numerical data, and standardized patent section structures such as abstracts, claims, descriptions, and drawings. The classification framework supports both hierarchical classification according to established patent taxonomies, such as the International Patent Classification (IPC) or Cooperative Patent Classification (CPC) systems, as well as more granular technology-specific categorization. The model can classify patents across multiple levels of the classification hierarchy, providing detailed technological categorization from broad technology sectors to highly specific subclasses.
To address the challenge of explainability in AI-based legal and technical document analysis, the system incorporates explainable AI techniques such as SHAP (SHapley Additive exPlanations), LIME (Local Interpretable Model-agnostic Explanations), Integrated Gradients, and attention visualization mechanisms. These interpretability tools help identify the specific text segments, technical terms, or contextual cues that most significantly influence the classification decision. This transparency is particularly valuable in the patent domain, where users must trust and understand the reasoning behind automated classifications for legal and strategic purposes.
The proposed framework further includes capabilities for multi-label classification, enabling the system to assign multiple relevant classification codes to patents that span across different technology domains. The system also supports the analysis of patent novelty, prior art relevance, and technology trend detection by examining classification patterns across temporal and geographical dimensions. Performance evaluation of the Transformer-based model will be conducted using accuracy, precision, recall, macro-F1 score, weighted-F1 score, and hierarchical classification metrics, while the explainability component will be assessed based on explanation faithfulness, consistency, and user interpretability.
The resulting system aims to provide patent professionals, researchers, and organizations with an accurate, efficient, and transparent tool for patent document classification, enabling faster prior art searches, improved patent examination processes, strategic technology landscape analysis, and informed intellectual property decision-making.
Datasets
Dataset	URL
USPTO Patent Classification Dataset	https://www.uspto.gov/learning-and-resources/electronic-data-products/patent-classification-dataset

CLEF-IP Patent Classification Dataset	https://www.clef-initiative.eu/track/clef-ip-2023

PatentBERT Dataset	https://huggingface.co/datasets/patent/patent_classification

WIPO Patent Corpus	https://www.wipo.int/standards/en/ipc/

Google Patents Public Datasets	https://cloud.google.com/blog/products/data-analytics/google-patents-public-datasets

NTCIR PatentMT Collection	https://www.thuir.cn/patentmt/




Approach
 


Project Group Members
S.NO.	ROLL NO.	STUDENT NAME
1.	2420030504	Vikas Suthar
2.	2420030446	Prakash
3.	2420030486	Kasam Vamshi
4.	2420030791	Om Pandey

