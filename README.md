# HVAC Lead Triage (GHL-ready)

AI triage for inbound HVAC leads. Paste a lead message and get back intent, urgency (1-5), a hot/warm/cold score, and a drafted SMS reply, all as structured JSON.

Companion to [ghl-hvac-construction-funnel](https://github.com/maetorresphils/ghl-hvac-construction-funnel):
**Meta Ads → Funnel → AI triage → CRM → Booking**

## The problem
HVAC leads go cold fast. A "no AC, 98°F, baby at home" message and a "just want a quote for next spring" message look identical in an inbox, and slow replies lose the job. This tool sorts them in seconds so the right lead gets a human first.

## What it returns
Target output schema:

```json
{
  "intent": "emergency_repair",
  "urgency": 5,
  "score": "hot",
  "reply": "We're sorry about the heat. A technician can call you within 15 minutes. What's the best number?"
}
```

## Status
🚧 **v1 in progress**: Python + LangChain structured output + Streamlit demo.

## Roadmap
- [x] Repo created
- [ ] v1: lead scoring (`qualifier.py`) + Streamlit demo
- [ ] Demo video (60 seconds)
- [ ] v1.5: send scored leads to a GoHighLevel webhook (contact tag + SMS trigger)
- [ ] v2: LangChain tool use (calendar availability check)

## Tech
Python · LangChain · Claude API · Streamlit · Pydantic

## Author
Mae Christine Torres | [Pixels by M](https://www.pixelsbymae.com/)
