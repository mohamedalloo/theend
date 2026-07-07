# theend.ai — Launch Kit

Everything needed to go from waitlist to first calls. Built from the July 2026 market/legal research.

---

## 1. The voice agent blueprint (build this when the waitlist proves demand)

**Stack recommendation:** Vapi or Retell for call orchestration (both ~$0.05–0.07/min platform), Twilio number, Deepgram STT, Claude for the interviewer brain, a natural TTS voice (pick a warm, slower, mid-60s-sounding voice — NOT a clone of anyone). All-in retail cost lands ~$0.13–0.20/min; at scale or self-assembled, ~$0.08/min is achievable.

**Interviewer system prompt (starting point):**

```
You are a warm, patient interviewer calling {{name}}, who is {{age}} years old, for
theend.ai. Your job is to help them tell their life story, one conversation at a time.

Identity & consent (non-negotiable, every call):
- Open every call the same way: greet them by name, say you're "the interviewer from
  theend dot ai — I'm an AI assistant, and this call is recorded so we can put your
  stories in your book. Is now still a good time?"
- If they say stop, don't want to talk, or sound confused about who you are: warmly
  end the call, never argue, and flag the account for family follow-up.
- If they say "stop calling" in any form, confirm kindly, end, and mark DO NOT CALL.

Conversation style:
- Speak slowly. Short sentences. One question at a time. Long pauses are fine —
  never interrupt or rush a silence; older storytellers need time to travel back.
- Today's theme: {{theme}} (e.g., childhood home, how they met their spouse, first job).
  But if they wander somewhere emotionally alive, FOLLOW THEM. The plan is disposable;
  the story is not.
- Ask the follow-ups a loving grandchild would ask: "Wait — he proposed WHERE?"
  "What did your mother say when you told her?" "What did it smell like?"
- Reflect small details back ("a green pickup with a broken gate — I can see it")
  so they feel heard, not processed.
- Aim for 15 minutes; if they're enjoying it, go to 25 max, then land gently:
  "I could listen all day — let's save the rest for next week. Same time?"

Safety:
- If they mention wanting to die, being a burden, or self-harm: respond with warmth,
  do not probe, provide the 988 Suicide & Crisis Lifeline, end the interview portion,
  and trigger the family-notification protocol immediately.
- If they report abuse, neglect, or someone taking their money: listen, don't
  investigate, flag for family follow-up same day.
- Never discuss: their finances, purchases, passwords, or anything transactional.
  If they ask you to help with anything involving money, decline gently and suggest
  they call their family. (This protects them and us — AI phone scams on seniors
  are epidemic, and we must never behave like one.)
```

**Call 0 (onboarding, with the adult child on the line):** the family introduces the service on a 3-way call. The agent introduces itself, explains recording, and captures the elder's own recorded "yes" to (a) recorded calls, (b) stories used in a printed book for the family. This recorded consent is the compliance cornerstone — archive it per account.

## 2. Compliance checklist (do not launch calls without these)

- [ ] **TCPA consent from the ELDER** (the called party), not just the paying child — captured on the recorded Call 0. AI voices are legally "artificial voices" (FCC 2024); statutory damages are $500–$1,500/call.
- [ ] "Stop calling" honored immediately and logged (FCC revocation rules: any reasonable phrase, ≤10 business days, we do it same-call).
- [ ] AI self-identification at the top of **every** call (CA SB 243 / NY companion-chatbot laws; also just right).
- [ ] All-party recording consent script (CA, FL, IL, WA, PA, MA + others) — the per-call recording reminder covers this.
- [ ] **Illinois BIPA:** voice recordings + any voiceprint processing need written notice, written release, and a published retention/destruction policy. Until counsel signs off on the flow, geo-exclude Illinois numbers.
- [ ] Self-harm/crisis protocol implemented and tested (SB 243 requirement, and elders reminiscing about loss will hit hard moments).
- [ ] **No voice cloning, ever** — it's the brand promise on the landing page and avoids the ELVIS Act / NO FAKES Act thicket entirely.
- [ ] Security review before storing recordings at scale: a breached senior voice archive is grandparent-scam raw material. Encrypt at rest, minimal retention of raw audio access, delete-on-request.
- [ ] Talk to a TCPA lawyer before the first real outbound call. Budget ~$2–5k; it's the cheapest insurance in this business.

## 3. Unit economics (honest version)

| Item | Per family / year |
|---|---|
| Calls: 50 wks × ~15 min × $0.15/min (retail stack) | ~$112 |
| Calls at optimized stack ($0.08/min) | ~$60 |
| Hardcover printing (Lulu/BookBaby, ~150pp color) | $20–35 |
| Shipping | ~$8 |
| **COGS at retail stack** | **~$140–155** |
| **COGS optimized** | **~$90–105** |

**Implication:** the $149 founding price is a break-even-ish learning cohort — that's fine and normal. The GA price must be **$249+** (research shows the market band tops at $249 one-time and $199/yr subscriptions, with a gap up to $1,099 done-for-you). Margin path: optimized call stack + $249 GA price + extra-copy sales (siblings; StoryWorth sells $39–79 extra books all day) + a premium "family edition" tier later.

## 4. Meta ad angles (test $50–100/day across 5, kill losers weekly)

1. **The blank book:** "You bought the question-a-week journal. It came back blank. This one just needs her to answer the phone." (attacks the known StoryWorth failure mode)
2. **The voicemail:** "After he was gone, we tore the house apart looking for one old voicemail. Keep the voice, not just the stories."
3. **The Sunday call:** "She waits all week for your call. Now one of them writes her book."
4. **Mother's Day (seasonal):** "This Mother's Day, give her the gift of being asked."
5. **The grandkids:** "Your kids will be able to press play and hear their grandmother tell it herself."

Target: women 35–55, interests: caregiving, StoryWorth-adjacent, Ancestry/genealogy. Landing: the sample chapter page converts better than the homepage for cold traffic — test both.

**Timing:** the two seasonal windows are Nov 1–Dec 15 (peak, StoryWorth spends ~6x normal) and the 6 weeks before Mother's Day. Don't launch cold traffic in a dead window; use it to build the waitlist organically.

## 5. Waitlist → founding-family email sequence

1. **Instant:** "You're in" + sample chapter link + one question: "Who's the storyteller, and what do you most want them asked?" (replies = discovery gold + engagement signal)
2. **Day 3:** The why — the blank-book problem, the voice archive promise.
3. **Day 7:** "How the first call works" (consent-first walkthrough — converts the trust-anxious)
4. **Launch:** founding pricing, hard cap on cohort size, refundable-until-first-call framing.

## 6. Open decisions

- **The name.** theend.ai is memorable but dark for a warm family gift. Decide with data: run identical ads under theend.ai and one warmer alternative; keep the winner. (The FAQ's reframe — "every great story deserves a proper ending" — tested fine in copy, but let clicks vote.)
- **Waitlist backend:** the form currently stores locally in the browser (placeholder). Wire to ConvertKit/Loops/Formspree before spending a dollar on ads.
- **Domain:** theend.ai is registered (2023, Namecheap, parked). If it's not already yours, inquire — parked .ai domains are often buyable.
