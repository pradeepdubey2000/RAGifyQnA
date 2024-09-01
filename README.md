# 📚 **Retrieval-Augmented Generation (RAG) System** for PDF Question Answering

Welcome to the **Retrieval-Augmented Generation (RAG) System** project! This cutting-edge system allows users to interact with PDF documents by uploading them and asking questions. The system intelligently retrieves relevant information and generates precise, contextually accurate responses.

## 🛠️ **Key Features**

### 1. **Document Ingestion** 📄
- **PDF Loading**: Utilizes `PyPDFium2Loader` for robust PDF processing.
- **Text Splitting**: Advanced segmentation methods:
  - **Semantic Chunking**: Breaks text into meaningful segments while preserving context.
  - **Recursive Splitting**: Divides text into smaller chunks to fit within token limits.

### 2. **Embeddings and Vector Store** 🔍
- **Embeddings Generation**: Converts text chunks into dense, semantic vectors with `FastEmbedEmbeddings`.
- **Vector Store**: Stores embeddings in a `Qdrant` vector store for quick retrieval during queries.

### 3. **Reranking and Filtering** 🎯
- **Reranking**: Uses `FlashrankRerank` to prioritize document chunks by relevance.
- **LLM Chain Filtering**: Optionally filters results using a Large Language Model (LLM) for enhanced accuracy.

### 4. **Question Answering (QA) Chain** 🤖
- **Prompt Construction**: Crafts structured prompts with a chat template for generating concise, relevant answers.
- **Response Generation**: Provides markdown-formatted responses using either local (`ChatOllama`) or remote (`ChatGroq`) LLMs.

### 5. **User Interaction** 💬
- **Streamlit Interface**: Offers a user-friendly web interface for seamless interaction.
- **Conversation Management**: Maintains session history for context-aware conversations.

### 6. **Session and Document Management** 📑
- **Session Handling**: Manages user sessions to preserve context across queries.
- **Document Upload**: Supports multiple PDF uploads, processing, and storage.

## 🎥 **Demo Video**

Experience the working Streamlit UI in action:

📄I have uploaded my resume for demonstration purposes.📄

[![Watch Demo Video](https://img.youtube.com/vi/your-video-id/maxresdefault.jpg)](https://github.com/user-attachments/assets/87b7ff0d-f139-412a-ac8c-df9e83a52b97)

## 🔄 **Workflow Overview**

1. **📥 PDF Upload**: Users upload a PDF, which is split into text chunks and embedded into vectors.
2. **❓ Question Submission**: Users ask a query; the system retrieves, reranks, and filters the most relevant chunks.
3. **💡 Answer Generation**: The system generates and presents an answer based on the retrieved context.
4. **🔍 Review and Interaction**: Users review the answer with references to source documents, ensuring transparency.

## 🚀 **Getting Started**

### **Prerequisites** 🔧
- Python 3.8+
- Streamlit

### **Installation** ⚙️

Clone the repository and install the dependencies:

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
pip install -r requirements.txt
```

### **Usage** 🏃‍♂️

To launch the application:

```bash
streamlit run app.py
```

Upload PDFs, ask questions, and explore the system’s capabilities via the web interface.

## 🤝 **Contributing**

Contributions are welcome! Fork the repository, make your changes, and submit a pull request. Please align your contributions with the project’s goals and coding standards.

## 📄 **License**

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## 🙏 **Acknowledgements**

This project leverages several advanced tools and models, including:
- **`PyPDFium2Loader`** for PDF processing 📄
- **`FastEmbedEmbeddings`** for generating embeddings 🔍
- **`Qdrant`** for vector storage 📦
- **`FlashrankRerank`** for reranking results 🎯
- **`ChatOllama`** and **`ChatGroq`** for language model-based responses 🤖

Special thanks to the creators of these technologies for making this project possible! 🌟
