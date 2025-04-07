# Semantic Image Retrieval

## Introduction
Semantic image retrieval uses advanced algorithms and deep learning techniques to find images that match the user’s query based on the understanding of the content and context within the images. This repository contains the work completed during my internship at DxO, where I developed a solution for efficient image search based on images. This approach moves beyond traditional methods that rely solely on metadata or manual labeling, which can be prone to errors.

## Project Overview
The project was divided into two main phases:

1. **Image Captioning**: Generating accurate and detailed captions for images using state-of-the-art models.
2. **Image Retrieval**: Retrieving images based on user queries by embedding both the captions and queries in a shared vector space and performing a similarity search.

## Image Captioning
In this phase, multiple state-of-the-art models were evaluated, including Florence 2, LLaVA, and GPT-4. Different approaches to caption generation were explored:

- **Direct captioning from models**
- **Using carefully designed prompts to guide captioning**

Evaluation metrics such as BLEU and ROUGE were utilized for qualitative and quantitative assessments. Detailed captions generated using tailored prompts proved more useful for retrieval tasks. The final model selection was based on a balance between detail and computational efficiency, prioritizing models that generated high-quality, context-aware captions without excessive processing overhead.

## Image Retrieval Workflow
Various embedding models were tested, including:
- Alibaba’s GTE Large
- Intfloat’s Multilingual E5 Large Instruct
- OpenAI’s Text Embedding 3 Large

Selection was based on their performance ranking in the Massive Text Embedding Benchmark (MTEB), ensuring robust performance across various scenarios. Similarity searches were primarily conducted using cosine similarity to match user queries with stored image descriptions.

## Results
The final implementation combines the best-performing captioning and embedding models, achieving an optimal balance of accuracy, computational efficiency, and resource usage. A proof of concept (POC) was developed as a web-based application using Streamlit, demonstrating the image retrieval solution for DxO’s software like PhotoLab.

## Flow Diagram
![flow](https://github.com/user-attachments/assets/96e338ac-833f-4d47-af91-6aa9cf9429e1)


## References
1. Bin Xiao, Haiping Wu, Weijian Xu, Xiyang Dai, Houdong Hu, Yumao Lu, Michael Zeng, Ce Liu, Lu Yuan, "Florence-2: Advancing a Unified Representation for a Variety of Vision Tasks", arXiv preprint arXiv:2311.06242, 2023.
2. Bo Li, Yuanhan Zhang, Dong Guo, Renrui Zhang, Feng Li, Hao Zhang, Kaichen Zhang, Yanwei Li, Ziwei Liu, Chunyuan Li, "LLaVA-OneVision: Easy Visual Task Transfer", arXiv preprint arXiv:2408.03326, 2024.
3. Niklas Muennighoff, Nouamane Tazi, Loïc Magne, Nils Reimers, "MTEB: Massive Text Embedding Benchmark", arXiv preprint arXiv:2210.07316, 2022.

## License
This project is approved and published with permission from DxO.
