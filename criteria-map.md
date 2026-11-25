# Challenge requirements: prototype coverage

Use this page to describe the project accurately during the discussion.

| Requirement | What this prototype does | Honest status |
|---|---|---|
| Real-time voice with STT/TTS | Optional browser speech recognition and speech synthesis | Basic browser feature; not telephone or streaming voice infrastructure |
| Contextual memory | Keeps the conversation transcript during the current browser session and uses collected lead fields | Basic session context; no long-term conversational memory |
| Multilingual communication | Hindi can be selected for speech recognition | Partial: agent responses are English |
| Lead qualification | Counts four collected fields; shows qualified once at least three are present | Simple heuristic, not learned/AI scoring |
| Sentiment analysis | Looks for a small set of positive/concerned phrases | Simple keyword heuristic |
| RAG knowledge retrieval | Searches a small FAQ using matching keywords and returns a prepared answer | FAQ retrieval demo; not vector RAG or LLM generation |
| Appointment booking | Saves a requested tour time and downloads an `.ics` file | User-imported request; no availability check or confirmed booking |
| CRM integration | Exports saved leads to CSV | Manual file export; no live CRM connection |
| Call summary / business insights | Displays a lead summary, score, sentiment, and status | Basic single-lead summary; no analytics dashboard |
| Source code | `index.html` and supporting files are included | Available for review |
| Architecture diagram | `architecture.svg` distinguishes current and proposed components | Included |
| End-to-end workflow | Question → FAQ answer → lead details → score/sentiment → tour request → summary/export | Demonstrable in the browser |
| Scale, security, deployment, costs, commercial feasibility | Discussed in `report.md` | Design proposal only; no production deployment, pilot results, or measured cost |
| Live coding / debugging | Candidate should practice changing a FAQ answer, adjusting qualification rules, and explaining the change | Interview preparation; not a built app feature |

## Short explanation

“I built a browser MVP for a fictional gym. It demonstrates the full lead-to-tour-request flow with optional browser speech, FAQ lookup, basic lead and sentiment rules, a summary, and calendar/CSV exports. It does not yet use an LLM or full RAG, and exports do not replace live calendar or CRM integrations. I included a scale and security plan for those production extensions.”
