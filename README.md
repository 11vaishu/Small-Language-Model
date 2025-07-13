# Small-Language-Model
This repository contains a Small Language Model (SLM) designed to answer questions based on the content of a given book using Retrieval-Augmented Generation (RAG). The model processes a book, retrieves relevant passages, and generates related responses.
# Small Language Model (SLM) for Book-Based Q&A

## Project Overview
This project develops a **Small Language Model (SLM)** capable of answering questions based on the content of a given book. Using **Retrieval-Augmented Generation (RAG)**, the model retrieves relevant text from a book and generates meaningful responses.

## Objectives
- **Process and store** book content efficiently.
- **Retrieve relevant sections** when a question is asked.
- **Generate accurate answers** using a fine-tuned transformer model.
- **Improve accuracy** through fine-tuning and embedding-based retrieval.

## Approach
The model follows the **Retrieval-Augmented Generation (RAG)** framework:
1. **Retrieval Mechanism**: Converts book text into embeddings and retrieves the most relevant passages.
2. **Generation Mechanism**: A fine-tuned transformer model generates an answer based on the retrieved content.

## Model Architecture
The architecture consists of:
- **Retrieval Component**: Uses vector embeddings and cosine similarity to fetch relevant text.
- **Transformer Model**: Fine-tuned for book-based question answering.

## Preprocessing Techniques
- **Tokenization**: Converts text into tokens for model processing.
- **Vectorization**: Embeds book passages for retrieval.
- **Data Cleaning**: Standardizes text format.
- **Batching & Padding**: Ensures structured inputs for training.

## Evaluation Methodology
- **Loss Calculation**: Uses **Mean Squared Error (MSE)** to measure performance.
- **Relevance Scoring**: Measures how well retrieved context matches queries.
- **Manual Validation**: Checks if generated answers correctly reflect book content.

## Instructions for Running the Model
### Install Dependencies
```bash
pip install torch transformers numpy
```

###  Load the Model
```python
from model import load_model
model = load_model("fine_tuned_model.pth")
```

###  Ask a Question
```python
query = "Who is the Cheshire Cat?"
answer = ask_question(model, tokenizer, retriever, query)
print(answer)
```
