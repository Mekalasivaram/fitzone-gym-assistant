# FitZone Gym Membership Assistant — Project Report

**Problem.** Gym staff spend time answering repeated questions and collecting visitor details. A prospective member may need help choosing a location, understanding membership options, or arranging a first visit.

**Solution.** FitZone Gym Assistant is a small web prototype that guides a visitor through a conversation, collects their fitness goal, preferred location, membership interest, and preferred tour time, and displays a lead status and summary for staff.

**Working demonstration.** Open `index.html` in a browser. The visitor types messages; scripted replies ask follow-up questions. The form displays visitor details, a basic status, a saved tour time, and a summary. Optional speech input and spoken replies rely on browser support. The prototype is not connected to a live gym, calendar, CRM, or AI service.

**Architecture.** The browser page contains the conversation interface and lead form. Small JavaScript rules choose follow-up prompts and assemble the summary. Fictional FAQ content is documented in `gym-faq.md`. In a production design, an application server would retrieve approved FAQ passages and send them with the visitor's question to an AI model. A secure database would store leads; calendar and CRM services could handle tours and staff follow-up. Speech-to-text and text-to-speech services could support phone or voice conversations.

**Security and privacy.** This demo processes sample visitor details in the browser and sends them nowhere. A production version should collect only needed data, use encrypted connections and storage, restrict staff access, define retention periods, and keep credentials in a secret manager rather than source code. Visitors should be told how their information will be used.

**Scaling and cost.** To support up to 100,000 users, deploy stateless application instances behind a load balancer, use a managed database with backups, and use a queue for slower AI, speech, and CRM tasks. Add rate limits, monitoring, and autoscaling. Actual costs depend on concurrent sessions, call duration, model and speech usage, database size, and hosting region; measure a pilot before estimating a budget.

**Limitations and next steps.** The current prototype uses scripted prompts, has no persistent database, and does not book a real calendar appointment. Next, add FAQ retrieval with clear “I don’t know” behavior, test responses, connect secure lead storage and a calendar, then add multilingual voice and CRM integration.
