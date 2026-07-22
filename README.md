# Real-Estate-AI-CRM
# 🏡 AI-Powered Real Estate CRM Automation

An AI-powered CRM automation workflow built using **n8n**, **Google Gemini AI**, **JavaScript**, and **Google Sheets** to automate real estate lead management. The workflow captures incoming leads, validates data, scores lead quality using AI, generates an intelligent summary, and stores the processed lead in Google Sheets.

---

# 📌 Features

- ✅ Capture leads using Webhook
- ✅ Normalize lead data
- ✅ Validate required fields
- ✅ AI-powered lead scoring
- ✅ Priority classification (High / Medium / Low)
- ✅ AI-generated lead summary
- ✅ Store processed leads in Google Sheets
- ✅ Fully automated workflow using n8n

---

# 🛠 Tech Stack

| Technology | Purpose |
|------------|---------|
| n8n | Workflow Automation |
| Google Gemini | AI Lead Analysis |
| JavaScript | Data Validation & Processing |
| Google Sheets | CRM Database |
| Webhook | Lead Collection |
| JSON | Data Exchange |

---

# 📂 Project Structure

```
real-estate-ai-crm-automation/
│
├── README.md
├── LICENSE
├── .gitignore
│
├── workflow/
│   └── real-estate-ai-crm.json
│
├── screenshots/
│   ├── workflow.png
│   ├── ai-output.png
│   ├── google-sheet.png
│   ├── webhook-test.png
│   └── execution.png
│
└── docs/
    └── architecture.png
```

---

# 🔄 Workflow

```
Webhook
   │
   ▼
Normalize Lead Data
   │
   ▼
Validate Lead Data
   │
   ▼
Google Gemini AI
   │
   ▼
Parse AI Response
   │
   ▼
Google Sheets CRM
```

---

# 📊 AI Lead Analysis

The AI analyzes every lead using the following information:

- Budget
- Property Type
- Purchase Timeline
- Customer Message

The model generates:

- Lead Score (0–100)
- Priority
- AI Summary

---

# 🧠 Lead Scoring Logic

## Budget

| Budget | Score |
|---------|-------|
| Above 1 Crore | +30 |
| 50 Lakhs – 1 Crore | +20 |
| Below 50 Lakhs | +10 |

## Timeline

| Timeline | Score |
|----------|-------|
| Immediate | +30 |
| 1 Month | +25 |
| 3 Months | +15 |
| More than 3 Months | +5 |

## Property Type

| Property | Score |
|----------|-------|
| Villa | +20 |
| Apartment | +15 |
| Plot | +10 |

---

# 📥 Sample Input

```json
{
  "name": "John Smith",
  "email": "john@gmail.com",
  "phone": "9876543210",
  "city": "Hyderabad",
  "budget": "80 Lakhs",
  "property": "3 BHK",
  "timeline": "1 month",
  "message": "Need apartment immediately",
  "source": "Website"
}
```

---

# 📤 Sample Output

```json
{
  "lead_score": 75,
  "priority": "High",
  "ai_summary": "John Smith is a high-intent lead looking for a 3 BHK apartment in Hyderabad with a budget of 80 Lakhs. He requires a property within one month and has expressed immediate urgency."
}
```

---

# 📸 Screenshots

## Workflow

> Add screenshot here

```
screenshots/workflow.png
```

---

## AI Lead Analysis

> Add screenshot here

```
screenshots/ai-output.png
```

---

## Google Sheets CRM

> Add screenshot here

```
screenshots/google-sheet.png
```

---

## Successful Workflow Execution

> Add screenshot here

```
screenshots/execution.png
```

---

# 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/real-estate-ai-crm-automation.git
```

### 2. Import Workflow

Open **n8n**

Import

```
workflow/real-estate-ai-crm.json
```

### 3. Configure Credentials

Connect:

- Google Gemini API
- Google Sheets OAuth

### 4. Execute Workflow

Send a POST request to the Webhook with lead information.

The workflow will:

- Validate the data
- Analyze the lead using AI
- Generate Lead Score
- Generate Priority
- Generate AI Summary
- Save the lead in Google Sheets

---

# 💼 Business Benefits

- Reduces manual lead qualification
- Prioritizes high-value customers
- Improves response time
- Automates CRM updates
- Provides AI-assisted decision making
- Scalable low-code workflow

---

# 🔮 Future Enhancements

- Email notifications for high-priority leads
- WhatsApp integration
- CRM integration (HubSpot/Salesforce)
- Dashboard with lead analytics
- Duplicate lead detection
- Sales agent assignment
- Database integration (PostgreSQL/MySQL)

---

# 👨‍💻 Author

**Shashank Adepu**

B.Tech Artificial Intelligence & Machine Learning

---

# ⭐ If you found this project useful, consider giving it a Star!
