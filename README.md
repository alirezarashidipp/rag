Input Ticket / Query (English)
        ↓
Embedding Model: nomic-embed-text-v1.5-v1 (OR text-embedding-3-small)
(Generates ONLY Dense Vectors)
        ↓
Single Vector DB: (Qdrant > 1.7) OR (Milvus > 2.14)
├── Generates Sparse internally via its Native Built-in BM25 Tokenizer
└── Executes ANN on Dense Vectors 
        ↓
Score-Based Fusion 
(Convex Combination executed natively inside Qdrant/Milvus)
        ↓
Top-40 Candidates
        ↓
Cross-Encoder Reranker (mixedbread-ai/mxbai-rerank-large-v1 - mixedbread-ai/mxbai-rerank-base-v1 - jinaai/jina-reranker-v2-base-en - Alibaba-NLP/gte-multilingual-reranker-base - BAAI/bge-reranker-v2-m3 - BAAI/bge-reranker-large - BAAI/bge-reranker-base - cross-encoder/ms-marco-MiniLM-L-12-v2 )
        ↓
Top-3 Results





Embedding Models:
1. UAE-v1
UAE (Universal Angle Embedding) is a state-of-the-art universal English sentence embedding model developed by WherelsAl. It is designed to generate high-dimensional vector embeddings that capture the semantic meaning of input text effectively.



2. nomic-embed-text-v1.5-v1
A versatile text embedding model from Nomic that generates dense vector representations optimized for semantic search, clustering, and data discovery across va domains.


3. text-embedding-3-large-v1
High-performance embedding model for large-scale semantic search and complex document retrieval.

4. text-embedding-3-small-v1
Fast, affordable embedding model for high-throughput, scalable semantic analysis use cases.


5. text-embedding-ada-002-v2
   Legacy multilingual embedding model for semantic search, clustering, and text classification.
