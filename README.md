# Talk to a PDF using AI

**Author:** Anish Mahapatra ([LinkedIn](https://www.linkedin.com/in/anishmahapatra/))

This project demonstrates how to use AI to interact with a PDF document stored in Google Drive. It leverages the power of Google Colab, OpenAI API, and a free Cassandra DB online to achieve this.

## Workflow

1. **Read the PDF:** The application reads the PDF document using PyPDF2.
2. **Create Text Chunks:** OpenAI Embeddings are used to split the text into meaningful chunks.
3. **Generate Text Embeddings:** Each text chunk is further broken down into text embeddings.
4. **Store Embeddings:** The text embeddings are stored in a NoSQL vector database (Cassandra DB on Datastax) for efficient retrieval.

## Components

* **Langchain:** Provides the framework for interacting with the document and LLM.
* **AstraDB (Datastax):** Offers a serverless Cassandra DB with vector search capabilities.
* **OpenAI:** Powers the text embedding generation and LLM used for answering questions.

## Prerequisites

* OpenAI API Key
* Datastax Account (for Database ID and Application Tokens)

## Setup

1. **Import Dependencies:** Install the required Python packages using pip.
2. **Provide Secrets:** Set your OpenAI API Key and Datastax credentials as environment variables.
3. **Create LangChain Vector Store:** Initialize the Cassandra vector store using Langchain and your Datastax connection.

## Usage

The notebook provides a question-answering loop where you can ask questions about the PDF document. The application retrieves relevant text snippets and uses an LLM to formulate an answer based on the context.

**Example Questions:**

* Who wrote the speech?
* Which year was the speech written?
* What are the 4 major castes according to the Prime Minister?

Feel free to explore the notebook and ask your own questions to interact with the PDF document using AI!