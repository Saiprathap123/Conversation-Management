
# Conversation Management & Classification using Groq API

## Overview

This project implements two core tasks utilizing the Groq API with OpenAI-compatible SDK:

- **Task 1:** Managing conversation history with summarization and truncation.
- **Task 2:** JSON schema-based classification and information extraction from user chats.

The solution is implemented in a Google Colab notebook using standard Python without any additional frameworks.

---

## Features

### Conversation Management

- Maintains a **running conversation history** between user and assistant.
- Supports **customizable truncation**:
  - Limit by number of conversation turns.
  - Limit by character length.
- Implements **periodic summarization** after every *k*-th conversation run to keep history concise.
- Demonstrates the system with sample conversations and varying truncation settings.

### JSON Schema Classification & Extraction

- Defines a **JSON schema** to extract structured user details:
  - Name, Email, Phone, Location, Age.
- Uses **Groq API function calling** for structured extraction.
- Validates extracted data and cleans it into standardized formats.
- Demonstrates extraction on multiple sample chat inputs.

---

## Setup & Usage

### Prerequisites

- Python 3 environment
- Groq API account and API key ([Get API Key here](https://console.groq.com))
- Git for version control (optional but recommended)

### Installation

```
pip install groq
```

### API Key Configuration

Set your Groq API key securely as an environment variable before running the notebook:

- Linux/Mac:
  ```
  export GROQ_API_KEY="your_api_key_here"
  ```
- Windows (PowerShell):
  ```
  setx GROQ_API_KEY "your_api_key_here"
  ```
- Or set it programmatically in the notebook:
  ```
  import os
  os.environ["GROQ_API_KEY"] = "your_api_key_here"
  ```

### Running the Notebook

- Open the provided Google Colab notebook.
- Run all cells sequentially to see:
  - Groq API chat model responses.
  - Conversation management with truncation and periodic summarization.
  - JSON schema-based structured information extraction from sample chats.

---

## Repository Structure

- `ConversationManagement.ipynb` – Complete Google Colab notebook with full implementation.
- `README.md` – This documentation file.
- `.gitignore` – For excluding unnecessary files from version control.

---

## Key Code Components

- `ConversationManager` class: Manages chat history, truncation, and summarization.
- `extract_user_info(text)`: Calls Groq API function calling for JSON extraction.
- `validate_extracted_info(data)`: Cleans and validates extracted user details.
- Sample chat inputs demonstrating features and outputs.

---

## Notes & Best Practices

- API keys **should never be hardcoded** and must be stored securely.
- Be mindful of API usage limits and costs when running large numbers of requests.
- The implementation uses only standard Python and avoids frameworks as per assignment guidelines.
- Modular, clean, and well-documented code ensures easy extensibility.

---

## License

This project is provided for academic purposes. Use responsibly as per Groq API terms and conditions.

---

## Contact

For questions or further assistance, please reach out via GitHub Issues or contact the developer.

---

# Thank you for reviewing this project!

```
