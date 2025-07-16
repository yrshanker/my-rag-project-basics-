
# My RAG Project (Basics)

This repository demonstrates a simple **Retrieval-Augmented Generation (RAG)** chatbot using cosine similarity and [Ollama](https://ollama.com/).

## Features

- Embeds your text dataset and stores it in-memory for efficient similarity search
- Retrieves the most relevant facts using cosine similarity
- Uses an Ollama language model to generate grounded answers based on retrieved context
- Lightweight and easy to run locally

---

## Setup Instructions

### 1. Clone this repository

```
git clone https://github.com/yrshanker/my-rag-project-basics-.git
cd my-rag-project-basics-
```

### 2. Set up a Python virtual environment (recommended)

```
python3 -m venv venv
source venv/bin/activate
```

### 3. Install dependencies

```
pip install -r requirements.txt
```

### 4. Install and set up Ollama

- Download and install Ollama from [https://ollama.com](https://ollama.com)
- Pull required models:
    ```
    ollama pull hf.co/CompendiumLabs/bge-base-en-v1.5-gguf
    ollama pull hf.co/bartowski/Llama-3.2-1B-Instruct-GGUF
    ```

---

## Usage

1. Add your text file (e.g. `cat-facts.txt`) to the project directory.
2. Run the chatbot:
    ```
    python rag.py
    ```
3. Enter your questions at the prompt. The chatbot will search your text chunks and answer using the LLM.

---

## File Structure

| File           | Description                         |
|----------------|-------------------------------------|
| rag.py         | Main RAG chatbot script             |
| requirements.txt| Python dependencies                |
| cat-facts.txt  | Example dataset (editable/replaceable) |

---

## Customize

- You can replace `cat-facts.txt` with any text file of your own facts, notes, or study material.
- Edit `rag.py` to load a different file if you choose to rename your dataset.

---

## Troubleshooting

- **Ollama not found?** Make sure you’ve installed and started Ollama.
- **Model errors?** Re-run the `ollama pull ...` commands to be sure the models are downloaded.
- **Dependency issues?** Ensure your virtual environment is active and dependencies are installed.

---

## License

MIT

---

## Acknowledgements

Inspired by Hugging Face's RAG tutorials and the Ollama community.

```
