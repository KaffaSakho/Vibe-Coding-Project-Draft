# **InBetween AI — Scheduling Copilot**

**Product Requirements Document (Phase 3 – Final)**

---

## **1. Product Overview (Updated)**

InBetween AI is an **AI-powered scheduling copilot** designed for **mental health private practices** to reduce friction during the earliest stage of client onboarding. New clients often disengage before their first session due to slow responses, confusing availability, or difficulty identifying a therapist who feels like a good fit.

The current prototype demonstrates how **conversational AI** can merge therapist discovery and scheduling into a single, guided interaction. Users describe their needs in natural language, the system asks brief clarifying questions when necessary, and then proposes a small set of realistic appointment options paired with therapist context to build trust. The prototype is intentionally scoped to **scheduling only**, using fictional data and session-based interactions to minimize ethical and privacy risks.

---

## **2. Core Features & Status**

### **Feature 1 — Conversational AI Scheduling Assistant**

**Status:** Implemented
**AI-dependent:** Yes

* Users enter free-text messages describing their scheduling needs (e.g., context of the help, preferred times, modality, flexibility).
* The assistant interprets the message conversationally.
* The system may ask short follow-up questions to gain context before proposing times.
* Outputs **2–3 appointment options** displayed directly within the chat flow.

Each suggested slot includes:

* Full date and time (e.g., *Monday, November 29th, 9:00–9:45 AM*),
* Modality (virtual or in-person),
* Therapist name.

---

### **Feature 2 — Therapist Trust & Fit Preview**

**Status:** Implemented
**AI-dependent:** No (content-driven, surfaced alongside AI output)

* Each proposed appointment includes a **“Read about Dr. [Name]”** button.
* Clicking the button reveals:

  * A short therapist bio,
  * A real photo (demo content),
  * A brief explanation of why the therapist may be a good fit,
  * A quote from the therapist.
* Therapists are intentionally diverse across ethnicity, background, and practice style.

Since there is no initial human interaction, this feature is designed to build **emotional trust** during the scheduling process, particularly for first-time clients.

---

### **Feature 3 — Scheduling Refinement Flow**

**Status:** Implemented
**AI-dependent:** Yes

* Users can indicate that suggested time slots do not work.
* The assistant generates new options.
* After 3 unsuccessful attempts, the assistant asks the user for additional preferences before proposing times again.
* Updated time slots replace previous suggestions and appear **below the chat input**, maintaining conversational continuity.

---

### **Feature 4 — Safety & Ethical Guardrails**

**Status:** Implemented
**AI-dependent:** Yes (rule- and prompt-based)

* If a user mentions:

  * Self-harm,
  * Harm to others,
  * Illegal activity,
  * Emergency situations,

  the assistant does **not** proceed with scheduling and instead directs the user to **911 or appropriate national crisis resources**, using language similar to Google’s safety responses.
* If user input is off-topic, the assistant responds politely and clarifies the purpose of the tool.
* The assistant consistently uses a **professional and empathetic tone** and avoids clinical interpretation.

---

## **3. AI Specification (Final)**

### **AI Tasks Performed**

* **Natural Language Understanding:** Interprets user intent and scheduling-related context.
* **Contextual Conversation Handling:** Maintains conversational flow and asks clarifying questions.
* **Recommendation Generation:** Proposes a limited set of appointment options based on fictional availability.
* **Text Generation:** Produces empathetic, professional responses.

### **What the AI Does Not Do**

* Provide therapy, diagnosis, or mental health advice.
* Make autonomous decisions without constraints.
* Store or recall user conversations across sessions.

### **Inputs**

* Free-text user messages entered via the chat interface either through typing or a voice prompt.

### **Outputs**

* Conversational responses.
* 2–3 appointment suggestions with:

  * Date,
  * Time range,
  * Modality,
  * Therapist name.
* Optional therapist bio display triggered by user action.

### **Model / Tooling**

* The prototype uses a **Gemini-style API request structure** (implemented as a placeholder in `script.js`).
* The design supports direct integration with Google AI Studio / Gemini APIs but operates with fictional data for demonstration.

---

## **4. Technical Architecture (Reality Check)**

* **Frontend:** HTML, CSS, JavaScript.
* **AI Interaction:** Client-side JavaScript constructs prompts and simulates responses from a Gemini-compatible endpoint.
* **State Management:** In-session browser state only.
* **Database:** None.
* **Hosting:** Static site.

No user data, chat history, or personal information is persisted.

---

## **5. Prompting & Iteration Summary**

Prompting evolved iteratively to:

* Shift from keyword-based interpretation to conversational understanding.
* Add clarifying questions before proposing time slots.
* Introduce safety language for crisis-related inputs.
* Enforce empathetic tone and professional boundaries.
* Support dynamic regeneration of appointment options.

This iterative prompt refinement directly shaped the UX and demonstrated how prompt design functions as product design.

---

## **6. UX & Limitations**

### **Intended User Journey**

1. User describes scheduling needs in natural language.
2. Assistant interprets and asks clarifying questions if needed.
3. Assistant proposes appointment options with therapist context.
4. User reviews options, requests alternatives, or explores therapist bios.

### **Known Limitations**

* Appointment availability is fictional.
* Time interpretation may be imperfect for ambiguous phrasing.
* No real calendar integration or persistence.
* The system is not suitable for urgent or crisis situations.

### **Ethical & Trust Constraints**

* Session-only interactions.
* No storage of user input.
* Explicit crisis redirection.
* Clear non-clinical positioning.

---

## **7. Future Roadmap**

If developed further, next steps would include:

* Real calendar and EHR integration.
* Admin approval workflows.
* Evaluation of scheduling success rates.
* More robust accessibility features.
* Formal HIPAA-compliant backend architecture.

---

### **Summary**

The Phase 3 prototype of InBetween AI demonstrates a **narrow, intentional, and responsible use of generative AI** to improve scheduling experiences in mental health private practices while maintaining strong ethical boundaries and minimizing risk.

