# MBR Agent

## Overview

The MBR Agent is a conversational AI agent built with Microsoft Copilot Studio.

It uses SharePoint as a knowledge source to provide answers about Monthly Business Review (MBR) documents.

The agent was designed to allow business users to query MBR information using natural language instead of manually searching through multiple documents.

## Knowledge Repository

The MBR source documents are stored in a dedicated SharePoint folder:

```text
DOCUMENTOS_AGENTE_MBR
```

The laboratory uses multiple MBR source files stored in SharePoint as the knowledge base for the agent.

The documents are indexed by Copilot Studio and made available as a knowledge source.

## Agent Configuration

The agent was created in Microsoft Copilot Studio with the following configuration:

| Property | Configuration |
|---|---|
| Agent name | MBR Agent |
| Platform | Microsoft Copilot Studio |
| Knowledge source | SharePoint |
| Content | MBR documents |
| Interaction | Natural language |
| Language model | Configured LLM |

## Agent Architecture

```text
User
 │
 │ Natural Language Question
 ▼
┌─────────────────────┐
│   Copilot Studio    │
│                     │
│      MBR Agent      │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ Knowledge Source    │
│                     │
│     SharePoint      │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│   MBR Documents     │
│                     │
│ DOCUMENTOS_AGENTE_  │
│ MBR                  │
└──────────┬──────────┘
           │
           ▼
      Relevant Information
           │
           ▼
      Language Model
           │
           ▼
       Agent Response
```
## Agent Instructions

The agent is configured to act as a corporate assistant specialized in Monthly Business Reviews.

The instructions define how the agent should behave when responding to users.

The agent should:

- Answer questions using the configured MBR knowledge source.
- Provide clear and concise responses.
- Avoid inventing information that is not available in the source documents.
- Indicate explicitly when the requested information cannot be found.
- Use the available documentation as the basis for its responses.

## Knowledge Configuration

The SharePoint knowledge source is connected to the `DOCUMENTOS_AGENTE_MBR` folder.

During the initial configuration, Web Search is disabled.

This configuration allows the prototype to be validated using the enterprise MBR documentation before introducing information from public Internet sources.

## Knowledge Indexing

The MBR documents must be indexed before testing the agent.

The knowledge source should display a `Ready` status before performing validation tests.

If indexing is still in progress, the agent may return incomplete answers or indicate that information cannot be found even though the documents have already been uploaded.

## Validation

The agent is tested using questions related to the MBR documentation.

Example validation questions:

- What is the Monthly Business Review?
- What KPIs are included in the MBR?
- Who is responsible for preparing the MBR?
- What information is contained in the sales report?
- Summarize the Monthly Business Review.

The same questions can also be tested in Spanish to validate the multilingual interaction capabilities of the agent.

## Validation Process

The validation process follows these steps:

1. Confirm that the SharePoint knowledge source is available.
2. Verify that the knowledge source status is `Ready`.
3. Ask questions related to the MBR documents.
4. Review the generated answers.
5. Verify that the answers are grounded in the available documentation.
6. Adjust the agent instructions when necessary.
7. Repeat the tests.

## Important Design Principle

The agent is not simply a language model.

The solution combines:

```text
Language Model
      +
Agent Instructions
      +
Enterprise Knowledge
      │
      ▼
   MBR Agent
