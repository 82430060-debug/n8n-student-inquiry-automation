# Student Inquiry Automation with n8n and Local AI

An AI-powered workflow that collects student inquiries, processes them using a locally running language model, and organizes inquiry data for storage.

This project explores workflow automation and the integration of AI models with external data services using **n8n, Ollama, and Airtable**.

## Workflow Preview

![Student Inquiry Automation Workflow](<Screenshot 2026-10-15 204054.png>)

## Project Overview

Student inquiries often require repetitive data collection and processing. This project demonstrates how a visual automation workflow can connect form submissions, AI processing, and data management in one pipeline.

The workflow accepts student information and a question, passes the relevant input to an AI Agent, and integrates with Airtable to organize inquiry records.

## Features

- **Form-based input:** Collects the student's name, major, and question.
- **AI integration:** Uses an AI Agent connected to a locally running language model through Ollama.
- **Workflow automation:** Connects processing steps using n8n nodes.
- **Data management:** Integrates with Airtable to organize student inquiry records.
- **Local model execution:** Uses a local language model rather than requiring a hosted LLM API for inference.

## Technologies Used

- **n8n** — Visual workflow automation
- **Ollama** — Local language model runtime
- **SmolLM 135M** — Lightweight language model used in the project
- **Airtable** — Inquiry data storage and organization
- **Docker** — Used to run the local n8n environment

## How It Works

1. A student submits a form containing their name, major, and question.
2. The form submission enters the n8n workflow.
3. An Edit Fields node prepares the relevant data.
4. The AI Agent processes the student's question using the configured Ollama Chat Model.
5. The workflow integrates with Airtable to organize inquiry records.

## Project Structure

- `Student Information Assistant.json` — Exported n8n workflow.
- `Screenshot 2026-10-15 204054.png` — Workflow screenshot.

## Setup and Installation

### Prerequisites

- A working n8n installation
- Ollama installed and running locally
- The model used by the workflow downloaded in Ollama
- An Airtable account and configured credentials, if required by the workflow

### Steps

1. Download or clone this repository.
2. Open n8n.
3. Import `Student Information Assistant.json` into your n8n instance.
4. Ensure Ollama is running and the configured model is available.
5. Verify the Ollama connection URL and model settings in the workflow.
6. Configure your own Airtable credentials and destination table.
7. Test the workflow with a sample student inquiry.

**Important:** Connection URLs may differ depending on whether n8n and Ollama run directly on your computer or in separate Docker containers. Configure the URL for your actual environment.

## Limitations

- The response quality depends on the selected language model and its capabilities.
- The lightweight model may produce incomplete or inaccurate answers.
- The workflow requires appropriate configuration of its local services and external integrations.
- AI-generated responses should be reviewed before being used for important academic guidance.

## Future Improvements

- Add input validation and error handling.
- Improve response quality through prompt engineering and model evaluation.
- Add sample test cases to assess the quality and consistency of generated answers.
- Expand inquiry categorization and data management.
- Explore a knowledge base containing verified academic information.

## Learning Objectives

This project provides practical experience with visual workflow automation, AI-agent integration, local language model deployment, and connecting AI workflows to external data services.
