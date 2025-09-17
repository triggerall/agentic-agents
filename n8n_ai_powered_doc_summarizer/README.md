How it works?
This workflow automatically watches a Google Drive folder for new files (Google Docs or PDFs). When a document is added:

- Detects file type → Google Doc vs PDF.
- Extracts text (Google Docs via API, PDFs via text extraction).
- Summarizes & analyzes content using OpenAI.
- Sends results as a notification to Slack and/or via Email.

Who is this for?
- Business teams that want quick digests of reports, proposals, or contracts.
- Educators / researchers who need summaries of long study materials.
- Founders / managers who want daily summaries without opening every file.
- Operations teams that track compliance or documentation.

What problem is this workflow solving? / Use case
- Reading long documents is time-consuming.
- Sharing key points across teams often requires manual effort.
- Context (sentiment, action items) is often missed.
👉 This workflow solves it by auto-summarizing and notifying, making knowledge sharing instant.

What this workflow does
- Monitors Google Drive for new Google Docs or PDFs.
- Extracts document text automatically.
- Uses OpenAI to generate:
	- Title 
	- Summary 
	- Key Points
	- Suggested Action Items 
	- Language detection
	- Sentiment (positive, neutral, negative)
- Pushes output to Slack channel and/or Email inbox.

Setup Process
1. Credentials needed:
	- Google Drive (OAuth2)
	- Google Docs (OAuth2)
	- OpenAI API key
	- Slack (OAuth2) or Gmail (OAuth2)

2. Steps:
	- Connect your Google Drive → select folder to monitor.
	- Connect Google Docs API (for text extraction).
	- Add your OpenAI credentials.
	- Connect Slack or Gmail (choose your notifier).
	- Save workflow and activate.
