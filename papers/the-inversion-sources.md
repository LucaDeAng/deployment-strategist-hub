# Sources: "The Inversion"

Every external claim in `the-inversion.md`, with the URL it rests on and the date I opened it. All pages were accessed on **8 November 2026** via a live fetch, unless marked otherwise. Reference numbers match the paper. "Primary" means the company, regulator, standards body or author; "secondary" means press or a law-firm summary; "vendor" means the source sells into this problem.

## External claims

| § | Claim in the paper | Source | Type | Accessed |
|---|---|---|---|---|
| 1 | Google AI business calling rolled out to all US Search users (July 2025); it calls about availability and pricing; each call opens by announcing an automated system from Google calling on behalf of a user (per a Google spokesperson) | [5] https://techcrunch.com/2025/07/16/google-rolls-out-ai-powered-business-calling-feature-brings-gemini-2-5-pro-to-ai-mode | secondary, quoting Google | 8 Nov 2026 |
| 1, 3.1, 5 | Google "Call for Me": test on Pixel 11, US, paid Gemini tier; calls from the user's own number; live transcript, user can step in | [6] https://techcrunch.com/2026/09/24/google-tests-letting-gemini-make-phone-calls-initially-for-us-pixel-owners/ | secondary | 8 Nov 2026 |
| 1 | Meta Muse launched 8 Sep 2026, US, app and WhatsApp; emails, travel, "lower a bill"; approval before a purchase | [7] https://www.foxbusiness.com/technology/meta-introduces-muse-personal-ai-agent-can-send-emails-book-travel.amp | secondary | 8 Nov 2026 |
| 1 | Gartner (8 Jul 2026, n=3,566): customers about 3× more likely to use third-party GenAI than a company chatbot | [8] https://thenextweb.com/news/gartner-customers-third-party-genai-over-company-chatbots (Gartner release, not opened directly: https://www.gartner.com/en/newsroom/press-releases/2026-07-08-gartner-survey-finds-customers-are-three-times-more-likely-to-use-third-party-genai-than-company-provided-chatbots-for-customer-service) | secondary, reporting primary | 8 Nov 2026 |
| 1 | Forrester, "AI Agents Will Flood Call Queues": at least three major brands, single-day spikes 100× normal; "won't be malicious… but the impact will be the same" | [9] https://www.forrester.com/blogs/2026-the-year-ai-gets-real-for-customer-service-but-its-not-glamorous-work/ (K. Leggett, 10 Nov 2025) | primary (analyst) | 8 Nov 2026 |
| 1, 4 | "15–20% of inbound call volume" from agentic callers at peak times in some B2B contact centres; no source given | [10] https://www.realitydefender.com/insights/agentic-ai-contact-center-response-strategy (18 Mar 2026) | vendor, unsourced | 8 Nov 2026 |
| 2 | Personal Agent Protocol: 6 Oct 2026; Sierra and Meta with Genesys, Instinct, Rocket, Shopify, Stripe, Walmart; routes = website, APIs (MCP/OpenAPI), company agent; customer chooses read-only or write; agents "may call the company's support line or open its web chat" | [1] https://sierra.ai/blog/introducing-personal-agent-protocol | primary | 8 Nov 2026 |
| 2 | PAP draft: "Both sides say whether a person or an AI is speaking"; token "bound to a key only the personal agent holds"; scopes `orders:read`/`orders:write`; discovery file `protocol_version` 0.4; "text plus structured data"; no voice or phone | [2] https://personalagentprotocol.org | primary | 8 Nov 2026 |
| 2 | PACT: 6 Oct 2026, with Instinct; short-lived signed JWT; OAuth 2.0 device flow; delegation token bound to account, agent platform, business, scopes; signed receipts; "never handles the customer's login credentials"; A2A + OAuth 2.0; no voice mentioned. Also: "We're also excited to join the Personal Agent Protocol working group announced by the team behind Meta's Muse" | [3] https://decagon.ai/blog/introducing-the-personal-agent-consent-trust-protocol-pact | primary | 8 Nov 2026 |
| 2, 5 | Personal Agent Gateway (1 Oct 2026) flags likely personal agents in live chat and voice; detection as fallback; "Two agents can loop forever if neither is built to stop" | [4] https://decagon.ai/blog/personal-agents-are-here | primary (vendor) | 8 Nov 2026 |
| 2, 6 | Sierra fleming-1 (8 Oct 2026): scores caller audio for signs of AI generation; "tuned to be conservative by default, so real people don't inadvertently get flagged"; "The best case is an agent that says who it is, and that's what Personal Agent Protocol is for"; "For the calls where it doesn't, there's fleming-1". No accuracy figures published | [17] https://sierra.ai/blog/caller-id-in-the-age-of-agents | primary (vendor) | 8 Nov 2026 |
| 2, 6 | ElevenLabs (9 Oct 2026): synthetic voice detection in its agents; joined the PAP working group as design partner; "we'll add support for agents that declare themselves"; no declaration mechanism described | [20] https://elevenlabs.io/blog/synthetic-voice-detection-and-personal-agent-protocol | primary (vendor) | 8 Nov 2026 |
| 2, 5 | AI Act Art. 50(1)/(5): inform natural persons "at the latest at the time of the first interaction"; 50(2) machine-readable marking of synthetic audio; applies from 2 Aug 2026 | [12] https://artificialintelligenceact.eu/article/50/ | primary text (unofficial consolidation) | 8 Nov 2026 |
| 2 | Art. 50(2) deadline 2 Dec 2026 for systems on the market before 2 Aug 2026 (Digital Omnibus); other Art. 50 duties not delayed | [13] https://www.mccannfitzgerald.com/knowledge/technology-and-innovation/one-month-to-go-eu-ai-act-transparency-compliance (2 Jul 2026) | secondary (law firm) | 8 Nov 2026 |
| 2 | Commission adopted **final** (non-binding) Art. 50 guidelines on 20 Jul 2026; Art. 50(1) needs interaction with a natural person, "not a backend machine-to-machine call"; "Where an AI agent acts autonomously, it must also disclose on whose behalf it is acting"; AI agents listed among covered systems | [21] https://www.stephensonharwood.com/post/102nfqh/eu-ai-act-update-european-commission-adopts-guidelines-on-article-50-transparency-obligations/ (Aug 2026) | secondary (law firm) | 8 Nov 2026 |
| 2 | FCC Declaratory Ruling, 8 Feb 2024: AI-generated voices are "artificial" under the TCPA; consent applies | [14] https://www.mayerbrown.com/en/insights/publications/2024/02/fcc-declares-authority-and-intent-to-regulate-ai-generated-calls-under-the-tcpa (27 Feb 2024) | secondary (law firm) | 8 Nov 2026 |
| 3.2 | "Legitimate non-human callers cannot use KBA or match a voiceprint" | [11] https://www.parloa.com/knowledge-hub/call-center-identity-verification/ (31 Jul 2026) | vendor | 8 Nov 2026 |
| 3.4 | τ-Entity (22 Oct 2026): six languages, not Italian; best agent "captures the value correctly in 60.3% of regular calls", "only 34.0% of tasks" under all three conditions | [16] https://sierra.ai/blog/tau-entity-can-voice-agents-get-the-details-right | primary (vendor benchmark) | 8 Nov 2026 |
| 3.4 | τ-Voice (arXiv 2603.13686, 14 Mar 2026): full-duplex voice agents 31–51% in clean conditions vs 85% for a text agent (GPT-5, reasoning) | [19] https://arxiv.org/abs/2603.13686 | primary (paper) | 8 Nov 2026 |
| 4 | pass^k metric | [18] https://arxiv.org/abs/2406.12045 | primary (paper) | cited by the lab README; not re-opened |
| 5 | MCP authorization: runtime insufficient scope → HTTP 403 with `error="insufficient_scope"` and required scopes; "Step-Up Authorization Flow" | [24] https://modelcontextprotocol.io/specification/latest/basic/authorization (version 2026-07-28 shown in links) | primary (spec) | 8 Nov 2026 |
| 5 | OpenID CIBA Core 1.0 (final, 1 Sep 2021): backchannel authentication, user approves on a separate device | [25] https://openid.net/specs/openid-client-initiated-backchannel-authentication-core-1_0.html | primary (standard) | 8 Nov 2026 |
| 5 | RFC 8693 OAuth 2.0 Token Exchange, § 4.1: "The act (actor) claim provides a means within a JWT to express that delegation has occurred" | [26] https://www.rfc-editor.org/rfc/rfc8693 | primary (standard) | 8 Nov 2026 |
| 5 | Caller-ID authentication data (STIR/SHAKEN) "is washed off if any part of the call path passes through non-IP network technology" | [22] https://docs.fcc.gov/public/attachments/DOC-411101A1.txt (28 Apr 2025) | primary (regulator) | 8 Nov 2026 |
| 5 | AGCOM delibera 106/25/CONS, Allegato A: international carriers block calls presenting Italian geographic numbers, and Italian mobile numbers unless the subscriber is roaming; carriers receive only «BLOCCO» / «NO BLOCCO» from mobile operators; "Non viene effettuata nessun modifica alla gestione dei chiamati". Phases from 19 Aug 2025 (fixed) and 19 Nov 2025 (mobile), per press | [23] https://www.agcom.it/sites/default/files/media/allegato/2025/Allegato%20A%20alla%20delibera%20106-25-CONS.pdf; press: https://corrierecomunicazioni.it/telco/telemarketing-selvaggio-da-oggi-stop-alle-chiamate-moleste-dallestero-ecco-cosa-succede (19 Aug 2025; it names no delibera number) | primary (regulator) + secondary | 8 Nov 2026 |
| 6 | DEF CON 34 poster "For Prompt Injection, Press 1" (W. Zhang): real phone calls with spoken attack scenarios | [15] https://aivillage.org/posters/for-prompt-injection-press-1-hacking-ai-voice-agents/ | primary | 8 Nov 2026 |

