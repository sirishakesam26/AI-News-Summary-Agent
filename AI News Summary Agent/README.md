# 🤖 AI News Summary Agent

> An AI-powered news summarization workflow built with **n8n**, **Google
> Gemini**, and **Gmail** that automatically fetches the latest news,
> summarizes it using AI, and delivers the summary directly to your
> inbox on a scheduled basis.

------------------------------------------------------------------------

# 📌 Project Overview

Keeping up with daily news can be time-consuming. This project automates
the entire process by collecting the latest news articles from an RSS
feed, summarizing them using Google's Gemini Large Language Model (LLM),
and sending a concise email summary automatically.

The workflow is fully automated and requires no manual intervention
after deployment.

------------------------------------------------------------------------

# 🚀 Features

-   ⏰ Runs automatically on a predefined schedule
-   📰 Fetches the latest news from RSS feeds
-   📑 Limits the number of articles to avoid unnecessary processing
-   🤖 Generates AI-powered summaries using Google Gemini
-   📧 Sends formatted summaries directly to Gmail
-   ⚡ Fully automated using n8n workflows

------------------------------------------------------------------------

# 🛠 Tech Stack

  Technology          Purpose
  ------------------- -----------------------
  n8n                 Workflow Automation
  Google Gemini API   AI News Summarization
  Gmail API           Email Delivery
  RSS Feed            News Source
  Basic LLM Chain     AI Processing
  Schedule Trigger    Automation

------------------------------------------------------------------------

# 📂 Workflow Architecture

``` text
Schedule Trigger
        │
        ▼
RSS Feed Reader
        │
        ▼
Limit Node (Top 5 Articles)
        │
        ▼
Aggregate Node
        │
        ▼
Basic LLM Chain
        │
        ▼
Google Gemini
        │
        ▼
Gmail
```

------------------------------------------------------------------------

# ⚙️ How It Works

## Step 1 -- Schedule Trigger

The workflow starts automatically based on a predefined schedule (daily
or at any configured interval).

## Step 2 -- RSS Feed Reader

Reads the latest news articles from an RSS feed and retrieves: - Title -
Description - Publication Date - Article URL

## Step 3 -- Limit Node

Processes only the latest five articles to reduce API usage and improve
summarization quality.

## Step 4 -- Aggregate Node

Combines the selected articles into a single prompt for the LLM.

## Step 5 -- Google Gemini (LLM)

The aggregated news is sent to Google Gemini with a prompt requesting a
concise daily digest.

Example Prompt:

``` text
Summarize these news articles into a concise daily news digest.

For each article include:
- Headline
- 2–3 sentence summary
- Key highlights

Use clear and simple English.
```

## Step 6 -- Gmail

The generated summary is automatically sent to the configured Gmail
account.

Example Subject:

``` text
Daily AI News Summary
```

------------------------------------------------------------------------

# 🎯 Problem Solved

Instead of visiting multiple news websites every day, this workflow: -
Collects the latest news automatically. - Summarizes articles using
AI. - Delivers a concise digest via email. - Saves time and improves
productivity.

------------------------------------------------------------------------

# 💡 Skills Demonstrated

-   AI Workflow Automation
-   Prompt Engineering
-   Google Gemini Integration
-   API Integration
-   Gmail Automation
-   RSS Feed Processing
-   Data Aggregation
-   Scheduled Workflows
-   No-Code / Low-Code Development
-   AI Content Generation

------------------------------------------------------------------------

# 📸 Screenshots

Add your screenshots in the `images/` folder.

    images/
    ├── workflow.png
    ├── execution.png
    └── email-output.png

------------------------------------------------------------------------

# 📧 Example Output

``` text
📰 Daily News Summary

1. OpenAI launches a new AI model
Summary:
OpenAI introduced a new reasoning model with improved coding capabilities.

---------------------------------

2. Google announces Gemini updates
Summary:
Google released new Gemini features for developers and enterprises.
```

------------------------------------------------------------------------

# 📁 Project Structure

``` text
AI-News-Summary-Agent/
│
├── README.md
├── workflow/
│   └── AI-News-Summary-Agent.json
├── images/
│   ├── workflow.png
│   ├── execution.png
│   └── email-output.png
├── prompts/
│   └── summarization-prompt.txt
├── LICENSE
└── .gitignore
```

------------------------------------------------------------------------

# 🔮 Future Improvements

-   Multiple news categories
-   HTML email formatting
-   Telegram and Slack notifications
-   Google Sheets / Notion integration
-   Duplicate article removal
-   Weekly and monthly digests
-   Multi-language summaries
-   Sentiment analysis

------------------------------------------------------------------------

# 📚 Learning Outcomes

This project helped me learn: - Building AI-powered automation with
n8n - Integrating Google Gemini into workflows - Working with RSS feeds
and APIs - Designing automated email systems - Prompt engineering for
summarization - End-to-end AI workflow development

------------------------------------------------------------------------

# 📈 Project Summary

  Category       Details
  -------------- ------------------------
  Project Name   AI News Summary Agent
  Type           AI Automation
  Difficulty     Beginner--Intermediate
  Automation     Scheduled Workflow
  AI Model       Google Gemini
  Platform       n8n
  Status         ✅ Completed

------------------------------------------------------------------------

## 👨‍💻 Author

**Sirisha Srinivas**

If you found this project useful, feel free to ⭐ this repository.
