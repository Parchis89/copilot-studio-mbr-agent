# Solution Architecture

## Overview

The solution implements an AI-powered Monthly Business Review (MBR) agent using Microsoft Copilot Studio and SharePoint as the enterprise knowledge source.

The agent allows users to query MBR documents stored in SharePoint and obtain answers and summaries using natural language.

## Architecture

```text
                    MBR Documents
                         │
                         ▼
                 ┌─────────────────┐
                 │   SharePoint    │
                 │                 │
                 │ DOCUMENTOS_     │
                 │ AGENTE_MBR      │
                 └────────┬────────┘
                          │
                          │ Knowledge Source
                          ▼
                 ┌─────────────────┐
                 │ Copilot Studio  │
                 │                 │
                 │    MBR Agent    │
                 └────────┬────────┘
                          │
                          ▼
                    Language Model
                          │
                          ▼
                 Business Questions
                          │
                          ▼
                 Answers & Summaries

```

## Main Components

### SharePoint

SharePoint provides the document repository used as the knowledge source for the MBR Agent.

The `DOCUMENTOS_AGENTE_MBR` folder contains the source documents used by the agent to answer questions about the Monthly Business Review.

### Copilot Studio

Microsoft Copilot Studio provides the environment used to create and configure the MBR Agent.

The agent is configured with:

- Name and description
- Instructions
- Language model
- SharePoint knowledge source

### Knowledge Source

SharePoint is configured as the enterprise knowledge source.

The agent retrieves relevant information from the indexed MBR documents before generating a response.

### Language Model

The language model interprets the user's question and generates the response.

The business information is provided by the configured knowledge source rather than being stored directly in the language model.

## Information Flow

The interaction follows these steps:

1. The user asks a question about the Monthly Business Review.
2. Copilot Studio processes the request.
3. The agent searches the configured SharePoint knowledge source.
4. Relevant information is retrieved from the MBR documents.
5. The language model interprets the available information.
6. The agent generates the response.
7. The user receives an answer or summary.

## Example Questions

- What is the Monthly Business Review?
- What KPIs are included in the MBR?
- Who is responsible for preparing the MBR?
- What information is contained in the sales report?
- Summarize the Monthly Business Review.
