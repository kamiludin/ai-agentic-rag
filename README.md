# Agentic RAG Chatbot with n8n and Supabase

Mastering Agentic RAG in n8n: Build a Chatbot That Plans, Thinks, and Answers

## Introduction

Despite the impressive capabilities of Retrieval-Augmented Generation (RAG), traditional RAG-based chatbots face serious limitations in real-world applications. They often:

- Retrieve document chunks without deep understanding.
- Struggle with numerical or tabular data.
- Fail to connect insights across multiple documents.
- Treat every query the same without tool or strategy selection.

**Traditional RAG** is like a smart librarian who finds books but doesn’t fully understand your question. **Agentic RAG** is like an assistant who not only finds the right books but also reads, analyzes, compares facts, and uses the right tools to deliver the best answer.

In this project, we introduce **planning**, **reasoning**, **memory**, and **tool selection** into the RAG process. The chatbot acts more like an intelligent agent — thinking before answering.

This repository shows you how to build an **Agentic RAG chatbot** from scratch using **n8n**, **Supabase**, **PostgreSQL**, and **Telegram**.

---

## Key Features

- 🧪 **Agentic RAG**: Combines retrieval, reasoning, planning, and decision-making.
- 📱 **Telegram Bot**: Interface for asking questions and receiving intelligent responses.
- 📊 **Supports Tabular and Text Documents**: Handles PDFs, Docs, Excel, and CSV files.
- 🛠️ **SQL Query Support**: Allows powerful tabular queries using PostgreSQL.
- 📆 **Memory Handling**: Supports conversation history and context awareness.

---

## How to Run

1. **Set up Supabase database** with the required tables (documents, document_metadata, document_rows).
2. **Set up n8n** (self-hosted or cloud).
3. **Configure Google Drive credentials** to access uploaded files.
4. **Configure Telegram Bot** via [BotFather](https://t.me/BotFather).
5. **Import n8n workflows** provided in this repo.
6. **Run ingestion flow** to populate your vector database.
7. **Start the Agentic RAG workflow** and chat with your intelligent assistant via Telegram.

---

## Notes

- For tabular queries, **always refer to `document_metadata` first** to ensure the correct dataset ID (`id` column) and exact schema match.
- Column names in SQL queries **must match exactly** (case-sensitive and spelling) to the schema.
- If the answer is not found, the chatbot will say: _"Sorry, I couldn't find what you were looking for in any document."_
- There may occasionally be inaccuracies due to the chunking strategy used — this is an area for potential improvement, which will be discussed in a future article.


## Demo Video

https://youtu.be/Qb5f2bVdB7Y?si=ULSh6Mxlo7vS7F2c


Thank You...
