# Student Inquiry AI Assistant Workflow (n8n & Airtable)

Hey there! This is a small automation project I built to handle student inquiries automatically using n8n, Airtable, and a local AI model. 

# What it does:
1. **Form Submission:** Students fill out a simple form with their name, major, and question.
2. **AI Agent:** An LLM processes the query and generates a personalized, major-specific response.
3. **Airtable Integration:** Everything (including the AI's response) gets saved neatly into an Airtable database.

# Tech Stack:
- n8n (running via Docker)
- Airtable (with Typecast enabled)
- Ollama (Local LLM / AI Agent)

# How to use it:
1. Download the `Student Information Assistant.json` file from this repo.
2. Import it into your n8n workflow editor.
3. Connect your own Airtable and Ollama credentials, and you're good to go!
