# Travel Visa Assistant (English)

This is a simple travel visa assistant built with LangChain, GPT-4, and FAISS. You can ask questions about visiting Canada, the US, or the UK, and the bot will pull up-to-date information from their official immigration websites. It uses web scraping + RAG (Retrieval-Augmented Generation) to give more grounded, relevant answers.

## Features ##

- Scrapes visa policy info from trusted government websites

- Splits the text into chunks and stores them in a FAISS vectorstore

- Uses GPT-4 to answer questions based on the scraped content

- Runs in a Jupyter Notebook with a simple Gradio chatbot UI

Right now, it's built just for English-language questions only.

## Tech Stack ##

- Python 3.8

- LangChain (for RAG)

- OpenAI GPT-4 (via langchain_openai)

- FAISS (vectorstore)

- Gradio (chat interface)

- BeautifulSoup + requests (scraping)

- dotenv (for secret keys)

## Version Compatibility ##

langchain==0.1.14\
langchain-community==0.0.33\
langchain-openai==0.0.7\
openai==0.28\
faiss-cpu==1.7.4\
gradio==3.50.2\
beautifulsoup4==4.12.2\
python-dotenv==1.0.1

⚠️ Mixing different langchain and langchain-community versions caused a lot of issues, so stick to this combo.

## Getting Started ##

### 1. Clone and navigate the repository
```
git clone https://github.com/zarinhq/ai-visa-assistant.git
cd travel-visa-assistant
```
### 2. Set up a virtual environment
```
python3 -m venv env
source env/bin/activate
```
### 3. Install dependencies
```
pip install -r requirements.txt
```
### 4. Create a .env file
Add your OpenAI API key like this:
```
OPENAI_API_KEY=your-openai-key
```
### 5. Launch the notebook
```
jupyter notebook
```
### 6. Open and run travel_assistant.ipynb

## Limitations ## 
- Gradio might not always work perfectly inside Jupyter. If needed, run it as a Python script.

- Scraping too many pages might get slow or hit website limits (so we cap depth and pages).

- Only tested on Mac (M1) and Linux with Python 3.8.
