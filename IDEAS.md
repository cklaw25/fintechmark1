# FintechMark1: idea shortlist (13 Oct 2026, submit by 20:10)

## Context
- Theme: "Start where money gets stuck." Tracks: payments / access / fraud
- Judging: impact 30 (named person + real money problem), originality 25 (one sentence), execution 25 (one flow end-to-end), trust 20 (what could go wrong + how users stay safe)
- Video 1:30 max: person 0:00 -> why now 0:15 -> demo 0:25 (wow by 1:00) -> trust 1:05 ("Real: X. Mocked: Y.") -> close 1:20 (who pays, why)
- Judges:
  - Daniele Parla (private credit analytics, DWS): prices loans for lenders
  - Till Tornieporth (PE, Verdane; built a company): "a path from tonight to thousands"
  - Anna Zverkova (PM, Experian; huge credit data pool): "data used right, and responsibly"
  - Luka Dadiani (insurtech product, Howden HX; co-host): "a flow so smooth it needs no pitch"
- Side tracks: Best use of Zaro (Zaro team), Best use of Fotor (Nora Chen)
- Zaro = London AI startup, $5.1M (Cherry VC, June 2026). A company-owned context layer where AI answers come from versioned files and every answer cites its source file. Governed, with logged actions. No public API found, so ask the Zaro team what access the tokens give.
- Sponsor: Singapore Global Network (EDB), with LSE Generate

## 1. Receipts: lender-ready loan pack with sources (Access) <- best Zaro fit
Tunde runs a cafe and was refused a £15k loan with no reason given. He uploads 6 months of bank CSV. The app builds the cashflow, a DSCR proxy and the likely reasons for the decline, plus matched products and lenders. **Every number links to the exact transactions behind it.**
Hits: DWS (loan pricing), Experian (responsible data use, consent), Zaro (attributable answers).

## 2. Paid?: fake payment-screenshot checker for small sellers (Fraud) <- best wow + Fotor fit
Priya sells on Vinted and Instagram. A buyer sends a "transfer sent" screenshot, she ships, and the money never arrives. AI image editors make these fakes in seconds. She uploads the screenshot. Vision AI extracts the amount, reference and time, flags signs of editing, and checks it against her real incoming transactions: "Not in your account. Don't ship."
Fotor angle: we used Fotor to make the fake test screenshots, which shows the threat is real.

---

# FRAUD & SECURITY idea list (chosen track)

Why now (works for any of these): AI makes scams cheap and convincing (cloned voices, perfect phishing, fake screenshots in seconds). Since Oct 2024 UK banks must reimburse most APP-scam victims (up to £85k), so banks now pay directly for every scam they fail to stop. That makes the bank a buyer.

Trust story (works for all): we never move or block money ourselves, we only add a pause and an explanation. The AI shows the red flags it found and where it found them (Zaro-style citations). No bank logins, and data is processed then thrown away.

### F1. Pause: "scam check before you pay"
- Person: Margaret, 68, gets a call from "Barclays fraud team" telling her to move £8,000 to a "safe account".
- Flow: she pastes or speaks the message, or answers 3 quick questions (Who asked? Why the urgency? New payee?). The AI matches it against known APP scam scripts (safe account, impersonation, urgency, secrecy) and returns a red/amber/green verdict. Each flag is highlighted in her own words, with one safe next step: "Hang up and call the number on your card."
- Who pays: banks build it into the payment screen, because every scam it stops is a reimbursement they don't pay.
- Build: very easy. One text box and an LLM with a structured verdict. Best "smooth flow" (Howden judge).

### F2. Rent Check: rental deposit scam checker
- Person: Wei, an international student starting at LSE. A "landlord" overseas asks for a £2,000 deposit before any viewing.
- Flow: paste the listing text and landlord messages, plus the photo. It checks the price against the area, script red flags (abroad, can't view, pay by transfer/crypto, rush) and reused photos. Ownership is checked with a mocked Land Registry lookup. Verdict plus a list of what to ask the landlord.
- Why: very relatable for this audience (LSE/Singapore network, students new to the UK).
- Who pays: universities and accommodation sites (SpareRoom, Rightmove) license it, or banks.

### F3. Invoice Guard: changed-bank-details scam for small businesses
- Person: Sam runs a 10-person building firm. A "supplier" emails: "We changed banks, pay the £14k invoice here."
- Flow: upload the invoice or email. It compares against the supplier's past invoices: bank details changed? Lookalike domain (suppl1er.co)? Urgency? It also runs a mocked Confirmation of Payee name check. Verdict: "Bank details changed + domain registered 3 days ago → call supplier on known number."
- Why: business email compromise is one of the costliest frauds for small businesses. It fits Zaro well, because it answers from the company's own invoice history with the source cited.
- Who pays: accounting tools (Xero/QuickBooks add-on) or business banks.

### F4. Paid?: fake payment-screenshot checker (see #2 above)
- Marketplace sellers. Vision AI plus matching against the seller's real incoming payments. Pairs with Fotor (we used Fotor to make the fakes).

### F5. Mule Alert: money-mule recruitment detector for students and young people
- Person: Jay, 19. An Instagram ad says "Earn £500/week, just receive money into your account."
- Flow: paste or screenshot the job ad or DM. The AI flags mule-recruitment patterns and explains the consequence (criminal record, bank account closed, CIFAS fraud marker). Safe next step offered.
- Who pays: banks and universities (prevention), social platforms.

### F6. Is It Really Mum?: voice-clone family emergency check
- Person: Dad gets a call in his daughter's cloned voice: "Lost my phone, need £600 now."
- Flow: a one-tap "verify" sends a challenge to her real number or asks for the family safe word. The AI flags the script (new number, urgency, emergency, money).
- Harder to demo live; more of a concept.

### F7. Second Pair of Eyes: trusted-contact check for vulnerable people
- An unusual large payment (new payee, odd hour, much bigger than usual) pings a chosen family member to confirm, with the AI's summary of why it looks odd.
- Needs mocked bank data; demo works but it's more product than tech.

## Recommendation (Fraud)
- **F1 Pause**: easiest to finish, cleanest flow, clearest buyer (banks + reimbursement rule).
- **F3 Invoice Guard**: most original and the strongest Zaro fit (answers from the company's own records, with sources).
- **F2 Rent Check**: most emotionally relatable for this room.
- Possible combo: build F1 as the engine, demo it on 2 scenarios (Margaret + Wei).

---

## 3. Stuck-payment translator (Payments)
Ana is a freelancer whose international payment was returned. She pastes the bank's reason code or message. The app gives a plain-English cause, what to do next and a pre-written message to the payer. Lower originality.
