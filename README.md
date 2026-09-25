# AI-Powered Monthly Business Review Agent

An AI-powered agent built with Microsoft Copilot Studio and SharePoint to help users query and summarize Monthly Business Review (MBR) information stored in enterprise documents.

## Business Problem

Monthly Business Reviews often require managers and business leaders to manually review multiple presentations and documents to identify:

- Business performance
- KPIs
- Risks
- Deals
- Team updates
- Recurring requests
- Business opportunities

This process can require significant manual effort and make it difficult to identify recurring topics across teams.

## Solution

This project implements an AI-powered MBR Agent that uses Microsoft Copilot Studio together with SharePoint as an enterprise knowledge source.

Users can interact with the agent using natural language and ask questions about the information contained in the MBR documents.

```text
MBR Documents
      │
      ▼
  SharePoint
      │
      ▼
Knowledge Source
      │
      ▼
Copilot Studio
      │
      ▼
   MBR Agent
      │
      ▼
 Language Model
      │
      ▼
Business Questions
      │
      ▼
 Answers & Summaries
