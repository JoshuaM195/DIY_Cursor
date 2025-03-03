# DIY Cursor App

## What I Built

This is a bare-minimum app inspired by Cursor, an AI-powered code editor. It clones a GitHub repository, parses its code files, stores embeddings in PineconeDB, and uses Retrieval-Augmented Generation (RAG) with DeepSeek to answer questions about the codebase. It’s a simple proof-of-concept to explore how AI can assist with coding.

### Features
- Clones a GitHub repo locally.
- Parses code files (e.g., `.py`, `.js`, `.tsx`) while ignoring irrelevant dirs (e.g., `node_modules`).
- Creates embeddings using HuggingFace’s `sentence-transformers`.
- Stores embeddings in PineconeDB for fast retrieval.
- Uses OpenAI’s API (via OpenRouter) and DeepSeek to answer queries like "What’s happening in this codebase?" based on retrieved context.

## What I Learned

- **GitHub Integration**: How to clone repos programmatically with `PyGithub` and `GitPython`.
- **File Parsing**: Filtering and processing specific file types while skipping unnecessary folders.
- **Embeddings**: Generating vector representations of text with HuggingFace’s `SentenceTransformer`.
- **Vector Databases**: Setting up PineconeDB to store and query embeddings efficiently.
- **RAG Basics**: Combining retrieval (Pinecone) with generation (DeepSeek) to make sense of code.
- **APIs**: Wiring up OpenAI’s API through OpenRouter for LLM responses.
- **Python Workflow**: Managing dependencies and environment variables in a Colab-like setup.

## How It Works

1. Install libraries like `pygithub`, `langchain`, and `pinecone-client`.
2. Clone a repo.
3. Extract content from supported code files.
4. Convert file contents to embeddings and store them in PineconeDB.
5. Query the system with a question, retrieve relevant code snippets, and get an AI-generated answer.

## Why I Built It

I wanted to understand the core mechanics of AI coding tools like Cursor by building a stripped-down version. It’s a learning project to grasp how codebases can be analyzed and queried using modern AI techniques.

Feel free to explore the code and ask questions. I’m learning too!
