# 🛡️ PayShield AI
### Intelligent Payment Protection & AI-Powered Customer Support

**Understand Risks Early. Navigate Payment Issues Smarter.**

PayShield AI is an AI-powered financial support platform designed to help freelancers, merchants, and digital payment users understand potential payment issues before they happen and navigate payment holds through intelligent assistance.

It combines payment-readiness guidance, explainable risk indicators, AI-powered customer support, smart escalation, and complaint tracking into one platform.

**Live Demo:** https://payshield-ai-lyart.vercel.app/

---

## 🌟 Key Features

### 1. Pre-Payment Readiness
- Collects simulated transaction information.
- Evaluates transaction context using transparent risk rules.
- Identifies potential payment friction before a transaction.
- Provides practical recommendations.

### 2. Explainable Risk Insights
- Generates Low, Medium, or High attention levels.
- Displays the factors contributing to each risk indicator.
- Explains why a transaction scenario requires attention.
- Provides actionable payment-readiness guidance.

### 3. Payment Hold Explanation
- Helps users understand payment holds and pending transactions.
- Explains notification messages in simple language.
- Separates known information from unknown information.
- Recommends appropriate next steps.

### 4. AI Support Copilot
- Understands payment-related questions.
- Identifies support categories and user concerns.
- Provides contextual assistance.
- Asks relevant follow-up questions.
- Summarizes conversations.

### 5. Smart Escalation
- Prepares structured support cases.
- Captures issue details and actions already attempted.
- Identifies situations requiring human assistance.

### 6. Complaint Tracking
- Displays submitted support cases.
- Tracks complaint reference numbers and statuses.
- Provides visibility into the support journey.

---

## 🛠️ Technology Stack

| Component | Technology |
|---|---|
| Frontend | React.js |
| Build Tool | Vite |
| Styling | Tailwind CSS |
| Backend | Node.js, Express.js |
| Database | Supabase PostgreSQL |
| Payment Platform | PayPal Developer Platform |
| Payment Testing | PayPal Sandbox |
| AI | Configurable LLM integration |
| Knowledge Retrieval | Curated support knowledge base |
| Deployment | Vercel |
| Version Control | Git and GitHub |

*The stack above follows the project architecture. Confirm the actual packages and integrations in the source code before treating every item as implemented.*

---

## 💳 PayPal Integration

PayShield AI is designed to integrate with the PayPal Developer Platform using its free Sandbox environment.

### PayPal Sandbox

The Sandbox provides a testing environment for payment workflows without processing real-money transactions.

Our intended integration uses:

- PayPal Developer Dashboard to create a Sandbox application.
- Sandbox client credentials for application authentication.
- PayPal Sandbox APIs for supported payment-testing workflows.
- Simulated transaction information for the risk-awareness engine.

### Integration Setup

1. Visit https://developer.paypal.com/
2. Sign in to your PayPal Developer account.
3. Open the Apps & Credentials section.
4. Select Sandbox.
5. Create a Sandbox application.
6. Obtain the Client ID and Secret.
7. Configure the credentials in the backend environment.

### Environment Variables

Keep credentials on the server. Never expose the PayPal Secret in frontend code.

Example backend `.env`:

```env
PORT=5000

PAYPAL_CLIENT_ID=your_sandbox_client_id
PAYPAL_CLIENT_SECRET=your_sandbox_client_secret
PAYPAL_BASE_URL=https://api-m.sandbox.paypal.com

SUPABASE_URL=your_supabase_url
SUPABASE_SERVICE_ROLE_KEY=your_supabase_service_role_key

AI_API_KEY=your_ai_provider_api_key
AI_MODEL=your_ai_model_name
```

**Important:** The actual PayPal API operations and AI provider must match the implementation in the submitted code. The roadmap allows a simulated payment flow when an approved PayPal integration is unavailable.

---

## 🤖 AI Integration

Artificial intelligence is the intelligence layer of PayShield AI.

### AI-Powered Customer Support

The language model is intended to:

- Understand natural-language payment questions.
- Identify user intent.
- Explain payment-related issues.
- Generate contextual recommendations.
- Summarize support conversations.
- Prepare structured escalation cases.

### Explainable Risk Assessment

The risk-awareness engine uses synthetic transaction features, including:

- New account age bands.
- Unusual transaction amounts.
- Incomplete seller information.
- Sudden sales-volume changes.
- Missing fulfilment details.

It produces an attention level and identifies the exact simulated factors contributing to that result.

### Retrieval-Augmented Generation (RAG)

A curated support knowledge base is used to retrieve relevant information before generating policy-related answers.

This approach is intended to reduce unsupported responses and improve the reliability of customer assistance.

**AI Provider:** Configure the actual provider and model used by the implementation. The project roadmap does not specify a particular LLM provider.

---

## 🏗️ System Architecture

```text
             USER
               |
               v
       PayShield AI Frontend
          React + Vite
               |
               v
        Node.js + Express
               |
       +-------+--------+
       |       |        |
       v       v        v
   PayPal    AI Engine  Supabase
   Sandbox   + RAG      Database
       |       |        |
       v       v        v
  Payment   Support   Cases &
  Testing   Guidance  Transactions
       |       |
       +---+---+
           |
           v
    Risk Insights &
    Support Workflow
           |
           v
     Human Escalation
```

---

## 🚀 Getting Started

### Prerequisites

Install the following:

- Node.js (LTS version)
- npm
- Git
- A Supabase account
- PayPal Developer Sandbox account (for PayPal integration)
- API credentials from the AI provider (for AI integration)

### 1. Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### 2. Navigate to the Project

```bash
cd YOUR_PROJECT_FOLDER
```

### 3. Install Dependencies

For the frontend:

```bash
npm install
```

For the backend, if it is maintained separately:

```bash
cd server
npm install
```

### 4. Configure Environment Variables

Create `.env` files using the environment variable examples above.

Add your actual credentials locally.

Never commit `.env` files to GitHub.

### 5. Start the Backend

```bash
cd server
npm run dev
```

### 6. Start the Frontend

Open another terminal:

```bash
npm run dev
```

### 7. Open the Application

Visit:

```text
http://localhost:5173
```

*Commands and directory names should be adjusted to match the actual repository structure and available npm scripts.*

---

## 🔐 Security and Responsible AI

PayShield AI follows a privacy-conscious design approach.

- Uses synthetic transaction data for demonstration scenarios.
- Does not request passwords, OTPs, or complete card numbers.
- Does not claim access to PayPal's internal risk engine.
- Does not guarantee payment-hold prevention or removal.
- Distinguishes verified information from unknown details.
- Recommends human assistance for complex or high-impact cases.
- Keeps sensitive API credentials on the backend.

---

## 🎯 Future Enhancements

- Deeper integration with authorized PayPal Sandbox APIs.
- Advanced explainable risk-awareness models.
- Multilingual AI customer support.
- Real-time case notifications.
- Human-agent support dashboard.
- Improved knowledge retrieval and source references.
- More comprehensive payment scenario testing.

---

## 👥 Project Information

**Project Name:** PayShield AI

**Hackathon:** PayPal AI Hackathon 2026 – Build What's Next with PayPal and AI

**Category:** AI-Powered FinTech / Payment Protection

**Live Application:** https://payshield-ai-lyart.vercel.app/

---

## 💙 Our Vision

We believe digital payments should be more than fast and convenient. Users should also understand what is happening with their money and know what to do when something goes wrong.

PayShield AI aims to bring proactive payment guidance and intelligent customer support together to create a more transparent and confident digital payment experience.

**PayShield AI – Understand Risks Early. Navigate Payment Issues Smarter.**
