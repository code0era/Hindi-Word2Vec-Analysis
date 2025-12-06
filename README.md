
-----

# Hindi Word2Vec Embedding Analysis and Visualization

This project implements a complete **Hindi Natural Language Processing (NLP) pipeline**. It uses the **Word2Vec model** to analyze word relationships in a large corpus and visually demonstrates semantic similarity using **t-SNE** for clustering.

## 🚀 Key Features and Project Overview

Our primary goal is to show that words belonging to similar **semantic categories** (like 'माँ' and 'पिता') cluster together in the vector space learned by the model.

# Visuals and Description 

 **Semantic Clustering:** The final t-SNE plot successfully visualizes word embeddings grouped by semantic type. The closeness of colored points confirms learned relationships. |
 
 <img width="1699" height="1190" alt="image" src="https://github.com/user-attachments/assets/8ee8d925-a3e2-446d-8335-b88322101862" />

 **Guaranteed Hindi Plotting:** This project includes critical fixes to ensure **Devanagari characters** are rendered correctly on the plot labels, solving common Matplotlib complex script issues. |
 <img width="1094" height="572" alt="image" src="https://github.com/user-attachments/assets/b01c423c-dd60-4145-999e-a93f48f950ae" />

 
 **Model Metrics:** The pipeline successfully trained on over **5 million Hindi words** and calculated word similarities and analogies. |

<img width="931" height="319" alt="image" src="https://github.com/user-attachments/assets/080e019a-8d57-4175-916c-e71acab3b63c" />

---

## 🛠️ Setup and Installation

### Prerequisites

You need **Python 3.7+** and an environment (like Google Colab or Jupyter Notebook) where system commands can be executed.

### Installation

Run this command to install all necessary Python packages, including the stability fix for `scikit-learn` and the essential **text shaping libraries** for Hindi rendering:


!pip install --quiet gensim numpy matplotlib scikit-learn==1.2.2 gdown arabic-reshaper python-bidi


### Font Fix Methodology

The project ensures reliable Hindi character rendering by:

1.  Downloading the **Noto Sans Devanagari** font using the stable `gdown` utility.
2.  Using the `arabic-reshaper` and `python-bidi` libraries to correctly handle the **complex glyph shaping** required by the Devanagari script before Matplotlib plots the annotations.

-----

## 🔬 Methodology

### Data and Training

1.  **Corpus Creation:** A synthetic, highly repetitive corpus (approx. 5M words) is generated and cleaned to isolate **Devanagari characters** and Hindi punctuation (`।`).
2.  **Model Training:** A **Skip-gram Word2Vec model** creates **100-dimensional vectors** for each unique word.
3.  **Data Selection:** Target words are filtered from the vocabulary and manually grouped into categories (e.g., **'संबंध'**, **'प्रकृति'**).

### Dimensionality Reduction and Visualization

1.  **t-SNE Reduction:** The 100D vectors are mapped to **2D coordinates** using **t-SNE** to preserve local semantic relationships.
2.  **Visualization:** The final plot is generated, with annotations handled by the **text shaping** fix to display perfectly rendered Hindi words.

<!-- end list -->

```
