# Medical Question Answering with Retrieval Augmented Generation (RAG)

This project demonstrates a Retrieval Augmented Generation (RAG) approach for answering questions related to medical information. It leverages a large language model (LLM) combined with a knowledge base of medical texts to provide comprehensive and accurate answers.

## Overview

The system works in the following steps:

1. **Knowledge Base Creation:** A knowledge base is built from medical textbooks using the `datasets` library.
2. **Document Splitting:** Textbooks are split into smaller chunks using `RecursiveCharacterTextSplitter` from `langchain`.
3. **Embedding and Indexing:** Text chunks are embedded using `SentenceTransformer` and indexed using `FAISS` for efficient retrieval.
4. **Question Answering:**
    - Given a user's question, relevant documents are retrieved from the knowledge base based on semantic similarity.
    - The retrieved documents and the question are used as context for a large language model (e.g., GPT-2).
    - The LLM generates a comprehensive answer based on the context.

## Dependencies

- Python 3.7+
- Libraries: `datasets`, `langchain`, `faiss-cpu`, `optimum-quanto`, `sentence_transformers`, `transformers`, `bitsandbytes`

## Usage

1. Install the required libraries: `pip install datasets langchain_community faiss-cpu optimum-quanto sentence_transformers transformers bitsandbytes`
2. Run the notebook in Google Colab.
3. Ask a medical-related question.
4. The system will retrieve relevant information and generate an answer.

## Limitations

- The accuracy of the answers depends on the quality and coverage of the knowledge base.
- The system may not be able to answer questions that require complex reasoning or inference.
- The LLM may sometimes generate inaccurate or irrelevant responses.

## Future Work

- Expand the knowledge base with more diverse medical texts.
- Fine-tune the LLM for better performance on medical question answering.
- Implement error handling and evaluation metrics.

## Acknowledgements

- This project is inspired by the work on Retrieval Augmented Generation.
- Thanks to the developers of the libraries used in this project.
