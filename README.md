# **Getting Started with NLP: Patent Phrase Matching**  

This repository is based on a **Kaggle tutorial for absolute beginners in natural language processing (NLP)** (https://www.kaggle.com/code/jhoward/getting-started-with-nlp-for-absolute-beginners), using the **U.S. Patent Phrase to Phrase Matching competition** as a practical example. The tutorial introduces key NLP concepts and techniques, guiding users through the process of building a semantic similarity model step by step.

---

### **Why Patent Phrase Matching?**  
The Kaggle competition focuses on matching pairs of phrases from patent documents by their contextual similarity. This task is crucial for patent professionals, helping them identify related patents, avoid redundancies, and improve patent examination workflows.  

This tutorial frames the challenge as a **classification problem**, making it accessible to beginners while showcasing the power of modern NLP techniques.

---

## **About the Competition**  
In this competition, participants predict the **semantic similarity** between pairs of phrases in the context of patent documents. Similarity is measured on a scale from 0 to 1, where:
- **0** means completely unrelated.  
- **1** means identical in meaning.  

For example:
- *Anchor*: "television set"  
- *Target*: "TV set"  
- **Score**: **1.0** (identical meaning).  

### **Data**  
The dataset includes:
- **Train set**: Contains pairs of phrases with similarity scores.  
- **Test set**: Contains pairs of phrases without similarity scores (to be predicted).  
- **CPC codes**: Provide context for phrases, indicating the technical domain they belong to.  

The training data helps the model learn to assess similarity in a patent-specific context, e.g., recognizing that *"strong material"* could mean *"steel"* in one domain but *"ripstop fabric"* in another.

--

## **Quick Start**  
### **Requirements**
This project relies on Python and the following libraries:
- `transformers`  
- `datasets`  
- `scikit-learn`  
- `pandas`  

Install dependencies with:  
```bash
pip install -r requirements.txt
```

---

## **Results**  
The model achieves a Pearson correlation of ~0.83 on the validation set, demonstrating its ability to assess semantic similarity effectively.  
