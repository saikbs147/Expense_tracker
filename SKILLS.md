---
name: expense-tracker
description: Track personal expenses by category and amount. Add new expenses like "food - 150" or "travel - 200", view a full expense summary table, or check total spending.
---

# Expense Tracker

## Instructions

When the user wants to add an expense, view expenses, or check spending:

1. Call the `run_js` tool with the following exact parameters:
   - script name: index.html
   - data: A JSON string with the following fields:
     - action: String. One of "add", "view", or "clear".
     - category: String. The expense category (e.g. "food", "travel", "date"). Required when action is "add".
     - amount: Number. The expense amount in currency. Required when action is "add".
     - note: String. Optional note or description for the expense.

### Examples

- User says "food - 150" → action: "add", category: "food", amount: 150
- User says "travel 200 for cab" → action: "add", category: "travel", amount: 200, note: "cab"
- User says "show my expenses" or "how much did I spend" → action: "view"
- User says "clear all expenses" → action: "clear"

After the script returns its result, summarize what was added or show the spending breakdown as described in the result.
