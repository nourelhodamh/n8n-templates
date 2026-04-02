# Leads Follow-Up — Auto Draft Generator

## How it works
1. Runs every weekday morning at 9AM
2. Reads leads from Google Sheets
3. Filters leads with no contact for 5+ days
4. Downloads meeting transcript from Google Drive
5. Uses Google Gemini to write a personalized email
6. Saves the email as a Gmail Draft for review
7. Updates lead status in the Sheet

## Required Google Sheet Columns
| Column | Description |
|---|---|
| Current status | New, Overdue, Draft Created, Sent, Closed |
| Last Contact | Date of last contact |
| Name | Lead's full name |
| Company | Lead's company name |
| Email | Lead's email address |
| Meeting Transcript | Google Drive link to transcript |
| Sales Rep | Name of the sales rep |
| FollowUp Draft Creation date | Auto-filled by workflow |

## Setup
- Google Sheets credential
- Google Drive access
- Google Gemini API key (free from Google AI Studio)
- Gmail account
- Slack workspace

## Supported file types
- PDF
- TXT

## Notes
- Emails are saved as **drafts only** — not sent automatically
- Skips leads with status: Draft Created, Sent, Closed
