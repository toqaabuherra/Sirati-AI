# Sirati AI

An automated recruitment platform and career development ecosystem that bridges the gap between job seekers and recruitment technologies. The system automates the job search workflow, simulates ATS screenings, and provides market-driven career insights using Gemini models and n8n backend automation.

## Core Features

- ATS Simulation and CV Analysis: Parses uploaded resumes to evaluate parsing accuracy, compute compatibility scores, and identify missing keywords against target job descriptions.
- Automated Job Matching: Periodically monitors and extracts relevant vacancies from platforms like Akhtaboot, evaluates role alignment using AI, and delivers targeted digests directly to candidate inboxes.
- AI CV Content Assistant: Suggests high-impact professional summaries and tailored experience sections based on candidate background data.
- HR Screening Pipeline: Automates corporate intake workflows by pre-evaluating applicants and generating structured evaluation reports for hiring teams.
- Market Skill Discovery: Tracks and ranks the top 15 in-demand skills for target roles to guide skill-building decisions.

## Architecture and Workflows

The architecture connects a modern client interface to backend processing pipelines via n8n automation workflows and LLM endpoints:

- Client Interface: Communicates with backend endpoints through webhook triggers.
- n8n Automation Engine: Orchestrates asynchronous workers, manages web scraping routines, and controls data transformations.
- AI Processing Layer: Leverages the Gemini API for structured data extraction, text parsing, and candidate-job semantic scoring.
- Database and Storage: Persists user configuration, execution logs, and matched job records.

## Technology Stack

- Frontend: HTML5, CSS3, JavaScript, React, Bootstrap 5
- Backend: PHP 8, JSON Webhooks
- Automation: n8n Workflow Automation Engine
- AI Integration: Gemini API
- Database: MySQL

## Setup Instructions

1. Clone the repository to your local environment.
2. Configure environment credentials in your n8n instance, including Gemini API keys and email transport details.
3. Import the workflow JSON configurations located in the workflows directory into n8n.
4. Deploy the frontend code to a web server and configure webhook URLs to point to your active n8n webhooks.
