# 📚 Retrieval-Augmented Generation (RAG) System for PDF Question Answering

Welcome to the **Retrieval-Augmented Generation (RAG) System** project! This system empowers users to interact with PDF documents by uploading them and asking questions. The system intelligently retrieves relevant information and generates precise, contextually accurate responses.

## 🛠️ Key Features

### 1. Document Ingestion
- **PDF Loading**: Leverages `PyPDFium2Loader` for robust PDF processing.
- **Text Splitting**: Utilizes advanced methods to segment documents:
  - **Semantic Chunking**: Breaks text into meaningful segments, preserving context.
  - **Recursive Splitting**: Ensures chunks fit within token limits for optimal processing.

### 2. Embeddings and Vector Store
- **Embeddings Generation**: Converts text chunks into dense, semantic vectors using the `FastEmbedEmbeddings` model.
- **Vector Store**: Efficiently stores embeddings in a `Qdrant` vector store for quick retrieval during queries.

### 3. Reranking and Filtering
- **Reranking**: Applies the `FlashrankRerank` model to prioritize document chunks by relevance.
- **LLM Chain Filtering**: Optionally filters results further using a Large Language Model (LLM) for enhanced accuracy.

### 4. Question Answering (QA) Chain
- **Prompt Construction**: Crafts structured prompts with a chat template, guiding the LLM to produce concise, relevant answers.
- **Response Generation**: Generates markdown-formatted responses using either local (`ChatOllama`) or remote (`ChatGroq`) LLMs.

### 5. User Interaction
- **Streamlit Interface**: Provides an intuitive, web-based interface for seamless user interaction.
- **Conversation Management**: Maintains session history for continuous, context-aware conversations.

### 6. Session and Document Management
- **Session Handling**: Manages user sessions, preserving context across multiple queries.
- **Document Upload**: Supports multiple PDF uploads, processing, and storing documents for ongoing interaction.

## 🔄 Workflow Overview

1. **PDF Upload**: Users upload a PDF, which the system processes by splitting it into text chunks and embedding them into vectors.
2. **Question Submission**: Users submit a query; the system retrieves the most relevant chunks, reranks, and filters them.
3. **Answer Generation**: The system generates an answer based on the retrieved context and presents it to the user.
4. **Review and Interaction**: Users can review the answer with references to the source documents, ensuring transparency and trust.

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- Streamlit

### Installation

Clone the repository and install the required dependencies:

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
pip install -r requirements.txt
```

### Usage

To launch the application:

```bash
streamlit run app.py
```

You can now upload PDFs, ask questions, and explore the system’s capabilities via the web interface.

## 🤝 Contributing

Contributions are welcome! If you have ideas to improve the project, feel free to fork the repository, make your changes, and submit a pull request. Please ensure that your contributions align with the project's goals and coding standards.

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## 🙏 Acknowledgements

This project leverages several cutting-edge tools and models, including:
- **`PyPDFium2Loader`** for PDF processing
- **`FastEmbedEmbeddings`** for generating embeddings
- **`Qdrant`** for vector storage
- **`FlashrankRerank`** for reranking results
- **`ChatOllama`** and **`ChatGroq`** for language model-based response generation

We extend our gratitude to the creators of these technologies for making this project possible.

