# 🏘️ RealEstate Research Tool

I built a user-friendly news research tool designed for effortless information retrieval. Users can input article URLs and ask questions to receive relevant insights from the real-estate domain. (But its features can be extended to any domain.)

## Features

* Load URLs or upload text files containing URLs to fetch article content.
* Process article content through LangChain's UnstructuredURL Loader
* Construct an embedding vector using HuggingFace embeddings and leverage ChromaDB as the vectorstore, to enable swift and effective retrieval of relevant information.
* Interact with the LLM's (Llama3 via Groq) by inputting queries and receiving answers along with source URLs.

## Set-up

1. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

2. **Create Environment File**
   Create a `.env` file with your GROQ credentials as follows:
   ```env
   GROQ_MODEL=MODEL_NAME_HERE
   GROQ_API_KEY=GROQ_API_KEY_HERE
   ```

3. **Run the Application**
   ```bash
   streamlit run app/main.py
   ```

## Usage/Examples

The web app will open in your browser after the set-up is complete.

* On the sidebar, you can input URLs directly.
* Initiate the data loading and processing by clicking "Process URLs ➤"
* Observe the system as it performs text splitting, generates embedding vectors using HuggingFace's Embedding Model.
* The embeddings will be stored in ChromaDB.
* One can now ask a question and get the answer based on those news articles

### Sample URLs for Testing

In the tutorial, we'll use the following news articles:

* https://www.cnbc.com/2024/12/21/how-the-federal-reserves-rate-policy-affects-mortgages.html
* https://www.cnbc.com/2024/12/20/why-mortgage-rates-jumped-despite-fed-interest-rate-cut.html
* https://www.cnbc.com/2024/12/17/wall-street-sees-upside-in-2025-for-these-dividend-paying-real-estate-stocks.html

## Requirements

```txt
python-dotenv
streamlit
unstructured
tiktoken
langchain-chroma
langchain-groq
langchain-community
protobuf
langchain-huggingface
selenium
```

