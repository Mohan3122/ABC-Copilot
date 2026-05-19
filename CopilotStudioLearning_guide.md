# Complete Microsoft Copilot Studio Training Guide — Morningstar Org

---

## Part 1: What is Microsoft Copilot Studio?

Microsoft Copilot Studio (formerly Power Virtual Agents) is a low-code/no-code SaaS platform for building AI-powered agents. It integrates with Power Automate, Power Apps, Dataverse, and Microsoft 365 Copilot to enable enterprise automation and intelligent workflows.

### Key Capabilities

- Grounded Answers: Agents can search connected sources such as SharePoint, documents, and websites to generate contextual responses.
- Actions & Automation: Agents can interact with business systems, trigger workflows, and perform operations using connectors.
- Multi-Channel Publishing: Agents can be deployed across Teams, SharePoint, websites, Power Pages, and custom apps.
- Generative AI Orchestration: The platform dynamically selects topics, tools, and knowledge based on user intent.

---

## How It Differs from Traditional Chatbots

| Aspect | Traditional Chatbot | Copilot Studio Agent |
|--------|-------------------|---------------------|
| Logic | Fixed decision trees & keyword matching | Dynamic reasoning using AI models |
| Responses | Pre-written templates | Generated dynamically using data and context |
| Actions | Very limited | Can perform real actions via APIs and workflows |
| Handling Unknowns | "I don't understand" | Attempts to reason and respond intelligently |
| Learning | Static | Context-aware and adaptive |

---

## Part 2: Copilot Studio UI — Complete Walkthrough

### Access

- Open browser → https://copilotstudio.microsoft.com
- Sign in using Microsoft work or school account

### UI Structure

The platform is organized into 4 major stages:

- Create
- Customize
- Deploy
- Manage

### Home Screen Components

- Environment Selector: Select the environment for storing agents
- Create Button: Start a new agent
- Describe Area: Create agents using natural language
- Agentic Automations: Direct entry into agent creation

### Agent Editor Layout

- Left Panel: Overview, Topics, Knowledge, Tools, Analytics, Channels, Settings
- Center Panel: Main configuration area
- Right Panel: Test panel for real-time conversation

### Key Tabs

| Tab | Purpose |
|-----|--------|
| Overview | Agent configuration, instructions, prompts |
| Knowledge | Add SharePoint, files, websites |
| Topics | Define conversation flows |
| Tools | Add connectors and automation |
| Analytics | Monitor performance |
| Channels | Publish the agent |
| Settings | Configure AI, authentication, language |

---

## Part 3: Agent Instructions

Instructions define how the agent behaves.

### Best Practices

- Role: Define what the agent does
- Tone: Keep it professional and concise
- Response Style: Provide answer first, then details
- Boundaries: Define limitations and escalation paths
- Privacy: Avoid unnecessary sensitive data requests
- Consistency: Use organization-specific terminology

---

## Part 4: Knowledge Sources (RAG)

Agents retrieve information from connected sources and use it to generate responses.

### Supported Sources

| Source | Use Case |
|--------|---------|
| SharePoint | Internal docs and policies |
| Files | PDFs, Word, Excel |
| Websites | External knowledge |
| Dataverse | Structured data |
| Connectors | External systems |
| Azure AI Search | Advanced retrieval |

### Adding SharePoint Knowledge

1. Go to Knowledge tab
2. Click Add knowledge
3. Select SharePoint
4. Enter SharePoint URL
5. Add name and description
6. Click Add to agent

---

## Part 5: Topics

Topics define conversation logic.

### System Topics

Built-in topics that handle common scenarios:

- Conversation Start
- Fallback
- Escalation
- Error handling
- Authentication

### Custom Topics

Used for business logic:

- Trigger phrases
- Questions
- Variables
- Conditions
- Actions

### Orchestration Modes

- Generative: AI selects logic dynamically
- Classic: Fixed rule-based flow

---

## Part 6: Connectors & Tools

### Connector Capabilities

- Connect to business systems
- Enable automation
- Integrate APIs

### Tool Types

| Tool Type | Description |
|----------|------------|
| Connectors | Ready integrations |
| Power Automate | Workflow automation |
| HTTP APIs | External services |
| Agent Flows | AI-driven workflows |

### Event Triggers

Agents can be triggered automatically by:

- SharePoint item creation
- File uploads
- Planner task completion
- Scheduled triggers

---

## Part 7: Publishing & Channels

### Supported Channels

- Microsoft Teams
- SharePoint
- Web apps
- Power Pages
- Copilot Chat

### Publishing Steps

1. Go to Channels
2. Select channel
3. Configure settings
4. Deploy agent

---

## Part 8: Settings & Configuration

### Key Settings

| Setting | Purpose |
|--------|--------|
| Generative AI | Enable orchestration |
| Authentication | Configure access |
| Model Selection | Choose AI model |
| Work IQ | Improve knowledge retrieval |
| DLP Policies | Control data access |

---

## Part 9: Analytics & Monitoring

### Metrics

| Metric | Description |
|-------|-------------|
| Resolution Rate | Query success rate |
| CSAT | User satisfaction |
| Abandon Rate | Drop-offs |
| Deflection | Reduced support load |
| Source Usage | Data utilization |
| Conversation Logs | Interaction review |
