# SQL-Powered Data Analysis with CrewAI and LangChain

## Overview
This project sets up an AI-powered workflow to analyze SQL databases using CrewAI, LangChain, and OpenAI's GPT-4o-mini. It automates SQL queries, data analysis, and report generation by leveraging AI agents.

## Features
- SQL Database Setup: Converts an Excel/CSV file into an SQLite database.
- OpenAI GPT-4o-mini Integration: Uses OpenAI’s LLM for intelligent data processing.
- LangChain Tools: Provides tools for listing tables, fetching schemas, and executing SQL queries.
- CrewAI Agents & Tasks: Automates SQL querying, data analysis, and report writing using AI agents.

## Installation
Ensure you have Python installed, then install the required dependencies:

```bash
pip install -U transformers langchain langchain-community langchain-experimental 'crewai[tools]' langchain_groq
```

## Setup
1. **Set up an SQLite database from a Titanic dataset:**

- Reads a CSV file.
- Stores it in an SQLite database.

2. **Configure OpenAI API:**
- Set your API key as an environment variable.

3. **Define LangChain SQL tools:**
- list_tables(): Lists available tables.
- tables_schema(): Retrieves table schemas.
- execute_sql(): Runs SQL queries.

4. **Load Agents & Tasks from YAML files.**

5. **Create CrewAI Agents:**
- sql_dev: Handles SQL execution.
- data_analyst: Performs data analysis.
- report_writer: Summarizes insights.

6. **Run an AI-powered analysis pipeline:**
- Extract data → Analyze → Write report.


## File Structure
```bash
📂 project-root
 ┣ 📜 agents.yaml          # Agent configurations
 ┣ 📜 tasks.yaml           # Task definitions
 ┣ 📜 titanic.csv          # Sample dataset
 ┣ 📜 master_db.db         # SQLite database
 ┣ 📜 script.py            # Main execution script
 ┣ 📜 crew.log             # Execution logs
 ┗ 📜 README.md            # Project documentation
```

## Dependencies
- Python 3.8+
- LangChain
- CrewAI
- OpenAI GPT-4o-mini
- Pandas & SQLAlchemy for database management