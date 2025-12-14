# Release Notes & Strategy 📦

This document outlines the version history and planned release schedule for **Kaduda AI**. We follow [Semantic Versioning](https://semver.org/) (MAJOR.MINOR.PATCH).

---

## ✅ Released

### **v0.1.0: The Concept** (Current)
*   **Release Date**: 2025-12-14
*   **Focus**: Visualization & Architecture Design
*   **Features**:
    *   Designed detailed architectural workflow for SMS-to-LLM bridge.
    *   Created interactive HTML simulation (`kaduda_workflow_preview.html`).
    *   Established Git repository structure with `README.md` and `ROADMAP.md`.
    *   Defined "Kaduda" core value proposition.

---

## 📅 Upcoming Releases

### **v0.2.0: The Foundation**
*   **Focus**: Basic Connectivity
*   **Target Features**:
    *   [ ] Initialize Python Flask server structure.
    *   [ ] Integrate Twilio SDK.
    *   [ ] Implement `/sms` Webhook to receive text messages.
    *   [ ] Implement simple "Echo Bot" (Server replies with the same message).

### **v0.3.0: The Brain**
*   **Focus**: AI Integration
*   **Target Features**:
    *   [ ] Integrate Google Gemini API.
    *   [ ] Implement Context Memory System (JSON/SQLite).
    *   [ ] Enable "Chat Loop": User Input -> Memory -> Gemini -> Reply.

### **v0.4.0: Optimization**
*   **Focus**: Constraints & Efficiency
*   **Target Features**:
    *   [ ] **Smart Shortener**: Logic to drastically summarize AI replies to <160 chars.
    *   [ ] **Token Management**: Sliding window context to manage API costs.
    *   [ ] **Error Handling**: Graceful fallbacks if AI times out.

### **v0.5.0: The Polyglot**
*   **Focus**: Localization
*   **Target Features**:
    *   [ ] Automatic Language Detection.
    *   [ ] Swahili System Prompts ("Ongea Kiswahili sanifu").
    *   [ ] Localized fallback messages.

### **v1.0.0: Go Live (Beta)**
*   **Focus**: Deployment
*   **Target Features**:
    *   [ ] Deploy mechanism (Docker/Cloud).
    *   [ ] Production Logging.
    *   [ ] Live public phone number availability.

---

## 🛠️ Hotfix Policy
*   Patches (e.g., v0.2.1) will be issued immediately for critical security bugs or crashing errors.
