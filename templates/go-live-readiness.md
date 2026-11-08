# Go-live checklist

Gates for a voice or chat agent, from lab to full traffic. Each gate has an owner, a number and a
way back. The stages follow the lab, shadow, pilot and rollout sequence described in
[this article](https://genai4business.com/writing/lab-shadow-pilot-rollout).

## Before anything: the paths that cannot fail

- [ ] Emergencies (a gas smell, a threat, a medical risk) reach a human or the right number in one
      turn, whatever the caller says first, and a test proves it
- [ ] Callers who ask for a human get one, and the agent does not argue
- [ ] The agent says it is an AI in its first turn (spoken, for voice) and on whose behalf it acts
      (EU AI Act, Art. 50 transparency obligations, applicable from 2 August 2026)
- [ ] Secrets (PINs, one-time codes, card numbers) go by keypad or link, never into transcripts or
      model context; logs are redacted
- [ ] The agent never treats something a caller knows (a customer code, a birth date) as proof of
      identity beyond what policy allows
- [ ] Writes (payments, address changes, contract changes) need the right level of verification
- [ ] A kill switch exists, someone on call knows where it is, and it has been used once in a test

## Gate 1: Lab

- [ ] Golden dataset of real or realistic conversations, with the rule each one tests
- [ ] Regression suite in CI; a prompt or model change cannot merge if a safety check fails
- [ ] pass^k over repeated trials on the critical paths, not one lucky run
- [ ] Simulated callers for the paths without data yet (angry, confused, elderly, another AI agent)
- [ ] Values captured by voice validated (checksums where they exist, read-back where they do not)
- [ ] Voice tested in audio, not only text: noise, accents, barge-in, keypad tones, p95 response latency
- [ ] Thresholds set per category (intent, entity type, safety tag), not one average

## Gate 2: Shadow

- [ ] The agent runs on live traffic without answering; its decisions are compared with the human's
- [ ] Disagreements read by a person, sorted into: agent wrong, human wrong, policy unclear
- [ ] Silent wrong actions counted separately from refusals and handoffs

## Gate 3: Pilot

- [ ] A small, reversible share of traffic, chosen so results can be compared with a control
- [ ] Repeat contacts within 7 days tracked, not just containment
- [ ] Handoffs pass a summary, identity status and a reason code; the caller is not asked again
- [ ] Daily transcript review with operations; a named owner for each failure category
- [ ] Rollback tested, with a threshold agreed in advance

## Gate 4: Rollout

- [ ] Traffic raised in steps, never straight to 100%, with the same thresholds at each step
- [ ] Monitoring on outcomes (resolution, repeat contacts, complaints), not only on latency and errors
- [ ] A regression test added for every production incident before it is closed
- [ ] Cost per outcome reviewed against the business case, under the actual pricing model

## Sign-off

| Gate | Owner | Number that passed | Date | Way back |
|---|---|---|---|---|
