# Project Requirement Document: Grama-Vaxi

## 1. Project Overview
**Project Name:** Grama-Vaxi (Livestock Digital Health Card)
**Domain:** Rural Healthcare / Agritech
**Platform:** Android (Kotlin)
**Objective:** To reduce livestock mortality rates in rural villages by providing a digital tracking system for vaccinations and health alerts.

---

## 2. Problem Statement
In rural India, livestock is often the primary source of wealth (the "Savings Account") for farmers. However, many animals die from preventable outbreaks (such as Foot-and-mouth disease or Blue Tongue) because:
1.  Farmers miss vaccination camp announcements (which are usually via loudspeakers).
2.  Lack of organized health records for individual animals.
3.  Delayed reporting of diseases in remote locations.

---

## 3. The Vision (Solution)
Grama-Vaxi transforms livestock management from reactive to proactive. It acts as a "Digital Health Card," documenting every animal’s profile and predicting vaccination requirements. The app uses automated background services to alert farmers days before government medical camps reach their specific village square.

---

## 4. Functional Requirements

### 4.1 Animal Ledger (Registration)
*   **Visual Recording:** Register animals with a profile photo, breed, age, and type (Sheep/Goat/Cattle).
*   **Unique Identity:** Each animal is assigned a digital ID for life-long tracking.

### 4.2 Automated Vaccine Calendar
*   **Cycle Prediction:** Based on the type and age, the app calculates "Next Shot" dates.
*   **History Tracking:** Log previous vaccination dates for medical compliance.

### 4.3 Camp & Disease Alerts
*   **Geo-Alerts:** Notify farmers: "Doctor arriving at Temple Square tomorrow at 9:00 AM."
*   **Advanced Warnings:** Push notifications triggered 3 days, 1 day, and 1 hour before scheduled camps.

### 4.4 AI-Powered Disease Reporting (Simulated)
*   **Symptom Check:** Farmers can submit symptoms (via text or voice).
*   **GenAI Integration:** The app provides immediate first-aid advice and connects the farmer to the nearest veterinarian.

---

## 5. Technical Specifications
*   **Language:** Kotlin (Modern, Type-safe).
*   **Database:** Room Persistence Library (Offline-first architecture).
*   **Background Services:** WorkManager API (Reliable scheduling of alerts even if the app is killed).
*   **UI/UX:** Material Design 3, focus on large "Animal Icons" and visual affordance for low-literacy users.
*   **Intelligence:** Google Gemini API for symptom analysis and localized advice.

---

## 6. Globalization & Accessibility
*   **Vernacular Support:** Comprehensive UI support for **Kannada** to ensure usability by local farmers.
*   **Visual-Heavy Interface:** Minimized text usage in favor of icons and photos.

---

## 7. Impact & Success Criteria
*   **Livestock Wealth:** Measurable reduction in preventable animal loss.
*   **Digitization:** Creation of a central, searchable database for village health officials.
*   **Success Metric:** Alerts must trigger reliably in background mode, and the "Register" process must be completed in under 60 seconds by a first-time user.
