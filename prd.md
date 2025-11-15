# InBetween AI – Scheduling Copilot  
## Product Requirements Document (Phase 2 – Updated)

# 1. Overview & Goal

**InBetween AI** is an AI-powered scheduling copilot for mental health private practices.  
The goal of the Phase 2 prototype is to demonstrate how AI can:

- Interpret a natural-language client message  
- Infer scheduling needs  
- Suggest three appointment times  
- Allow users to simulate booking a slot  

This prototype was built **entirely in Lovable**, a vibe coding tool that converts natural-language instructions into working code.

# 2. Core Features (Implemented)

### 2.1 Feature 1 — AI Scheduling Interpreter (Main AI Feature)

Users enter a message such as:

> “Hi, I’m looking for a virtual therapy session after 5pm next week.”

The AI:

- Reads the message  
- Infers:
  - Client type  
  - Day preferences  
  - Time preferences  
  - Mode (virtual / in-person)  
- Uses fictional therapist availability  
- Returns:
  - A summary sentence  
  - Three appointment suggestions  

### Sample fictional availability:

- **Dr. Rivera** — virtual — Tue/Wed 5–7pm  
- **Dr. Lee** — virtual or in-person — Thu 3–6pm  
- **Dr. Chen** — in-person — Mon/Fri 9am–12pm  

### 2.2 Feature 2 — Slot Selection + Simulated Calendar Invite

Users can:

1. Click on a suggested appointment slot  
2. Type their email  
3. Click **Receive Calendar Invite**

This displays a confirmation message (simulation only).

This satisfies the requirement for a **second interactive feature**.

# 3. AI Specification

### Model  
The prototype uses a **Gemini-style API request structure** (placeholder endpoint and key) in `script.js`.  
The code includes a `fetch()` call that can easily be connected to a real Gemini endpoint.

### Task Breakdown

AI performs:

- Natural language understanding  
- Intention parsing  
- Availability matching  
- Suggesting three appointment slots  

### Input
Free-text client message.

### Output
JSON object:
```json
{
  "summary": "...",
  "options": [
    { "day": "...", "time_range": "...", "mode": "...", "therapist_name": "..." }
  ]
}
