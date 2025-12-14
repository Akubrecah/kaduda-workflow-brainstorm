# Kaduda AI: Implementation Roadmap 🛤️

This document tracks the step-by-step implementation plan for the Kaduda AI system.

## 📦 Phase 1: Foundation (Backend Setup)
- [ ] **Setup Python Environment**
    - [ ] Initialize `backend/` directory.
    - [ ] Create `requirements.txt` (Flask, Twilio, Google-GenerativeAI).
    - [ ] Create basic `app.py` server structure.
- [ ] **Twilio Integration**
    - [ ] Implement webhook endpoint `/sms`.
    - [ ] Verify incoming requests from Twilio.
    - [ ] Implement basic echo response.

## 🧠 Phase 2: AI Logic & Memory
- [ ] **Gemini Integration**
    - [ ] Configure Google Gemini API Key.
    - [ ] Create helper function to send prompts to Gemini.
- [ ] **Context Management**
    - [ ] Design simple file-based or SQLite JSON memory store (`memory.json`).
    - [ ] Implement `load_history(phone_number)` and `save_history(phone_number, message)`.
- [ ] **Token Counting**
    - [ ] Implement simple word/token counter to ensure context window acts efficiently.
    - [ ] Implement sliding window logic (keep only last N turns).

## 🌍 Phase 3: Advanced Features
- [ ] **Response Shortener**
    - [ ] Add logic to strictly enforce <160 character limit.
    - [ ] Prompt Gemini to "reply in under 30 words".
- [ ] **Multi-language Support**
    - [ ] Detect language (Swahili/English) from input.
    - [ ] Instruct Gemini to rely in the same language.

## 🚀 Phase 4: Production Readiness
- [ ] **Environment Variables**: Move secrets to `.env`.
- [ ] **Logging**: Add proper request/error logging.
- [ ] **Deployment**: Prepare `Procfile` or Dockerfile.

---

## 🛠️ Version Control Strategy

We follow a **Feature Branch** workflow for perfect version control.

1.  **`main`**: The stable code.
2.  **`feature/backend-setup`**: For Phase 1.
3.  **`feature/ai-integration`**: For Phase 2.
4.  **`feature/multi-lang`**: For Phase 3.

**To start working on a feature:**
```bash
git checkout -b feature/backend-setup
# ... make changes ...
git add .
git commit -m "Setup Flask backend"
git push origin feature/backend-setup
# Then create a Pull Request to merge into main
```
