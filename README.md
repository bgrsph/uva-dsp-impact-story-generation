# Research Impact Interview

UvA Data Systems Group Project: Generating Impact Stories from Research

## Team

Matt Boerio, Akira Driessen, Warren Fernandes, Buğra Sipahioğlu, Liwia Tarkowska

## Overview of the Project

A guided human-AI process for translating research into summaries that assist the creation of societal impact stories. The system conducts conversational interviews with researchers about their papers and generates structured summaries for impact narratives.

## Features

- PDF upload and automatic paper summarization 
- Interactive interview process between researcher and LLM. 
- Structured impact story generation across six sections (Note that sections are customazible within the code.)
- Revision and refinement workflow 
- Export to PDF, Word, and email formats
- Admin panel for creating and managing multiple interviews
- Progress tracking and session persistence (i.e., database integration)

## Products that were used in the project

- Python
- Streamlit for UI
- LangChain with OpenAI GPT-4 (UvA framework)
- SQLite for data persistence
- ReportLab for PDF generation
- python-docx for Word export

## Installation

```bash
pip install -r requirements.txt
```

## Configuration

Create `src/.streamlit/secrets.toml` with:

```toml
OPENAI_API_KEY = "your-api-key"
ADMIN_PASSWORD = "your-admin-password"
```

## Usage

Run the application:

```bash
streamlit run src/app.py
```

Navigate to the provided local URL.

### Admin Workflow

1. Select "Admin" role
2. Login with admin password
3. Upload research paper (PDF)
4. Share generated interview code with researcher

### Researcher Workflow

1. Select "Researcher" role
2. Enter access code
3. Answer interview questions
4. Generate and refine summary that is going to be used in an impact story by communication manager at UvA
5. Export final summary

## Impact Story Structure

- Title
- Introduction
- Societal Impact
- Research and Approach
- People and Collaboration
- Conclusion/Outlook

## Database

SQLite database stores:
- Uploaded papers and summaries
- Interview codes and states
- Conversation transcripts
- Generated stories and revision counts
