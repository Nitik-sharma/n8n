# Assignment Report: Upwork Automation Lead Gen

## 1. Issues Identified & Fixed
- **Issue:** Data overlap from previous runs. 
- **Fix:** Implemented a filter node using `$now.minus(6, 'hours')` to ensure only the newest jobs are processed.
- **Issue:** AI response variability.
- **Fix:** Enforced "JSON Output" mode in the GPT-4o node to ensure Airtable parsing never fails.

## 2. Sample Scored Jobs
1. **Title:** "n8n automation for CRM" | **Score:** 10 | **Priority:** High.
2. **Title:** "AI Agent Developer (Retell/Twilio)" | **Score:** 10 | **Priority:** High.
3. **Title:** "Simple Data Entry" | **Score:** 2 | **Priority:** Low.
4. **Title:** "Zapier to n8n migration" | **Score:** 8 | **Priority:** Medium.
5. **Title:** "Looking for Python script" | **Score:** 5 | **Priority:** Medium.

## 3. Mandatory Enhancements
- **Slack Alerts:** Added a Slack node that triggers only when `priority == High`.
- **Pre-Filtering:** Added a filter to remove any jobs with a budget under $50 before sending to AI.
