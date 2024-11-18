# LLM-Data-Engineering
**Overview**
This repository contains a complete solution for ingesting, processing, vectorizing, and querying mixed structured and unstructured data. The pipeline also integrates Retriever-Augmented Generation (RAG) to generate summaries from queried data. The project demonstrates scalable and efficient data engineering practices using modern NLP tools and vector storage.

**Features**
**Data Ingestion:**
1. Load data from SQLite database and CSV file.
2. Ensure schema is optimized for querying.
   
**Data Preprocessing:**
1. Clean text data by removing noise.
2. Handle missing values for robust analysis.
   
**Text Embedding:**
1. Use sentence-transformers to generate embeddings for unstructured text.
2. Support batch processing for large datasets.
   
**Similarity Search:**
1. Implement FAISS for efficient similarity-based search.

**RAG Integration:**
1. Generate concise summaries for retrieved data using pre-trained transformer models.

**Logging and Monitoring:**
1. Track data pipeline performance and execution time for key stages.
   
**Scalability:**
1. Batch processing and modular design enable handling large datasets.

   **Installation**
**Prerequisites**
1. Python 3.8 or higher
2. Required libraries:

!pip install sentence-transformers faiss-cpu transformers pandas sqlite3

**Dataset**
**Amazon Fine Food Reviews Dataset**

**Place the following files in the working directory:**
1. database.sqlite
2. Reviews.csv

  ** File Structure**

assignment.ipynb: Main notebook containing the end-to-end pipeline implementation.
database.sqlite: SQLite database used as one of the data sources.
Reviews.csv: CSV file used as the second data source.
faiss_index_sqlite and faiss_index_csv: FAISS indices for similarity search.
embeddings_sqlite.npy and embeddings_csv.npy: Pre-generated embeddings stored as numpy arrays.

**Key Components**
**1. Data Ingestion:**

Loads data from SQLite and CSV sources.
Prepares the schema for efficient querying.

**2. Preprocessing:**

Cleans text fields using regular expressions.
Adds a Cleaned_Text column for processed data.
Vectorization:

Generates embeddings using the all-MiniLM-L6-v2 model.
Saves embeddings for reuse.

**3. Query Retrieval:**

Retrieves similar records based on vector embeddings.
Uses FAISS for fast and scalable similarity search.

**4. RAG Workflow:**

Combines retrieved text and generates summaries using Hugging Face's transformers.

**5. Monitoring and Logging:**

Logs time taken for each step to identify bottlenecks.



