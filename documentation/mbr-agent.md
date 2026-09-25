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
