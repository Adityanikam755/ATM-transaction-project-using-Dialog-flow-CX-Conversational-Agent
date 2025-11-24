📌 Overview

Aditya ATM is a conversational AI agent built using Dialogflow CX designed to simulate and automate common ATM interactions through natural language. The agent helps users perform ATM-related tasks such as checking account balance, cash withdrawal, mini statement, card issues, PIN reset, and more — all through a smooth, human-like conversational experience.

This project demonstrates how Dialogflow CX can be used to build a full banking assistance flow, integrating with backend APIs or mock data, while following secure and structured banking dialogs.

🎯 Key Features
✔ 1. Balance Inquiry Flow

Collects necessary user authentication parameters (card number, account type).

Verifies user identity through PIN or OTP (optional extension).

Returns the real-time or mock account balance.

✔ 2. Cash Withdrawal Flow

Allows users to request withdrawal amounts.

Validates amount (min/max ATM limits).

Confirms the transaction before dispensing (or simulating) cash.

✔ 3. Mini Statement Flow

Fetches last few transactions from backend or sample data.

Displays date, type, and amount in structured form.

✔ 4. Card & ATM-Related Issue Handling

Lost card reporting

Card blocked status check

Incorrect PIN attempts

Request for new/duplicate card

✔ 5. PIN Reset Flow

Handles PIN reset or PIN change requests.

Can be integrated with backend to send OTP or generate temporary PIN.

✔ 6. Fallback & Repair Mechanisms

Handles unexpected user inputs gracefully.

Redirects the user back to the correct flow smoothly.

Provides clear prompts and confirmations.

🏗 Project Architecture
🔹 Dialogflow CX Components

Flows:

Main Flow

Balance Inquiry Flow

Cash Withdrawal Flow

Mini Statement Flow

Card Issues Flow

PIN Reset Flow

Fallback Flow

Intents:

check_balance

withdraw_cash

mini_statement

pin_reset

card_block

fallback_default

provide_card_number

provide_amount

provide_pin

Entities:

card_number

amount

pin

account_type

issue_type

Backend Integration (Optional)

You may connect the agent with:

Banking APIs

Custom authentication API

Mock data services

Webhook fulfillment for performing transactions or responses dynamically

🧩 How It Works
Step 1: User Starts Conversation

The user triggers the agent with something like:

"I want to withdraw cash"
"What is my account balance?"
"I lost my ATM card"

Step 2: Agent Collects Required Parameters

Card number

Account type

PIN

Withdrawal amount

Issue category

Step 3: Validations

Check if card number format is valid

Check if PIN is correct (via webhook or mock validation)

Ensure withdrawal amount is within limits

Step 4: Action Fulfillment

Once inputs are validated, the agent:

Retrieves data

Processes withdrawal

Prints a mini statement

Logs a complaint

Resets PIN

Step 5: Confirmation & Completion

The agent summarizes actions and closes the session.

🧪 Testable Demo Scenarios
Scenario 1 — Check Balance

User: What is my balance?
Agent: Please enter your card number.
User: 1234 5678 9876 5432
Agent: Please enter your PIN.
...
Agent: Your current balance is ₹25,450.

Scenario 2 — Withdraw Cash

User: I want to withdraw 2000 rupees.
Agent: Please enter your card number.
...
Agent: Transaction successful. Please collect your cash.

Scenario 3 — Report Lost ATM Card

User: I lost my card.
Agent: I’m sorry to hear that. Do you want to block your card now?

📁 Technology Stack
Component	Technology
Conversational Engine	Dialogflow CX
Logic Execution	Webhook (Node.js / Python optional)
Data Source	API / Mock JSON
Deployment	GCP Project
🚀 Installation / Import Instructions

Go to Dialogflow CX Console

Create a new agent

Navigate to Agent Settings → Export & Import

Select Import Agent

Upload the provided export file (Aditya ATM.blob)

Deploy and test

📈 Future Enhancements

Integration with real banking APIs

Multi-language support

Voice-enabled ATM assistant

Fraud detection & unusual activity alerts

Cash deposit simulation

Biometric authentication (Face/Fingerprint)
