# Recipe Generator Chatbot with RAG (Retrieval-Augmented Generation)

**"AI Recipe Master: A Chatbot with RAG-Powered Recipe Retrieval"**

## Overview

This project demonstrates how to build a recipe generator chatbot using Retrieval-Augmented Generation (RAG). The chatbot can fetch recipes from a local database or perform web searches to provide users with accurate and relevant cooking instructions. This step-by-step guide uses Langflow to simplify the integration of multiple components like chat inputs, agents, and databases.

---

## Features

- **User-Friendly Interaction** : Chat-based interface for recipe queries.
- **RAG Integration** : Combines database retrieval and generative AI for robust recipe fetching.
- **Dynamic Search** : Automatically switches to web search if the recipe is not available in the local database.
- **Database Integration** : Uses AstraDB to store and retrieve recipe data efficiently.
- **Customizable Agents** : Configurable agents to handle information retrieval and processing.

---

## Prerequisites

Before starting, ensure you have the following installed:

- **Python 3.8+**
- **Langflow** : [Langflow Installation Guide](https://github.com/logspace-ai/langflow)
- **AstraDB Account** : Sign up at [AstraDB](https://www.datastax.com/astra)
- **API Access** : Gemini API or any web-search API for external information retrieval.
- **Other Libraries** : Install dependencies listed in `requirements.txt`.

---

## Setup Instructions

### 1. Clone the Repository

```bash
$ git clone https://github.com/your-username/recipe-generator-rag.git
$ cd recipe-generator-rag
```

### 2. Install Dependencies

```bash
$ pip install -r requirements.txt
```

### 3. Configure Environment Variables

Create a `.env` file in the root directory and add the following:

```env
ASTRADB_ID=<your-astradb-client-id>
ASTRADB_SECRET=<your-astradb-client-secret>
WEB_API_KEY=<your-web-search-api-key>
LANGFLOW_API_KEY=<your-langflow-api-key>
```

### 4. Setup AstraDB

- Create a database named `recipes`.
- Add a table with fields for recipe name, ingredients, and steps.

---

## Step-by-Step Workflow

### 1. Setup

- Sign up or log in to Langflow.
- Create a new project flow and name it `Recipe Generator`.

### 2. Creating Inputs/Outputs

- **Inputs** : Add a chat input node to capture user queries.
- **Outputs** : Add a text output node to display chatbot responses.

### 3. Agent Configuration

- Use Langflow to create agents.
- Connect tools for database retrieval and web search API integration.

### 4. Database Integration

- Link the chatbot to AstraDB using Langflow's database tool.
- Ensure queries to AstraDB return accurate recipe details.

### 5. Functional Testing

- Query the chatbot with example inputs like:
  - "How do I make a chocolate cake?"
  - "What's a good recipe for pasta salad?"
- Validate responses from both the database and web search.

---

## Usage

### Run the Chatbot

```bash
$ streamlit run ./main.py
```

### Example Query

**User** : "How do I make garlic bread?"

**Chatbot** : "To make garlic bread, you will need: ... [recipe details fetched from database or web]"

---

## Screenshots

### Langflow Architecture

Here is the visual representation of the Langflow workflow used to build the chatbot:

![Langflow Architecture]![1736099390443](image/README/1736099390443.png)
![1736099366500](image/README/1736099366500.png)

### Chatbot Output

Example of chatbot interaction in the Streamlit UI:

![1736099433219](image/README/1736099433219.png)
![1736099445665](image/README/1736099445665.png)

---

## Langflow Playground

Explore the Langflow playground with a live demo:

[Langflow Playground Demo](https://astra.datastax.com/langflow/62f7f0d1-631b-449d-a892-b475e8114ed1/flow/a17833e2-2c48-4065-800e-839a451c1d2b)

---

## Acknowledgements

- **Langflow** for simplifying AI workflow management.
- **AstraDB** for robust database services.
- **OpenAI** for powering generative responses.

---

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
