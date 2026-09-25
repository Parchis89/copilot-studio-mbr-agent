# Business Case

## Business Problem

Monthly Business Reviews (MBR) require business leaders to review information coming from multiple teams and documents.

The information may include:

- Business updates
- Sales performance
- KPIs
- Deals
- Risks
- Obstacles
- Requests and escalations

When this information is distributed across multiple presentations and documents, the review process becomes time-consuming and makes it difficult to identify recurring topics and patterns.

## Current Situation

In a traditional MBR process, leaders may need to manually:

1. Review multiple team presentations.
2. Identify relevant business updates.
3. Extract risks and obstacles.
4. Identify recurring requests.
5. Compare information across teams.
6. Prepare a consolidated summary for management.

The reference scenario describes an organization preparing a regional sales review using presentations from more than 10 team leaders. A director may spend several hours reviewing the material and preparing a consolidated summary.

## Proposed Solution

The proposed solution is an AI-powered MBR Agent built with Microsoft Copilot Studio.

The agent connects to MBR documents stored in SharePoint and allows users to interact with the information using natural language.

Instead of manually searching through multiple documents, users can ask questions such as:

- What is the Monthly Business Review?
- What KPIs are included in the MBR?
- Who is responsible for preparing the MBR?
- What information is contained in the sales report?
- Summarize the Monthly Business Review.

## Solution Approach

The solution uses SharePoint as the enterprise knowledge source for the agent.

```text
Multiple MBR Documents
          │
          ▼
      SharePoint
          │
          ▼
   Knowledge Source
          │
          ▼
    MBR Agent
          │
          ▼
 Natural Language Query
          │
          ▼
   Answer / Summary
