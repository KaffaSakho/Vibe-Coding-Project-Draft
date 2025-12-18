Implementation & Ethics Memo for InBetween AI: Scheduling Copilot (Phase 3)

**How I Used AI During the Build**

AI served two distinct functions throughout this project. On one hand, it formed the backbone of the product’s conversational scheduling capabilities. On the other hand, it was an invaluable tool during development, helping me build and refine the prototype.
During development, I mainly used Lovable, a code generation tool that converts plain-language instructions into working front-end code. Rather than starting from scratch, I relied on Lovable to set up the interface, tweak layouts, build conversational flows, and quickly test out different behaviors. This allowed me to spend more time making product decisions like how the system should interact and where its boundaries should be instead of getting bogged down in repetitive setup.

On top of using lovable AI chat, many of the outputs required editing, clarification, or outright rejection. I had to step in frequently to limit scope,and ensure the system behaved appropriately given the mental-health-adjacent context. AI was useful for speed and exploration, but human judgment was necessary to decide what was actually acceptable even as a demo.
Overall, this process reinforced that AI works best as a collaborator rather than an authority. The final prototype is the result of repeated back-and-forth between AI-generated suggestions and deliberate human decisions.
Why the AI Feature Is Designed This Way
The AI feature in InBetween AI is intentionally narrow. It exists to help with one specific task: understanding scheduling-related messages and proposing realistic appointment options. I chose this focus very deliberately.
Scheduling is a high-friction, low-glamour problem in mental health practices. It is repetitive, and often the point where potential initial clients disengage. At the same time, it is an area where mistakes are relatively low-risk as long as the system is constrained. This makes it a strong candidate for AI assistance without crossing into clinical territory.
During development, I decided not to expand the AI’s role beyond scheduling. Features such as emotional analysis, diagnosis, or mental health guidance were technically feasible, but they would have blurred the line between administrative support and care delivery and increased risk. They could have made the product more impressive on the surface but those features would have made it less responsible.
The conversational flow reflects this decision. The assistant may ask follow-up questions to clarify time preferences or availability, but it does not attempt to interpret a user’s mental state or respond therapeutically. When sensitive topics appear, the system maintains a neutral, empathetic tone without offering advice.
I also included therapist bios and quotes alongside appointment suggestions. This would support trust without relying on AI inference. In a real mental health setting, trust should come from transparent human information, not from algorithmic assumptions.

**Risks, Trade-offs, and Ethical Choices**

*Privacy and Data Handling*
One of the most important choices I made was to avoid storing user data entirely. The final prototype does not save chat messages, scheduling requests, or personal information. All interactions exist only for the duration of the session and are lost when the page is refreshed.
Scheduling conversations can include sensitive disclosures, especially when users are seeking therapy for the first time. Persisting that data would have introduced privacy and security risks that were unnecessary for a prototype. By keeping the system stateless, I reduced both ethical risk and technical complexity.

*Bias and Representation*
Another consideration was how therapists are presented. The system does not attempt to algorithmically “match” users to therapists based on inferred identity traits. Instead, it shows a diverse set of therapist profiles and explains fit in general, non-deterministic ways. This avoids reinforcing stereotypes or creating opaque matching logic that users cannot understand or challenge.

*Over-Trust in AI*
Conversational interfaces can encourage users to attribute more intelligence or authority to the system than is warranted. To address this, the assistant is framed clearly as a scheduling tool. Its language is professional and empathetic, but restrained. The prototype does not claim to offer mental health support, and the documentation explicitly defines its scope.

*Crisis and Safety Handling*
The system includes explicit guardrails for crisis-related language. If a user mentions self-harm, harm to others, illegal activity, or emergencies, the assistant stops the scheduling flow and directs the user to 911 or appropriate national resources using standardized, widely accepted language. It does not attempt to handle these situations on its own.
This reflects a conscious boundary: acknowledging risk without pretending to resolve it.

*Academic Integrity*
Throughout the project, AI assisted with coding and iteration; however, the product decisions, ethical constraints, and final framing were my own. Whenever AI-generated content was used, it was reviewed and revised to ensure it accurately reflected my intent.

*What I Learned About Building with Generative AI*
The biggest takeaway from this project is that deciding what not to build is just as important as deciding what to build. Generative AI makes expansion tempting, but restraint is essential especially in sensitive domains like mental health.
I also learned that prompts are not just technical inputs; they are design choices. Tone, boundaries, and refusal behavior all emerge from how the system is instructed. Iterating on prompts felt similar to iterating on interaction design.
If I were advising another founder using GenAI, I would emphasize starting small, defining clear limits, and treating ethical constraints as first-class product requirements rather than afterthoughts.
More broadly, this project changed how I think about AI in my future work. Instead of seeing AI as something that replaces human decision-making, I now see it as a way to support well-defined tasks within thoughtfully designed systems. When used carefully, AI can improve real workflows without undermining trust or accountability.

*Conclusion*
InBetween AI demonstrates a constrained and intentional use of generative AI in a mental health context. By limiting the AI’s role to scheduling, avoiding data persistence, and adding explicit safety guardrails, the prototype prioritizes responsibility over technical buzzword. This project reinforced the importance of aligning AI capabilities with real user needs while maintaining clear ethical boundaries.


