# SCIT Payment Reminder & Reconciliation Agent

An AI-assisted payment reminder workflow built with **Zapier Agents, Google Sheets, and Gmail**. It is designed to read invoice records, identify pending payments, send reminder emails, find payment-related replies, and update the matching spreadsheet row according to the configured rules.

## Project Overview

The Google Sheet named **SCIT Invoice** acts as the invoice register. It contains fields such as Invoice ID, Type, Name, Amount, Account No, Bank Name, and Status. The Zapier agent uses Gmail and Google Sheets tools to help coordinate payment follow-up.

## Workflow

1. Read invoice rows from the `SCIT Invoice` Google Sheet.
2. Identify records marked `Pending` and skip records already marked `Completed`.
3. Send a reminder email to the intended recipient.
4. Find and review incoming email replies for payment confirmation and transaction/reference details.
5. Match the reply to the correct invoice using reliable identifiers.
6. Update only the corresponding spreadsheet row when the configured confirmation rules are satisfied.

## Example Data

| Invoice ID | Type | Name | Amount | Bank | Status |
|---|---|---|---:|---|---|
| 1001 | Maintenance | Madhav | ₹50,000 | Axis | Pending |
| 1002 | Project | Ram | ₹28,000 | HDFC | Completed |
| 1003 | Maintenance | Pavan | ₹45,000 | SBI | Pending |
| 1004 | Project | Raj | ₹7,450 | Kotak | Pending |

These are sample values visible in the project screenshots. Check the live sheet before relying on them.

## Tools Used

- **Zapier Agents** — agent instructions and workflow orchestration.
- **Google Sheets** — invoice register and payment status.
- **Gmail: Send Email** — sends payment reminders.
- **Gmail: Find Email** — searches for relevant replies.
- **Google Sheets: Update Spreadsheet Row(s)** — updates the matching record.
- **Default Tools: Visit Site & Web Search** — available to the agent, although not central to the payment workflow shown.

## Setup Steps

1. Create a Google Sheet with unique invoice IDs and consistent status values.
2. Open Zapier Agents and create or open the payment reminder agent.
3. Connect Google Sheets and select the `SCIT Invoice` spreadsheet and correct worksheet.
4. Connect Gmail and configure the Send Email and Find Email tools.
5. Configure the Google Sheets row-update tool to target the correct row using a unique invoice identifier or row ID.
6. Add the invoice sheet as a knowledge source if needed by your agent configuration.
7. Write agent instructions for reading pending invoices, sending reminders, matching replies, and updating statuses.
8. Test with sample records and a test mailbox before using real invoice data.

## Important Controls

- Do not change a row already marked `Completed`.
- Match each reply to the correct invoice before updating a row.
- A message claiming payment is not, by itself, proof that funds have settled.
- Use human review or an approved verification process for uncertain cases.
- Protect account numbers, customer email addresses, and financial details.
- Never commit passwords, API keys, or private credentials to GitHub.

## Limitations

- Email replies may be incomplete, misleading, or sent from an unexpected address.
- Search and AI interpretation may make mistakes.
- A spreadsheet status is not bank settlement confirmation.
- The exact behavior depends on the agent instructions, tool configuration, permissions, and trigger settings.

## Suggested Repository Structure

```text
zapier-payment-reminder-agent/
├── README.md
├── documentation.docx
└── screenshots/
    ├── initial-google-sheet.png
    ├── reminder-email.png
    ├── payment-reply.png
    ├── agent-tools.png
    └── agent-configuration.png
```

## Author

**Sadicsha Khandait**

## Conclusion

This project demonstrates how an AI agent can help coordinate payment reminders and spreadsheet updates using Zapier, Gmail, and Google Sheets. It aims to reduce repetitive follow-up work while keeping invoice records organized. Reliable invoice matching and payment verification remain important before changing a financial status.
