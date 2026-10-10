
# RAG-Based PDF Question Answering System

A Python-based Retrieval-Augmented Generation (RAG) project that explores how to answer natural-language questions using information retrieved from PDF documents.

## Overview

Large language models may not have access to the contents of a user's private documents. This project explores a document question-answering workflow that retrieves relevant text from a PDF and uses that context to generate a response.

## Problem Statement

Finding specific information in lengthy PDF documents can be time-consuming. This project explores a way to make document information easier to access through natural-language questions.

## How It Works

1. **PDF Loading:** Extract text from a PDF document.
2. **Text Splitting:** Divide the extracted text into smaller chunks.
3. **Embedding Generation:** Convert text chunks into vector representations.
4. **Vector Storage:** Store the embeddings in a vector database.
5. **Similarity Search:** Retrieve chunks relevant to the user's question.
6. **Answer Generation:** Provide the retrieved context to a language model to generate an answer.

## Technologies

- Python
- LangChain
- OpenAI embeddings and language models
- ChromaDB
- PyPDF
- Jupyter Notebook

## Project Structure

```text
RAG-Based-PDF-QA-System/
├── notebooks/
│   └── rag_based_pdf_qna_bot.ipynb
├── README.md
├── requirements.txt
├── .gitignore
└── .env.example
```

## Setup and Installation

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/RAG-Based-PDF-QA-System.git
cd RAG-Based-PDF-QA-System
```

Replace `YOUR-USERNAME` with your GitHub username.

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure the API key

Create a local `.env` file based on `.env.example` and add your own API key.

Do not commit the `.env` file to GitHub.

### 5. Run the notebook

Open the notebook in VS Code or Jupyter Notebook and execute the cells in order. Follow any additional setup instructions required by the notebook.

## Testing Plan

- Test the workflow with a PDF containing readable text.
- Ask questions whose answers appear explicitly in the document.
- Check whether the retrieved text is relevant to each question.
- Test questions about information absent from the PDF.
- Verify how the system handles empty, scanned, or unsupported PDFs, where applicable.

## Limitations

- Answer quality depends on document extraction, chunking, retrieval, and the language model.
- Scanned PDFs may require OCR support.
- Model API usage may incur costs.
- Retrieval-based answers can still be incorrect or unsupported by the source.

## Learning Objectives

- Understand the fundamentals of Retrieval-Augmented Generation.
- Explore document loading and text chunking.
- Learn how embeddings and vector databases support semantic retrieval.
- Understand how retrieved context can be used for LLM-based question answering.

## Project Status

Update this section after running the notebook and verifying the workflow.

## Acknowledgment

This project is based on learning material from the
[Complete GenAI Course — Python and LangChain](https://github.com/techsimpluslearning/Complete-GenAI-Course-Python-Langchain).

The notebook and implementation should be credited in accordance with the original repository's license.
