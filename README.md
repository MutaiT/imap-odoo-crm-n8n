# IMAP to Odoo CRM Integration (n8n)

## Overview
Automatically creates CRM opportunities in Odoo from incoming emails via IMAP.

## Workflow
Email Trigger (IMAP) → Parse Email Data → Search Existing Leads → Check Duplicate Logic → Is Duplicate? → Create an opportunity / No Operation

## Features
- Parses contact name, email, subject, description and phone from email body
- Duplicate check based on email address and subject
- Creates opportunities directly in Odoo CRM pipeline

## Setup Requirements
- n8n instance
- Gmail account with App Password
- Odoo instance (local or cloud)

## Credentials needed
- IMAP: Gmail host, port 993, SSL, App Password
- Odoo: Site URL, database name, username, API key

## Nodes used
- Email Trigger (IMAP)
- Parse Email Data (Code node)
- Search Existing Leads (Odoo Custom Resource)
- Check Duplicate Logic (Code node)
- Is Duplicate? (IF node)
- Create an opportunity (Odoo node)
- No Operation
