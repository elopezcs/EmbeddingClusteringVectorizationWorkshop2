# **EmbeddingClusteringVectorizationWorkshop ** 

### **Team Member:** 
   - *Sabrina Ronnie George Karippatt*
   - *Edwin Lopez*

This repository contains the complete implementation for the  
**Embedding, Clustering, and Vectorization Workshop**, including Word2Vec,  
GloVe (pretrained alignment), co-occurrence modeling, and hierarchical clustering.

---

## **Project Description**

This workshop demonstrates end-to-end NLP vectorization techniques using a
real-world corpus. The workflow includes:

1. **Document Collection & Preprocessing**  
   - Brown Corpus loading  
   - Tokenization  
   - Lowercasing & normalization  

2. **Vocabulary & Co-occurrence Matrix Construction**  
   - 478-word vocabulary  
   - Sliding-window co-occurrence matrix  
   - Foundation for GloVe-style global models  

3. **Hierarchical Clustering & Visualization**  
   - Ward’s method clustering  
   - Truncated dendrogram (25 cluster groups)  
   - Visualization of word similarity patterns  

4. **Word Embedding Models**
   - **Word2Vec** (predictive, local context)  
   - **GloVe** (count-based, global co-occurrence)  
   - Alignment of pretrained GloVe vectors (50d)

5. **Model Comparison**
   - A detailed table comparing **Word2Vec vs GloVe**  
   - Discussion of strengths, weaknesses, and use cases  

---

## **Files Included**

- **EmbeddingClusteringVectorizationWorkshop.ipynb**  
  Complete notebook with all code, outputs, markdown, clustering, Word2Vec,  
  GloVe alignment, and comparison table.

- **/data**  
  Folder containing pretrained GloVe embeddings (`glove.6B.50d.txt`).

---

## **Dataset Used**

### **Brown Corpus (NLTK)**
- Source: https://www.nltk.org/nltk_data/  
- License: Public domain (varies by category, all distributable for academic use)  
- Used: First 50 sentences for demonstration purposes

### **GloVe Embeddings**
- Source: https://nlp.stanford.edu/projects/glove/  
- File used: **glove.6B.50d.txt**  
- License: Apache License 2.0

---

## **How to Run**

1. Install dependencies:
   ```bash
   pip install nltk gensim scipy numpy matplotlib

### **Place the GloVe file in the following directory:**
     data/glove.6B.50d.txt

### **Run the notebook:**

Open EmbeddingClusteringVectorizationWorkshop.ipynb in Jupyter Notebook or VS Code and run all cells.

### **Notes**
   - GloVe vectors are not trained in this notebook. We perform pretrained GloVe vector alignment to our custom vocabulary.
   - Ward’s hierarchical clustering is used because it minimizes intra-cluster variance, making relationships clearer in the dendrogram.
   - Co-occurrence sparsity explains why truncated dendrograms provide better interpretability.