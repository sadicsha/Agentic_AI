# RetailWise — AI Retail Assistant

RetailWise is a conversational AI assistant designed to answer common retail questions about products, inventory, pricing, discounts, promotions, orders, and returns. The project uses a visual workflow to connect user input, prompt instructions, a language model, chat output, and message-history components.

## Project Goal

Provide quick, easy-to-understand guidance for retail-related questions. For example, RetailWise can explain what to consider before offering a discount, how to think about excess inventory, or what factors may affect a promotion.

## Example Question

**What factors should a retailer consider before offering a discount?**

The example response mentions product cost, profit margin, customer demand, competitor prices, stock levels, and the expected increase in sales. A discount is worthwhile only when the additional sales can compensate for lower profit per item.

## Workflow

1. **Chat Input** receives the user's question.
2. **Message History — Retrieve** provides stored conversation context, if configured.
3. **Prompt Template** defines the RetailWise role and the topics it should handle.
4. **Language Model** generates an answer. The supplied screenshot shows `openai/gpt-oss-20b` selected.
5. **Chat Output** displays the response.
6. **Message History — Store** receives the response for possible use in later turns.

## Components

- Chat Input
- Prompt Template
- Language Model
- Chat Output
- Message History retrieval and storage

## How to Use

1. Open the workflow in the environment where it was created.
2. Confirm the language-model provider and credentials are configured.
3. Enter a retail-related question in the Playground.
4. Run the flow and review the response.
5. Ask a follow-up question to test whether message history works as intended.

## Example Questions

- What factors should a retailer consider before offering a discount?
- How can a retailer reduce excess inventory?
- What should be checked before launching a promotion?
- How can a retailer respond to an increase in product returns?
- What data is needed to determine whether a discount was profitable?

## Limitations

- The screenshots show a prompt-based assistant, not a verified live connection to a retailer's inventory or sales database.
- Real-time stock, pricing, order, or return information must not be assumed unless a relevant data source is connected.
- Model responses can be inaccurate; verify important business decisions against actual data.
- Message-history behavior depends on the component settings and storage configuration.

## Suggested Repository Structure

```text
retailwise-ai-retail-assistant/
├── README.md
├── RetailWise_Project_Documentation.docx
└── screenshots/
    ├── retailwise-chat-interface.png
    ├── retailwise-node-graph.png
    └── retailwise-workflow.png
```

## Author

**Sadicsha Khandait**

## Summary

RetailWise demonstrates how a visual AI workflow can turn a retail question into a natural-language response. It can be extended with trusted product data, inventory integrations, pricing analytics, and business-specific safeguards.
