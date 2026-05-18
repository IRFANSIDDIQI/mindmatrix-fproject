# 🐏 Grama-Vaxi — Livestock Health & Vaccination Passport
**MindMatrix VTU Internship Program** | **Project Title: 98**

An Android-based "Digital Health Card" designed for rural livestock farmers. It tracks the vaccination lifecycle of sheep, goats, and cattle, sends automated camp alerts, and provides AI-powered disease diagnostics to prevent livestock loss.

---

## 📱 Features

| Feature | Description |
| :--- | :--- |
| **🐏 Animal Ledger** | Register animals with photo, breed, age, and unique ID tracking. |
| **📅 Vaccine Calendar** | Automatically generates "Next Shot" dates and tracks medical history. |
| **🔔 Camp Alerts** | Smart notifications for government vaccination camps arriving in the village. |
| **🤖 AI Disease Alert** | Integrated Gemini AI to analyze symptoms and provide first-aid advice. |
| **🌐 Multilingual** | Full support for **Kannada** and English to serve rural populations. |
| **📴 Offline First** | Built with Room DB to ensure functionality in areas with poor connectivity. |
| **🚀 Reliable Alerts** | Uses WorkManager for background notifications even if the app is closed. |

---

## 🏗️ Tech Stack
*   **Language:** Kotlin
*   **Database:** Room (SQLite) for local persistence
*   **Background Tasks:** WorkManager API
*   **AI Engine:** Google Gemini API (via Secure Server Proxy)
*   **Architecture:** MVVM (Model-View-ViewModel)
*   **UI/UX:** Material Design 3 with custom high-contrast animal icons

---

## 🚀 How to Run (Android Studio)
1.  **Clone this repo:** `git clone https://github.com/yourusername/grama-vaxi.git`
2.  **Open in Android Studio:** Use version **Hedgehog** or later.
3.  **GEMINI_API_KEY:** Add your API key to `local.properties` or environment variables.
4.  **Gradle Sync:** Wait for the project to sync all dependencies (Room, WorkManager, GenAI SDK).
5.  **Run:** Select an emulator (Min API 26) or connect a physical device and click **Run**.

---

## 📂 Project Structure
```text
/android_source/    → Full Kotlin code for Android Studio
├── AndroidManifest.xml
├── java/
│   ├── data/       → Room Database & Entity
│   ├── ui/         → MainActivity & ViewModel
│   ├── worker/     → WorkManager Alerts
│   └── repository/ → Data Source Logic
└── res/
    └── values-kn/  → Kannada Language Support
```

## 🚀 How to Run in Android Studio
1. **Download the project** as a ZIP file.
2. **Open Android Studio**, create a New Project (Empty Views Activity).
3. **Copy the contents** of `/android_source/java/` to your project's `java` folder.
4. **Copy the contents** of `/android_source/res/` to your project's `res` folder.
5. **Update your build.gradle.kts** with the dependencies listed in `ANDROID_STUDY_GUIDE.md`.
6. **Press Run.**

*   **Livestock Wealth:** Preventing animal loss, which acts as the "Savings Account" for rural families.
*   **Animal Welfare:** Ensuring 100% timely medical care for the rural cattle population.
*   **Health Digitization:** Creating a reliable database of village animal health for local officials.
*   **Rural Empowerment:** Bringing precision technology and AI to the fingertips of small-scale farmers.

---

## 📄 License
Copyright © 2026 Grama-Vaxi Team. Built for the VTU Internship Program.
