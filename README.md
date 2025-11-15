# Vibe Coding Project Draft
# InBetween AI – Scheduling Copilot Demo  
*A Product Demo for how InBetween AI would be integrated in private practices platforms*

Overview

**InBetween AI** is an AI-powered scheduling copilot designed to help mental health private practices speed up the onboarding and scheduling process of new clients. This is because one of the main admin pain points in our customer discovery is being able to coordinate the schedule of a client and of the right therapist. Clients often have to go through the process of finding the right therapist at a private practice then find the right schedule slot. This demo shows how AI can be used to merge those two steps into one by using a easy short prompt from the user. It interprets those messages and provide **three realistic appointment options** based on fictional therapist availability.

This prototype was built entirely using the **Lovable AI coding environment**, which generated the initial codebase and supported iterative development.

## Features

### 1️ **AI Scheduling Interpreter (Main AI Feature)**  
The user enters any natural-language message such as:

> “Hi, I’m a new client looking for a virtual session after 5pm next week.”

When the user clicks **Suggest Appointment Times**, the app:

- Sends the message to a Gemini endpoint (**placeholder in repo**)  
- Uses a system prompt to tell the model how to interpret the request  
- Extracts scheduling preferences  
- Produces **three appointment suggestions** using fictional availability  

The output includes:  
- A short summary  
- Three clickable appointment slots  

---

### 2️ **Slot Booking Simulation (Second Interactive Feature)**  
After the AI suggests times, the user can:

1. Click one of the suggested time slots  
2. Type their email  
3. Click **Receive Calendar Invite**  

The app then shows a **simulated confirmation message**.  
(For safety and grading reasons, **no real emails are sent**.)

This completes the second interactive feature required for Option 2.

---

## How It Works

1. User enters a client-style message  
2. User clicks **Suggest Appointment Times**  
3. JavaScript builds a prompt and sends it to a Gemini API endpoint (placeholder)  
4. Gemini returns:
   - A summary  
   - Three appointment suggestions  
5. User selects a slot  
6. User enters an email and simulates receiving a calendar invite  

All availability used is fictional:

- Dr. Rivera — virtual — Tue/Wed 5–7pm  
- Dr. Lee — virtual or in-person — Thu 3–6pm  
- Dr. Chen — in-person — Mon/Fri 9am–12pm  

## Repository Structure

index.html → UI and structure
style.css → styling
script.js → AI logic, slot selection, booking simulation
README.md → documentation
prd.md → updated Product Requirements Document (Phase 2)


## Running the Prototype

1. Clone or download the repository  
2. Open `index.html` in a browser  
3. In `script.js`, replace:
   - `YOUR_GEMINI_API_KEY`
   - `YOUR_GEMINI_ENDPOINT_URL`

The prototype runs entirely client-side.


## Sample Messages

Try messages like:

Hi, I’m looking to start therapy. Any virtual sessions after 5pm next week?

I’m a returning client. Can I book something Wednesday or Thursday evening?

Do you have morning sessions this Friday?


## Ethical Notes

- Not for real clinical use  
- Do not input sensitive or identifying health information  
- All appointment times are fictional  
- No emails or invites are actually sent  


## Vibe Coding Tool: Lovable

This prototype was created entirely using **Lovable**, a vibe coding tool that:

- Generates code from natural-language prompts  
- Allows iterative refinement  
- Handles project structure  
- Supports HTML/CSS/JS generation  

Lovable replaced Google AI Studio for the development workflow.


## Assignment Context

This project satisfies:

**Option 2 — Product Demo / Interactive Prototype**

Requirements met:
- ✔ Two interactive features  
- ✔ One AI-driven feature  
- ✔ Working demo in browser  
- ✔ Updated PRD with prompt history  
- ✔ README explaining AI use  

## Future Enhancements

If developed further, next steps would include:

- Real calendar integration  
- Therapist dashboards  
- User authentication  
- Intake forms  
- HIPAA-compliant backend  
- Expanded scheduling logic  
