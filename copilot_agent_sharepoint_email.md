# AGENT 1: SharePoint Data Retriever + Email Trigger

## Scenario  
An agent that retrieves data from a SharePoint list/document library and sends it as an email using Outlook.

---

# Phase 1: Create the Agent

## Step 1: Sign In
- Open browser → go to https://copilotstudio.microsoft.com  
- Sign in with your Microsoft work account  

---

## Step 2: Create a New Agent
- Click **+ Create → New Agent**  
- You will see:
  - Details pane (center)
  - Conversation/Test pane (right side)

---

## Step 3: Configure Name & Description
- **Name**: SharePoint Data Email Agent  
- **Description**:  
  This agent retrieves data from SharePoint and sends insights via email to the specified recipient  
- Click **Create**  

---

## Step 4: Write Agent Instructions

Paste:

```
You are a data insights assistant. You retrieve information from the connected SharePoint knowledge source 
and help users get specific data. When asked to email data, collect the required details (query/topic and 
recipient email) and send a well-formatted email with the insights. Always present data in a clean, 
tabular format. If information is not available, clearly inform the user.
```

- Click **Save**  

---

# Phase 2: Add SharePoint as Knowledge Source

## Step 5: Add SharePoint
1. Go to **Knowledge tab**  
2. Click **Add knowledge**  
3. Select **SharePoint**  
4. Enter your SharePoint site:  
   ```
   contoso.sharepoint.com/sites/SalesData
   ```
5. Add Name and Description  
6. Click **Add to agent**  

---

## Step 6: Enable Work IQ
- Go to **Settings**  
- Turn ON **Work IQ**  
- Save  

---

# Phase 3: Enable Generative Orchestration

## Step 7: Turn ON AI Orchestration
1. Click **Settings (top-right)**  
2. Open **Generative AI**  
3. Enable:
   - Generative orchestration  
4. Set language = **English**  
5. Click **Save**  

---

# Phase 4: Add Email Tool

## Step 8: Add Outlook Email Tool
1. Go to **Tools tab**  
2. Click **+ Add a tool**  
3. Search:
   ```
   Send an email
   ```
4. Select:
   - **Send an email (V2) – Office 365 Outlook**  
5. Click **Add to agent**  
6. Authenticate  

---

## Step 9: Configure Inputs

| Input   | Fill Using   | Description |
|--------|-------------|------------|
| To     | Fill with AI | Recipient email |
| Subject| Fill with AI | Meaningful subject line |
| Body   | Fill with AI | Formatted SharePoint insights |

- Click **Save**

---

## Troubleshooting
If you get a 403 error:
- Create a Power Automate flow:
  - Trigger → Run from Copilot  
  - Action → Send Email  
  - Respond → Return to Copilot  
- Add this flow as tool  

---

# Phase 5: Create Topic

## Step 10: Create Topic
- Go to **Topics**  
- Click **+ New Topic → From blank**  
- Name:  
  ```
  Send Data via Email
  ```

---

## Step 11: Add Trigger Phrases

```
Send data details to my email
Email me the insights
Send details to outlook
Mail me the data
Email insights
```

---

## Step 12: Ask Question (Data Query)

- Add node → **Ask a question**

Text:
```
What specific data or topic would you like me to email?
```

- Identify as: User response  
- Save variable:
```
DataQuery (string)
```

---

## Step 13: Ask Question (Email Address)

- Add node → **Ask a question**

Text:
```
Please provide the recipient email address
```

- Identify as: Email address  
- Save variable:
```
RecipientEmail (string)
```

---

# Phase 6: Create Prompt (Data Retrieval)

## Step 14: Create Prompt

- Add node → **Call an action → Create a prompt**

Name:
```
Generate Data Insights
```

Instructions:

```
Based on the knowledge source data, provide a detailed summary for the query: {Topic.DataQuery}. 
Format it neatly for an email using headers, bullet points, and tabular format if relevant.
```

---

## Configure Prompt

- Input:
```
DataQuery → {x} DataQuery
```

- Knowledge source:
  - Select SharePoint  

- Output:
```
InsightsText (string)
```

---

# Phase 7: Send Email

## Step 15: Add Email Tool Node

- Add node → **Call a tool → Send an email (V2)**  

Mapping:

```
To = {x} RecipientEmail

Subject = Concatenate("Data Insights — ", Topic.DataQuery)

Body = {x} InsightsText
```

---

# Phase 8: Confirmation Message

## Step 16: Add Message

```
Email sent successfully! Check your inbox for the data insights.
```

---

# Phase 9: Test the Agent

## Step 17: Test

1. Open Test Panel  
2. Type:
```
Email me the sales data insights
```

3. Provide:
- Query → "Sales last quarter"  
- Email → your email  

---

## Expected Outcome
- Email is received  
- Data is formatted properly  
- Data is retrieved from SharePoint  
