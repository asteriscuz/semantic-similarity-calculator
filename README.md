# Semantic Similarity Calculator

A tool that measures how similar two sentences are in meaning using sentence embeddings and cosine similarity.

## What It Does

- Converts text into vector embeddings (numerical representations)
- Calculates semantic similarity between sentences (0 = different, 1 = identical)
- Works on meaning, not just exact word matching

## Quick Start

### Install Dependencies
```bash
pip install -r requirements.txt
```

### Run the Notebook
Open `semantic_similarity_calculator.ipynb` in Jupyter or Google Colab


## Example Usage
```python
from semantic_similarity import semantic_similarity

sent1 = "The cat sits on the mat"
sent2 = "A feline rests on a rug"

score = semantic_similarity(sent1, sent2)
print(f"Similarity: {score:.3f}")  # Output: ~0.75-0.85
```

## Sample Results

| Sentence 1 | Sentence 2 | Similarity Score |
|-----------|-----------|-----------------|
| "I love dogs" | "Puppies are cute" | 0.68 |
| "The weather is sunny" | "I ate pizza" | 0.12 |
| "Machine learning is fun" | "ML is exciting" | 0.82 |

## Tech Stack

- **sentence-transformers** - Pre-trained embeddings (all-MiniLM-L6-v2)
- **scikit-learn** - Cosine similarity calculation
- **Python 3.x**

## What I Learned

- How embeddings represent text as vectors
- Cosine similarity measures angle between vectors
- Similar meanings = closer vectors in embedding space
- Foundation for RAG systems and semantic search

## 🔗 Resources

- [Sentence-Transformers Documentation](https://www.sbert.net/)
- [The Illustrated Word2Vec](http://jalammar.github.io/illustrated-word2vec/)

## 📝 License

MIT License


## **requirements.txt:**
```
sentence-transformers
scikit-learn
numpy
