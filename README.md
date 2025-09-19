Developer Recruitment Tasks
This repository contains the solutions for three developer recruitment tasks, demonstrating skills in web scraping, automation, and bot development. Each task has been implemented and tested, with artifacts stored in structured formats as specified. Below is an overview of each task, along with setup and execution instructions.
Repository Structure

Task 1: Automation in Make.com to generate random contacts in Airtable, create a company summary using ChatGPT, store it in a Google Doc, and send a daily report to a Slack channel.
Task 2: YouTube Scraper to extract video details and store them in JSON, Excel, and Google Sheets.
Task 3: Slack Bot ("Report Bot") integrated with Make.com to send weekly reports to a private Slack channel.
Reports: Documentation for each task is included in the docs/ directory:
YouTube_Scraper_Report.md
Slack_Bot_Report.md
Make_Airtable_Automation_Report.md (to be generated separately)



Task 1: Make.com Automation with Airtable, ChatGPT, Google Docs, and Slack
Objective
Create an automation in Make.com that:

Generates a list of random contacts in Airtable with Name, Email, and Company Name.
Uses ChatGPT to generate a company summary.
Stores the summary in a Google Doc with the company name and summary text.
Sends a daily report to a Slack channel at 7:00 AM.

Implementation

Airtable: A table was created to store random contacts with fields for Name, Email, and Company Name.
ChatGPT: Integrated via Make.com to generate a summary for each company.
Google Docs: A new document is created for each company summary, containing the company name and summary text.
Slack: A daily report is sent to a specified Slack channel at 7:00 AM IST, summarizing the contacts and company details.
Make.com: A scenario was set up to automate the process, triggered daily via a scheduler.

Artifacts

Airtable base with contact data.
Google Docs containing company summaries.
Slack messages with daily reports.
Report: docs/Make_Airtable_Automation_Report.md (to be provided).

Task 2: YouTube Scraper
Objective
Develop a scraper to extract YouTube video details (title, channel name, description, publish date, view count) and store them in JSON, Excel, and Google Sheets.
Implementation

YouTube Data API: Used to fetch video metadata.
Storage:
JSON file (youtube_data.json) for raw data.
Excel file (youtube_data.xlsx) for tabular data.
Google Sheets for online access and collaboration.


Error Handling: Managed API quotas, invalid video IDs, and data formatting issues.

Artifacts

youtube_data.json: Raw data in JSON format.
youtube_data.xlsx: Structured data in Excel format.
Google Sheet with video details.
Report: docs/YouTube_Scraper_Report.md.

Task 3: Slack Bot with Make.com Integration
Objective
Create a Slack bot named "Report Bot" and connect it to Make.com to send weekly reports to a private Slack channel with the format:
Weekly Report:
Leads Contacted: 2345
Replied: 56
Meetings Booked: 4
Positive Replies: 12

Implementation

Slack Bot: Created "Report Bot" using the Slack API with chat:write permissions.
Make.com: Configured a scenario to trigger weekly, sending the report with the exact metrics provided.
Private Channel: Ensured the bot was invited to the target channel for message delivery.

Artifacts

Slack bot ("Report Bot") configured and operational.
Make.com scenario for weekly report automation.
Report: docs/Slack_Bot_Report.md.