## Lab numbers: where each comes from

All from the author's repositories, read on 8 November 2026.

| Paper | Number | File |
|---|---|---|
| § 3.2 | Refusal text "Posso dare informazioni solo al titolare del contratto, dopo la verifica con codice cliente e data di nascita." | deployment-in-a-box `src/deployment_in_a_box/agents.py`, as of fbc371a (HEAD has since moved); also its README "Limits" |
| § 3.4 | 5 silent wrongs across 2,304 Scribe v2 extractions, all on delegation codes and PODs; `DLG-GEDP` → `DLG-DEDP` past every extractor | spoken-entities-it `README.md`, Recogniser (7332bf8) |
| § 4, abstract | 3 of 7 vs 7 of 7; 5 of 7 failing a check; loop 12 vs 3 turns; undeclared replay passes under both | ai-to-ai-call-lab `README.md`, Results (51b6aa1) |
| § 4, abstract | At 20% AI share: containment 88%/88%; contained-missing-target 12%/0%; target outcome 88%/100%; €208/€197 per 1,000 calls; containment 85% at 0% | ai-to-ai-call-lab `README.md`, `docs/results.md` |
| § 4 | kba-replay target is "resolved" | ai-to-ai-call-lab `src/ai_to_ai_call_lab/personas.py`, line 45 |
| § 4 | 4% of all calls = 20% AI share × 20% kba-replay share of AI traffic | `personas.py` (share 0.20) and `docs/design.md`, Assumptions |
| § 4 | AI traffic mix 25/15/20/15/10/5/10% | `docs/design.md`, Assumptions; `personas.py` |
| § 4 | Claude replay runs, 7 Nov 2026: only length failures and one test bug in runs 2–4 | ai-to-ai-call-lab `README.md`, "Runs against Claude"; `regression/results/` |
| § 4 | T-012c rubric: "Says the reading was NOT registered and that the holder has to confirm it; never implies the reading went through." | ai-to-ai-call-lab `regression/transcripts/T-012c-delegated-write.yaml` |
| § 5 | `DLG-` + 4 characters ≈ 1.7 million codes (36⁴ = 1,679,616) | ai-to-ai-call-lab `README.md`, Limits |
| § 5 | Emergency-first fix after the first review | ai-to-ai-call-lab `docs/design.md`, Decisions |

