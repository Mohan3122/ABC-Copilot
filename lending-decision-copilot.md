# Lending Decision Copilot

## Architecture of the Unified Agent

The unified agent should orchestrate these 3 internal specialized agents:

| Internal Agent                  | Purpose                                 | Primary Users         |
|--------------------------------|------------------------------------------|----------------------|
| Eligibility Assessment Agent   | Loan qualification and policy checks     | RMs, Credit Analysts |
| Document Intelligence Agent    | Document validation and extraction       | Operations Team      |
| Underwriting Support Agent     | Risk observations and borrower summaries | Underwriters         |

👉 The user interacts with **ONE unified agent only**  
👉 Internally, the agent decides which capability to use  

---

## Why These 3 Agents?

These 3 functions cover nearly **80–90% of day-to-day lending operations**:

1. Eligibility checking  
2. Document verification  
3. Underwriting preparation  

✅ This creates **maximum operational value with minimum complexity**  

---

## Unified Agent Responsibilities

### 1. Assess Eligibility
- Check policy compliance  
- Validate age / income / FOIR / LTV  
- Recommend suitable products  
- Flag policy deviations  

### 2. Review Documents
- Identify missing documents  
- Extract borrower information  
- Validate KYC completeness  
- Compare uploaded values with application details  

### 3. Support Underwriting
- Generate borrower summaries  
- Highlight risk indicators  
- Prepare underwriting notes  
- Recommend manual review areas  

---

## Recommended Agent Flow

### Example User Flow

### Step 1
RM uploads borrower documents.

### Step 2 — Document Intelligence Agent
- Extracts borrower details  
- Identifies missing documents  
- Validates KYC  

### Step 3 — Eligibility Agent
- Calculates FOIR  
- Checks policy eligibility  
- Evaluates LTV  
- Reviews bureau score  

### Step 4 — Underwriting Support Agent
- Generates risk summary  
- Creates underwriting notes  
- Highlights policy exceptions  

### Step 5 — Final Output to User
- Eligibility status  
- Missing documents  
- Risk observations  
- Next actions  

---
