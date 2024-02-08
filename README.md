# Retrieval Augmented Generation using Language Chains and PG Vector

Retrieval Augmented Generation (RAG) represents a cutting-edge approach that integrates retrieval mechanisms with natural language generation, enhancing the quality and relevance of generated content. This project leverages language chains and PG vectors to implement a robust RAG system.

 The system loads PDF documents, splits them into semantic chunks, computes embeddings using OpenAI's embeddings, and stores them in a PostgreSQL database using PG vectors. It then performs similarity searches and max marginal relevance searches based on user queries.

## Requirements

- Python 3.x
- [langchain_community](https://github.com/organization/langchain_community)
- [langchain_experimental](https://github.com/organization/langchain_experimental)
- [langchain_openai](https://github.com/organization/langchain_openai)
- [dotenv](https://pypi.org/project/python-dotenv/)
- PostgreSQL
- `biden.pdf` (sample PDF document)

## Setup

1. Install the required Python packages using `pip`:

   ```bash
   pip install langchain_community langchain_experimental langchain_openai python-dotenv

2. Install PostgreSQL and create a database. 
    ```python
    CONNECTION_STRING="postgresql+psycopg2://@localhost:5432/your_database"
    ```
3. run the jupytern notebook.

## What is PG Vector?

PG Vector, short for PostgreSQL Vector, is a powerful extension for PostgreSQL databases that facilitates efficient similarity search operations. It allows for the storage and indexing of high-dimensional vectors, making it ideal for applications requiring similarity matching, such as information retrieval and recommendation systems. PG Vector enables fast and scalable retrieval of semantically similar documents, making it an indispensable tool for retrieval augmented generation systems.

## How Similarity Search Works

Similarity search is the engine driving our Retrieval Augmented Generation system. It involves finding items in a dataset that closely match a given query. In our context, this means identifying relevant documents or passages from a corpus based on user input. By computing vector representations (embeddings) of both the query and the documents in the corpus, and measuring their similarity using advanced distance metrics, our system delivers precise and tailored results every time.

## Max Marginal Relevance Search vs. Similarity Search

While traditional similarity search aims to find the most similar documents to a given query, we take it a step further with Max Marginal Relevance (MMR) search. MMR search doesn't just focus on relevance – it also prioritizes diversity. By selecting documents that are not only relevant but also diverse from each other, MMR search ensures that our system delivers a comprehensive and varied set of results. It's a nuanced approach to information retrieval that sets us apart from the rest.

So dive in, explore, and experience the future of content generation with Retrieval Augmented Generation using Language Chains and PG Vector. Your journey to unparalleled insights and creativity starts here!