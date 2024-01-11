# QA System for Cloud Computing

## Overview

This colab notebook aims to develop a robust Question-Answering (QA) system for cloud computing, utilizing the RAG (Retrieval-Augmented Generation) model, Pinecone for vector embeddings, and Hugging Face Transformers for natural language processing. The system efficiently answers questions related to cloud computing by combining information retrieval and state-of-the-art language models.

## Features

- **Document Loading:** The system loads documents from the specified directory using a custom loader.

- **Document Splitting:** Documents are split into chunks for efficient processing, leveraging RecursiveCharacterTextSplitter.

- **Embeddings:** HuggingFaceEmbeddings are used for generating contextual embeddings of the input text.

- **Pinecone Indexing:** Pinecone is employed to index the document chunks, facilitating fast and scalable similarity searches.

- **Hugging Face Hub Integration:** The system integrates with the Hugging Face Hub to access language models for retrieval and generation.

- **RetrievalQA:** The project includes a RetrievalQA module that combines the power of Pinecone's retriever and Hugging Face language models for accurate question answering.

## Usage

Example usage with the provided query:

```python
query = "what is cloud computing"
result = qa.run(query)
print(result)
```

The expected result for the query "what is cloud computing" is:
```
Cloud computing is the delivery of computing services—including servers, storage, databases, networking, software, analytics, and intelligence—over the internet (“the cloud”) to offer faster innovation, flexible resources, and economies of scale.