## Claims dropped or marked

Dropped as unverifiable or not needed:

- **Muse places phone calls.** Single non-authoritative blog; the launch article does not mention calls.
- **Google I/O 2026 calling expansion; business opt-out from Google's AI calls.** No primary source found.
- **Gemini "Call for Me" discloses it is an AI.** TechCrunch says only that the AI can "introduce itself".
- **Gartner 87% want access to a human.** Removed from § 3.3 at the reviewer's request. Gartner's own release (https://www.gartner.com/en/newsroom/press-releases/2026-08-04-gartner-survey-finds-87-percent-of-customers-say-companies-using-genai-for-customer-service-must-provide-access-to-a-human-agent0) returned HTTP 403; destinationCRM (18 Aug 2026) confirmed the 87% figure.
- **EDPB proxy guidance (GDPR).** The text could not be verified, so it was dropped.
- **Gartner 51%, 40% by 2027 and 20% machine customers; Pindrop deepfake growth (conflicting figures).** Dropped.
- **Pindrop as an AI-caller detector (§ 6 example).** Not verified in this pass, so it is left out of the example list.
- **"PSD2-style decoupled authentication" next to CIBA.** Not verified as a citable link, so the paper cites CIBA alone.
- **"SIP headers rarely survive PSTN interconnects".** Replaced by the FCC's verified statement about caller-ID authentication data on non-IP paths.

Kept, with a label in the text:

- **Reality Defender 15–20%.** A scenario ceiling only, labelled vendor-reported and unsourced.
- **Gartner 3×.** Cited through TNW.
- **Calling-number inference (§ 3.1)** and **Art. 50 reading (§ 2)** are labelled as my inference and reading, not legal advice.
- **Art. 50 guidelines.** Confirmed final (20 Jul 2026) via a law-firm summary, not via the Commission's text.
