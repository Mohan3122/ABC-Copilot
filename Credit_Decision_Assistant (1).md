# Credit Decision Assistant (High Impact)

## Architecture of the Unified Agent

The unified agent orchestrates **4 internal specialized capabilities**:

- **Credit Memo Summarizer** – Extract key insights from credit proposals (Users: Credit Analysts, Approvers)
- **Risk Signal Detector** – Identify financial and qualitative risks (Users: Risk Teams, Underwriters)
- **Policy Advisor** – Validate decisions against credit policies (Users: Credit Managers, Compliance)
- **Underwriting Assistant** – Recommend credit decisions and structuring options (Users: Underwriters, Senior Approvers)

The user interacts with **one unified agent**, which dynamically applies the right capability.

## Why This Combination?

These 4 capabilities cover the end-to-end credit decision workflow:

1. Understanding the case (Memo Summary)
2. Identifying risks (Risk Detection)
3. Ensuring compliance (Policy Validation)
4. Driving decision-making (Underwriting Support)

✅ Delivers complete decision intelligence, not just analysis.

## Unified Agent Responsibilities

### 1. Summarize Credit Memos
- Extract borrower profile (individual/company) and loan purpose
- Summarize financials (revenue trends, profitability, key ratios such as DSCR and leverage)
- Capture loan structure, collateral details, and proposed decision

**Output:**
- Case summary
- Financial highlights
- Decision snapshot

### 2. Detect Risk Signals
- Identify financial risks (declining revenue, high leverage, weak cash flows)
- Detect qualitative risks (industry stress, customer concentration, management concerns)
- Flag inconsistencies across documents and unrealistic projections

**Output:**
- Key risk indicators
- Red flags
- Risk severity (Low / Medium / High)

### 3. Validate Policy Compliance
- Compare case against credit policies, including eligibility norms, exposure limits, and sector restrictions
- Detect policy breaches and deviations
- Suggest required approvals and structuring adjustments

**Output:**
- Compliance status (Compliant / Deviation)
- Deviation list
- Recommendations for alignment

### 4. Underwriting Decision Support
- Generate borrower risk profile based on financial strength, industry outlook, and repayment capacity
- Recommend credit decisions:
  - Approve (standard terms)
  - Approve with conditions (collateral, covenants, pricing)
  - Restructure (tenure, EMI, limits)
  - Decline
- Suggest structuring improvements such as adjusting amount/tenure, adding collateral or guarantees, and introducing covenants
- Highlight key decision drivers, approval concerns, and manual review triggers

**Output:**
- Underwriting recommendation
- Risk-adjusted decision logic
- Suggested loan structuring
- Approval conditions / covenants

## End-to-End Output

- Case Summary
- Risk Assessment
- Policy Compliance Check
- Underwriting Recommendation
- Key Approval Concerns
- Decision Support Insights

## Example Queries

- Summarize this case and highlight risks
- Is this proposal aligned with policy?
- What are the key approval concerns?
- Should we approve this loan?
- Suggest better structuring for this case
- What conditions should we apply before approval?

## Business Impact

- Faster credit approvals
- Better risk visibility
- Strong policy adherence
- Consistent underwriting decisions
- Reduced dependency on senior reviewers
