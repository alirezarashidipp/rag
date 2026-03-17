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
