# Agentic Financial Research Assistant

## About the Project

This project is something I built to explore how AI agents can make working with financial documents easier.

Financial reports can be quite lengthy, and finding specific information in them often takes time. So I wanted to build an assistant where users can simply ask questions about a financial PDF and get answers based on its content.

I also wanted to go beyond basic question answering. The assistant can perform mathematical calculations and convert currencies using different tools. It automatically decides which tool to use depending on what the user asks.

The project combines Retrieval-Augmented Generation (RAG) with a LangChain agent and conversation memory.

## What Can It Do?

- **Ask questions about PDF documents:** Get answers from financial documents without manually searching through every page.
- **Find relevant information:** Uses Hugging Face embeddings and ChromaDB to retrieve relevant text.
- **Perform calculations:** Uses a calculator tool to solve mathematical expressions.
- **Convert currencies:** Uses an external exchange-rate API to convert currencies.
- **Choose tools automatically:** The agent understands the user's request and selects the appropriate tool.
- **Remember conversations:** Maintains conversation history using LangGraph.
- **Keep conversations separate:** Uses different thread IDs to maintain independent user sessions.

## Technologies Used

| Technology | How I used it |
|---|---|
| Python | Main programming language |
| LangChain | Building the agent and integrating tools |
| Google Gemini | Generating responses |
| Hugging Face | Creating text embeddings |
| ChromaDB | Storing and retrieving document embeddings |
| LangGraph | Managing conversation memory |
| PyPDF | Extracting text from PDF documents |
| Exchange-rate API | Currency conversion |

## How I Built It

The project follows a few main steps:

1. **Loading the document:** I used PyPDF to load a financial PDF document.
2. **Splitting the text:** The document was divided into smaller chunks so that relevant information could be retrieved more easily.
3. **Generating embeddings:** Hugging Face embeddings were used to convert the text into numerical representations.
4. **Storing the data:** ChromaDB was used as the vector database.
5. **Building the RAG tool:** The system retrieves relevant document content and uses Gemini to generate answers.
6. **Creating the agent:** I integrated three tools: RAG, calculator and currency converter.
7. **Adding memory:** LangGraph's InMemorySaver maintains conversation history and keeps different user sessions separate.

## Example Queries

**Document-based questions**
- What is the purpose of an annual report?
- Why is cash flow analysis important?

**Calculations**
- What is (15.5 × 24) / 3.2?

**Currency conversion**
- Convert 100 USD to INR.

**Conversation memory**
- What is my name?
- What were my previous questions?

## Project Structure

```text
Agentic-Financial-Research-Assistant/
│
├── Agentic_Financial_Research_Assistant.ipynb
└── README.md
```

## How to Run the Project

The project was developed and tested in Google Colab.

1. Download or clone this repository.
2. Open the notebook in Google Colab.
3. Add your Gemini API key to Colab Secrets using the name `PROJECT_KEY`.
4. Upload the financial PDF to Google Drive and update its path in the notebook if needed.
5. Run the notebook cells in order.
6. Try the example queries to test the different tools.

**Requirements:** A Gemini API key and an internet connection for currency conversion.

## Future Improvements

There are a few things I'd like to explore further:

- Building a simple interface using Streamlit.
- Supporting multiple PDF documents.
- Improving document retrieval and answer quality.
- Adding more useful tools for financial analysis.
- Deploying the assistant so it can be accessed through a web application.

## About Me

**Ronit Wadkar**

MSc Data Science Student

[GitHub Profile](https://github.com/ronit9805)
