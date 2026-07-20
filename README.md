# AI ATS Resume Matcher

An AI-powered ATS (Applicant Tracking System) Resume Matcher built using **n8n**, **Groq LLM**, **Docker**, **PostgreSQL**, and **AWS EC2**.

The application automatically compares a candidate's resume against a job description scraped through linkedin, generates an ATS compatibility score, identifies missing skills, and records structured recommendations in a google sheet.

---

## 🚀 Features

- 📄 Resume parsing
- 💼 Job description analysis
- 🤖 AI-powered ATS scoring using Groq LLM
- 📊 Skill gap identification
- ⭐ Match score generation
- 🐳 Dockerized deployment
- 🔒 HTTPS with Let's Encrypt
- ☁️ Self-hosted on AWS EC2
- 🗄️ PostgreSQL for workflow persistence

---

# ⚙️ Workflow

The workflow performs the following steps:

1. Receive a resume and job description via webhook.
2. Extract resume content.
3. Extract or receive job description via linkedin.
4. Send both inputs to Groq LLM.
5. Generate:
   - ATS Score
   - Match Summary
   - Missing Skills
6. Filter results based on configurable score threshold.
7. Record in a google sheet

---

# 🛠 Tech Stack

| Category | Technology |
|-----------|------------|
| Automation | n8n |
| AI | Groq LLM |
| Cloud | AWS EC2 |
| Nginx |
| Database | PostgreSQL |
| Containerization | Docker |
| SSL | Let's Encrypt |
| DNS | DuckDNS |

---

# 📦 Deployment

The application is deployed on an AWS EC2 instance using Docker Compose.