
# A BERT Based Hybrid Recommendation System For Academic Collaboration

## Overview
This codebase implements a hybrid recommendation system for profile matching, optimized to overcome limitations in traditional networking methods. This project evaluates three techniques (TF-IDF, BERT and Hybrid) to enhance networking efficiency within academic circles. the hybrid approach was found to be optimal, effectively capturing both usage patterns and contextual relevance for user profiles. A unique dataset is also distributed for further study on this domain.


A unique, curated dataset is included to support further research and development in academic networking and recommendation systems. This dataset provides comprehensive features tailored to profile recommendation use cases, allowing for in-depth analysis and experimentation within the domain.








## Directory structure

```
project_root/
├── requirements.txt
├── Dataset/
│   ├── responses.csv   #Corpus from survery form.
│   ├── Skills.csv      #Extracted skills for synthetic data.
|   ├── topic.csv       #Extracted domain interests for synthetic data.
│   ├── Synthetic profiles.ipynb    #Synthetic data generation.
│   └── merged_df.csv          #Compiled corpus
├── BERT/
│   └── BERT.ipynb
|
├── TF-IDF/
│   └── TF-IDF.ipynb
│
└── Hybrid/
    └── Hybrid.ipynb
```




## Dataset

The dataset comprises of user profile information collected using survery forms and additional synthetic data generation.

| Column            | Data Type | Description                                   |
|-------------------|-----------|-----------------------------------------------|
| **Full Name**         | `String`    | Full name of the user                         |
| **Email**             | `String`    | Email address of the user                     |
| **Profession**        | `String`    | Profession or job title of the user           |
| **Experience**        | `Number`    | Years of experience in the user's profession  |
| **Interest**          | `String`    | Type of academic or professional interest     |
| **Collaboration with**| `String`    | Preferred collaborators for projects          |
| **Domain**            | `String`    | Domain or field of collaboration              |
| **Skillset**          | `String`    | User's key skills or expertise     

Affinity propagation cluster based relabelling was employed to cluster similar profiles based on the similarity scores as on the notebooks. 

![hybrid_cluster](https://github.com/user-attachments/assets/0f276071-8713-440e-a422-ef80e8f3f15b)


## Results

| Metric            | BERT     | TF-IDF   | Hybrid  |
|-------------------|----------|----------|---------|
| **Davies-Bouldin**   | 1.5238   | 1.0342   | 1.1052  |
| **Silhouette**       | 0.1578   | 0.3876   | 0.3383  |
| **Intra-Cluster**    | 0.8819   | 0.7430   | 0.8053  |
| **NDCG**             | 0.8329   | 0.7634   | **0.8587**  |
| **MAP**              | 0.7858   | 0.8112   | **0.8275**  |

### Metric Descriptions

- **Davies-Bouldin Index**: Measures the average similarity ratio between each cluster and the one most similar to it. A lower value indicates better-defined clusters.
- **Silhouette Score**: Ranges from -1 to +1, indicating how similar a data point is to its own cluster compared to others. Higher values represent better clustering performance.
- **Intra-Cluster Distance**: The average distance between data points within the same cluster. Lower values indicate more compact clusters.
- **NDCG (Normalized Discounted Cumulative Gain)**: Evaluates the ranking quality by accounting for the relevance of results. Higher values indicate better ranking quality.
- **MAP (Mean Average Precision)**: Measures the average precision across multiple queries. Higher MAP values indicate better performance in terms of relevance and ranking quality.
## Acknowledgements

**Funding:** H. Thangaraj V. Varun J. Eshaan V. Kanishka and K . Diya
contributed to this work while undertaking a research collaboration with the Department of Computer Science, Vellore Institute of Technology under Professor Sangeetha N.

**Open Access:** For open access purposes, the authors have applied a Creative Commons Attribution (CC BY) licence to any Author Accepted
Manuscript version arising.

**Data Access Statement:** This study involves primary analyses of a custom curated dataset, that are described in the text.


## Appendix

**Note:** Please, when using any of the resources provided here, remember to cite our paper

