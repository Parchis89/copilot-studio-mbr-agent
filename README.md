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

```

## Key Capabilities

- Query MBR documents using natural language.
- Retrieve information from SharePoint.
- Generate concise answers based on the available documentation.
- Summarize Monthly Business Review information.
- Support questions about KPIs, sales information, responsibilities and business topics.
- Provide a conversational interface to enterprise information.

## Technologies

- Microsoft Copilot Studio
- SharePoint
- Microsoft 365
- Large Language Model (LLM)
- Knowledge Grounding

## Architecture

The solution separates the conversational model from the enterprise knowledge source.

The language model is responsible for interpreting the user's question and generating the response, while SharePoint provides the business information used to ground the response.

For more details, see:

- [Solution Architecture](documentation/architecture.md)

## Example Questions

The agent can answer questions such as:

> What is the Monthly Business Review?

> What KPIs are included in the MBR?

> Who is responsible for preparing the MBR?

> What information is contained in the sales report?

> Summarize the Monthly Business Review.

## Project Status

**Status:** Prototype / Learning Project

The current implementation focuses on knowledge retrieval and conversational interaction with MBR documents stored in SharePoint.

Future iterations could extend the solution with additional automation, actions, analytics and business workflows.

