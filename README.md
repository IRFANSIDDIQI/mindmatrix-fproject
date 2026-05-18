# 🐑 Grama-Vaxi — Digital Livestock Health Card & AI Assistant

> **MindMatrix VTU Internship Program** | **Project Title:** 23
> *An AI-powered web ecosystem engineered for rural environments to track livestock life cycles, secure community herd health, and bridge communication gaps with automated, localized alerting.*

---

## 📱 Features

* **🐾 Animal Ledger:** Register local village livestock with an intuitive, highly visual, icon-driven interface designed intentionally for rural accessibility.
* **📅 Vaccine Calendar & Alerts:** Automated tracking workflows that calculate **"Next Shot"** targets and broadcast persistent camp timelines (e.g., *“Doctor arriving at Temple Square tomorrow”*).
* **🧠 GenAI Disease Analysis:** Fully integrated with the **Gemini 1.5 Flash API** to handle real-time symptom logging and deliver immediate first-aid/triage recommendations.
* **📊 Health Trends Dashboard:** High-density, interactive **Bento-style grids** displaying real-time regional livestock populations and historical vaccine coverage metrics.
* **🌐 Localized UI Architecture:** Built-in localization architecture with comprehensive **Kannada language support** to systematically remove technical and language barriers for farmers.

---

## 🏗️ Technical Stack Breakdown

| Layer | Technology Used | Purpose |
| --- | --- | --- |
| **Frontend** | `React 19` + `TypeScript` | Houses core application logic, strict state boundaries, and explicit type safety. |
| **Styling** | `Tailwind CSS 4.0` | Powers the modular bento layout systems, custom fluid margins, and responsive grids. |
| **Animations** | `Motion (Framer Motion)` | Drives organic, ultra-smooth visual transitions when navigating between the Ledger and Dashboard. |
| **Visuals** | `Recharts` | Renders lightweight, scalable canvas tracking for animal demographic and coverage data. |
| **Backend** | `kotlin` | Functions as a dedicated local server proxy layer to keep production API integrations secure. |
| **AI / ML** | `Gemini 1.5 Flash` | Handles natural language prompt pipelines to deliver instantaneous veterinary triage summaries. |
| **Icons** | `Lucide-React` | Delivers high-contrast, universally recognizable visual indicators for non-text navigation. |

---

## 🚀 How to Run

**open terminal then**
`cd (file name)`
`npm install`
`npm run dev`

> 💡 **System Note:** Launch your local browser instance and map to `http://localhost:3000`. Toggle or verify layout components to inspect standard responsive breakpoints and Kannada string file adjustments.

---

## 📂 Project Structure

```text
Grama-Vaxi/
├── 📁 src/                  # Frontend Source Code Layer
│   ├── App.tsx             # Main Layout Core, View Routers, & State Synchronization
│   ├── main.tsx            # Application Compilation Entry Point
│   ├── types.ts            # Explicit Data Blueprint Models (Animals, Alerts, Logs)
│   └── index.css           # Custom Typography Imports & Bento Grid Layout Tokens
├── 📁 dist/                 # Static Production Target Output (Auto-Generated)
├── server.ts               # Backend Express Server Engine (Secures Gemini Proxies & Routing)
├── package.json            # Framework Dependencies, Config Meta, & Execution Scripts
├── tsconfig.json           # Global Compiler Directives for TypeScript Strict Enforcement
├── vite.config.ts          # Core Asset Bundler Optimization Pipelines
├── .env                    # Target Environment Variables & Protected Application Credentials
└── PROJECT_REQUIREMENTS.md # Internship Compliance Guidelines & Project Scope Checklists

```

---

## 🎯 Impact Goals

* **🛡️ Protecting Livestock Wealth:** Drastically lowering localized animal mortality rates during unexpected outbreaks to protect the essential "living savings accounts" of rural farming communities.
* **🩺 Elevating Animal Welfare Standards:** Streamlining day-to-day access to accurate, AI-backed veterinary health triage insights while striving for **100% regional vaccination coverage**.
* **📊 Accelerating Rural Digitization:** Migrating traditional, easily missed loudspeaker schedules or paper tracking frameworks into an instantly accessible, visual ledger system.
