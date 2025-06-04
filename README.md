# SQL Agents: Agentic AI for Automated Query Generation and Database Interaction

## 🚀 Overview

This project presents a modular, intelligent framework for converting natural language (NL) queries into executable SQL queries using Agentic AI principles. Built with **LangChain**, **LangGraph**, and **SQLDatabaseToolkit**, it allows users—including non-technical professionals—to interact with multi-format enterprise databases effortlessly.

## 🧠 Key Features

- 🔍 **Natural Language to SQL**: Converts user queries into accurate SQL statements using Llama 3.1 (8B) LLM via Ollama.
- 🗂 **Multi-format Support**: Handles `.csv`, `.xlsx`, `.xls`, and `.db` files and converts them to normalized SQL databases.
- 📊 **Schema-aware Generation**: Uses Jaccard Similarity for selecting the most relevant schema elements.
- 🧩 **Modular Agentic Workflow**: Implements modular nodes using LangGraph for stateful and scalable automation.
- ✅ **Validation and Execution**: Validates generated queries and executes them securely on selected databases.
- 🤖 **Chatbot Integration**: Provides human-readable responses, enhancing usability for non-experts.
- 🔐 **Privacy-first**: Fully local deployment using Ollama, ensuring data security and compliance.

## 🛠️ Architecture

1. **LLM Initialization**: Deterministic setup of Llama 3.1 using Ollama.
2. **File Processing**: Converts structured files into SQLite databases.
3. **Schema Retrieval**: Fetches tables, columns, and metadata using `InfoSQLDatabaseTool` & `ListSQLDatabaseTool`.
4. **Query Generation**: Generates SQL using LLM with schema context.
5. **Validation & Execution**: Uses `QuerySQLCheckerTool` and `QuerySQLDatabaseTool`.
6. **Natural Language Output**: LLM converts result into a user-friendly answer.
