# AI Q&A Bot (RAG Approach)

## **Goal**
Build a **Question & Answer bot** that can:
- Search through local text files
- Find relevant context using **embeddings + FAISS**
- Answer questions using **ChatGPT (GPT-4o-mini)**

---

## **Features**
- **Multiple Documents**: Reads all `.txt` files from `data/`
- **Chunking**: Splits large texts into small, searchable pieces
- **Embeddings**: Uses `text-embedding-3-small` for vector representation
- **Vector Search**: FAISS for fast similarity search
- **Context-Aware Answers**: Uses retrieved text as context for GPT answers

---

## **Tech Stack**
- **Language**: Python
- **Libraries**: OpenAI, FAISS, NumPy
- **Model**: GPT-4o-mini + text-embedding-3-small

---

## **Project Structure**
```
project_rag/
│── data/
│    ├── doc1.txt
│    ├── doc2.txt
│── rag_bot.ipynb
│── rag_bot.py
│── README.md
```

---

## **Setup & Run**
### **1. Install dependencies**
```
pip install openai faiss-cpu numpy
```

### **2. Set OpenAI API Key**
```
export OPENAI_API_KEY="your_key_here"
```

### **3. Run Notebook**
Open `qabot-with-chatpgt-embeddingst.ipynb` in Jupyter.

### **4. Run Python Script**
```
python qabot-with-chatpgt-embeddingst.ipynb.py
```