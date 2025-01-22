# End-to-End Medical Chatbot

This project is an end-to-end medical chatbot that uses LangChain, Pinecone, and Hugging Face for document retrieval and question-answering tasks.

## Description

The chatbot allows users to ask medical-related questions and get answers based on the context retrieved from a set of medical documents. The project uses LangChain for document loading and splitting, Pinecone for vector storage, and Hugging Face for embeddings and language models.

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/medical-chatbot.git
    cd medical-chatbot
    ```

2. Create a virtual environment and activate it:
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the required dependencies:
    ```sh
    pip install -r requirements.txt
    ```

4. Set up environment variables:
    - Create a [.env](http://_vscodecontentref_/0) file in the root directory with the following content:
        ```env
        PINECONE_API_KEY = "your_pinecone_api_key"
        HUGGINGFACEHUB_API_TOKEN = "your_huggingfacehub_api_token"
        ```

## Usage

1. **Indexing Documents:**
    - Run the [store_index.py](http://_vscodecontentref_/1) script to load PDF files, split them into chunks, and store the embeddings in Pinecone:
        ```sh
        python store_index.py
        ```

2. **Running the Chatbot:**
    - Start the Flask application:
        ```sh
        python app.py
        ```
    - Open your browser and go to `http://localhost:8080` to interact with the chatbot.


