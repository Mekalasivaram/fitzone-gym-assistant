# FitZone Gym Sales Agent Prototype

A small browser prototype demonstrating a gym sales conversation from first question through a saved tour request and staff summary.

## Run it

1. Open `index.html` in Chrome or another modern browser. The text demo works locally without setup or an API key.
2. Ask about a membership, classes, equipment, opening hours, or a tour. The assistant searches the sample FAQ using simple keyword matching.
3. Enter a visitor name, fitness goal, preferred location, membership interest, and future tour date/time.
4. Click **Save visitor & tour**. The request is stored in this browser on this device; staff still need to confirm the appointment.
5. Click **Download calendar invite** to create an `.ics` request to import into a calendar, or **Export lead list (CSV)** to download the locally saved records.
6. Try **Speak** or **Read replies aloud** if the browser supports speech features and grants permission. Text is the reliable demo path.

## Files

- `index.html` — runnable prototype.
- `gym-faq.md` — sample knowledge base.
- `report.md` — one-page project report.
- `architecture.svg` — current and proposed system architecture.
- `criteria-map.md` — honest mapping from the challenge requirements to this prototype.

## What is implemented

- Typed chat and optional browser speech input/output.
- Keyword-based FAQ lookup with follow-up prompts.
- Session conversation history.
- Basic lead score based on four collected fields and keyword sentiment label.
- Summary and tour request saved in browser local storage.
- Calendar invite (`.ics`) and lead list (`.csv`) exports.

## Limitations (explain these honestly)

This is a rules-based prototype, not a live generative AI service. FAQ matching is not full RAG; sentiment and lead score use simple rules; Hindi speech input is recognized but replies are English. The `.ics` file is a tour request the user imports; it is not a confirmed booking. CSV export is not a live CRM integration. There is no phone network, server, or secure database. Do not enter real customer data.

## Next production steps

Add a grounded RAG pipeline and LLM, multilingual responses, secure server-side storage, real calendar and CRM connectors, robust telephony, monitoring, consent handling, staff escalation, and load testing. See `report.md` for scale and cost considerations.
