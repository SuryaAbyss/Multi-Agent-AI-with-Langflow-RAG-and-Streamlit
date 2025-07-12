# 🧠 Multi-Agent AI System using Langflow, RAG, and Streamlit

This project is a real-world, Python-based AI system that utilizes **Langflow**, **Retrieval Augmented Generation (RAG)**, and **Streamlit** to build a **multi-agent customer support assistant**. It retrieves and reasons over both structured (CSV) and unstructured (PDF) company data to provide accurate responses to customer queries.

---

## 🚀 Features

- 🔁 **Multi-Agent Architecture**: Manager agent routes user queries to specialized sub-agents (e.g., FAQ Agent, Order Lookup Agent).
- 🧩 **Langflow Integration**: Visual flow builder for AI logic with easy export/import of JSON flows.
- 📄 **Document & Data Processing**: Supports uploading PDFs and CSVs for knowledge ingestion.
- 🔍 **Retrieval-Augmented Generation (RAG)**: Uses vector search to embed and retrieve relevant information.
- 🧠 **Context-Aware Query Handling**: Dynamically fills prompts using parsed JSON results and user input.
- 🌐 **Streamlit Frontend**: Clean UI for chat interaction with the AI assistant.
- 🔐 **Environment Variable Management**: Keeps API keys and configuration secure.

---

## 🛠 Tech Stack

| Tool           | Purpose                            |
|----------------|------------------------------------|
| Python         | Backend logic                      |
| Langflow       | Visual AI workflow builder         |
| Streamlit      | Chat-based UI                      |
| Astra DB       | Vector storage and search          |
| PDF & CSV      | Data ingestion and retrieval       |
| RAG            | Context-aware answer generation    |

---

## 📁 Project Structure

.
├── flows/
│ └── customer_support_flow.json # Langflow flow export
├── data/
│ ├── orders.csv # Sample structured order data
│ ├── products.csv # Sample product catalog
│ └── support_docs.pdf # PDF file with FAQs or policy data
├── main.py # Streamlit app
├── api.py # Python API calls to Langflow
├── .env # Environment variables (API keys, config)
├── requirements.txt # Dependencies
└── README.md # This file


---

## ⚙️ Setup Instructions

### 1. Clone the Repository


2. Install Dependencies
bash
Copy
Edit
pip install -r requirements.txt
3. Set Environment Variables
Create a .env file in the root directory:

LANGFLOW_API_KEY=your_api_key
LANGFLOW_ENDPOINT=https://your-langflow-instance.com/run
⚠️ Do not commit this file to version control.

4. Run the Streamlit App

streamlit run main.py
💡 How It Works
User Query ➝ Sent to Langflow API

Manager Agent ➝ Decides if it’s an FAQ or Order Lookup

Sub-Agent ➝ Retrieves data using RAG from documents or databases

Final Response ➝ Returned and displayed in Streamlit UI

🧪 Example Use Cases
"What is the return policy?"

"Where is my order with ID ORD-1234?"

"Can I cancel an order after shipping?"

📤 Exporting and Sharing Flows
Flows created in Langflow can be exported as JSON:

In Langflow, click Export Flow.

Save the .json file to /flows.

Share or reuse in other Langflow instances.

📝 Future Enhancements
🧾 Add payment and refund processing agents

🌍 Connect to real-time shipping APIs

🤖 Enhance agent logic with LangGraph or Agentic chains

🧱 Add authentication for user-specific queries

📜 License
This project is open-source and available under the MIT License.
