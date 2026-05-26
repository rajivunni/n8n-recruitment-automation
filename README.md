# n8n Recruitment Automation

n8n workflows that automate the end-to-end recruitment pipeline - from sourcing candidates on Apollo to parsing CVs with AI, scoring against job requirements, and generating personalised outreach.

## Workflows

### Candidate Sourcing Automation
Pulls candidate profiles from Apollo based on defined job requirements, normalises the data, scores each candidate against the role using Claude AI, filters and ranks the top 50, then generates personalised outreach emails for each.

**Stack:** Apollo API, Claude (Anthropic), Google Sheets, n8n batch processing

### CV Intake to Candidate Profile
Monitors a Gmail inbox for incoming CV emails. Extracts the attached CV, parses it with OpenAI to structured fields, maps the data, generates a personalised outreach email, and logs everything to Google Sheets.

**Stack:** Gmail Trigger, OpenAI, Google Sheets

## Tech Stack

- [n8n](https://n8n.io) - workflow automation
- Apollo - candidate sourcing
- Claude (Anthropic) - candidate scoring and outreach
- OpenAI - CV parsing
- Gmail - CV intake
- Google Sheets - candidate tracking

## Usage

1. Import the `.json` file into your n8n instance via **Workflows > Import from file**
2. Configure credentials: Apollo API key, Anthropic API key, OpenAI API key, Gmail OAuth, Google Sheets OAuth
3. Update the Set Variables node with your target job requirements
4. Activate the workflow

## About

Built by [Rajiv Unnikrishnan](https://www.rajivunnikrishnan.com) - n8n automation specialist.
