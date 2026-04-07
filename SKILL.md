---
name: deriv-ux-writing
description: "Write, audit, or rewrite UX copy for Deriv products - buttons, error messages, empty states, tooltips, modals, onboarding flows, form labels, success/failure states, notifications, and microcopy. Use when writing interface copy, auditing UI text, naming buttons, drafting error messages, or writing tooltips for Deriv product terms. Trigger on: write a button label, what should this error say, rewrite this tooltip, UX copy, microcopy, UI text, in-app copy, or any request involving words inside a product interface. Always fetch the live Deriv glossary before writing copy involving any Deriv product term, trade type, or feature name."
---
 
# Deriv UX writing
 
Write interface copy that earns trust, reduces friction, and drives action. Every word in a product is a design decision. This skill makes those decisions good ones -- in Deriv's voice, with Deriv's terminology, and within the constraints of the screens where traders actually use them.
 
---
 
## Before you write: check the copy bricks and glossary
 
**Always check `References/copy-bricks-1.csv` (or `copy-bricks-2.csv`) first** for any copy request. The copy bricks are a repository of approved UX copy for Deriv products. If a brick exists for the exact element and context you're writing for, use the preferred copy — do not rewrite it.
 
See the [Copy Bricks](#copy-bricks) section below for how to search and apply them.
 
**Always read `References/product-glossary.md` first** if the copy involves any of these:
 
- A trade type (CFD, Accumulator options, Multipliers, Digital options, Vanilla options, etc.)
- A Deriv-specific feature (Deal cancellation, Growth rate, Stop loss, Indicative price, etc.)
- A platform name (Deriv MT5, Deriv cTrader, Deriv GO, Deriv One, SmartTrader, etc.)
- A proprietary market (Derived indices, Synthetic indices, Crash/Boom indices, etc.)
- A Deriv Tokens term (Creator, Buyer, NAV, High-water mark, Minting, etc.)
 
**If the copy involves Deriv One**, read `References/deriv-one-product-context.md` first. It contains MVP scope boundaries, approved tooltips, error patterns, empty states, push notifications, onboarding copy, connection states, and restricted terms specific to this platform. Writing Deriv One copy without checking this file risks referencing features that don't exist yet.
 
### Glossary structure
 
Each entry contains three fields:
 
- **Topic** — the product area (e.g. "Trading focus", "Account management"). Use this to confirm the copy belongs in the right context.
- **Definition** — the approved explanation of the term. Use this as the source of truth for tooltip copy and helper text. Paraphrase for the UI — do not copy the definition verbatim.
- **EU availability** — whether the feature is available to EU-regulated clients. This is critical for UX copy (see below).
 
Using the wrong term — or the right term with wrong capitalisation — damages trust.
 
### EU availability: how to apply it in copy
 
The glossary flags each term as **Available** or **Not available in EU**. Apply this as follows:
 
| Scenario | What to do |
|----------|-----------|
| Writing copy for a feature marked "Not available in EU" | Do not expose this feature in EU-regulated flows. If you're unsure whether the screen is EU-specific, flag to the designer or compliance team before writing. |
| A feature is available in EU but restricted in some non-EU markets | Use positive framing: "Available in selected countries" — never "Not available in your country." |
| Copy must work across both EU and non-EU surfaces | Write for the more restricted version. Flag to the designer that a variant may be needed for non-EU. |
| Tooltip or helper text for an EU-unavailable term appears in a shared codebase | The copy should be written but the component hidden for EU users — confirm with the engineer, don't omit the copy entirely. |
 
---
 
## Deriv's tone in product copy
 
Deriv's voice is **friendly and direct, never condescending**. In UX copy specifically, that means:
 
- Talk to traders as capable adults who understand risk. Don't over-explain the obvious.
- Be warm but get to the point. "Deposit successful. Funds usually appear in a few minutes." Not "Great news! Your deposit has been successfully processed."
- When something goes wrong, stay calm. A loss is serious. The copy should be steady, not alarming.
- Use "you" and "we" -- the relationship is clear. Avoid the passive voice that hides who does what.
- Simple language, always. Deriv's traders come from 38+ markets. Many are not native English speakers. If a sentence sounds clever, it may not translate.
 
### Tone calibration by context
 
| Context | Tone | Example |
|---------|------|---------|
| Onboarding | Warm, encouraging | "Let's get your account set up. It takes about 3 minutes." |
| Trade placement | Focused, efficient | "Place trade" not "Let's go!" |
| Error / failure | Calm, helpful | "Something went wrong. Try again or contact support." |
| Financial loss / stop-out | Steady, factual | "Your position has been closed. The market reached your stop-out level." |
| Success | Confirming, brief | "Withdrawal submitted. We'll process it within 1-3 business days." |
| Empty state | Inviting, low pressure | "Your trades will appear here. Ready to start?" |
| Destructive action | Clear, no drama | "Delete your account? This can't be undone." |
 
---
 
## Core principles
 
### 1. Say the thing first
No preamble. No "please note that." No "in order to." The most important word goes first.
 
| ❌ | ✅ |
|----|-----|
| Please note that your session has expired | Your session has expired |
| In order to proceed, you'll need to verify your identity | Verify your identity to continue |
| We wanted to let you know that your deposit was successful | Deposit successful |
| Kindly be informed that this feature is unavailable | This feature isn't available yet |
 
### 2. Active voice
Passive voice hides who does what. In a product, someone always acts.
 
| ❌ | ✅ |
|----|-----|
| Your account has been verified | We've verified your account |
| An error was encountered | Something went wrong |
| Your withdrawal has been submitted | We've submitted your withdrawal |
| Deal cancellation has been activated | Deal cancellation is now active |
 
### 3. Positive framing
Tell traders what they *can* do, not what they *can't*. This is a hard rule for geographic restrictions.
 
| ❌ | ✅ |
|----|-----|
| Not available in your country | Available in selected countries |
| You can't withdraw until you verify | Verify your identity to unlock withdrawals |
| This feature is not supported on mobile | Available on desktop |
| Stop loss is not available during deal cancellation | Stop loss is available once deal cancellation expires |
 
### 4. Be specific
Vague copy forces traders to guess. Specific copy removes doubt -- especially for financial actions.
 
| ❌ | ✅ |
|----|-----|
| We'll be in touch soon | We'll respond within 2 business days |
| Your request is being processed | Withdrawal processing -- usually 1-3 hours |
| Please try again later | Try again in a few minutes |
| A small fee applies | A cancellation fee of [amount] applies |
 
### 5. Plain language, not jargon
Use Deriv's approved terminology (from the glossary), but write around it plainly. The label can say "Barrier offset" -- the tooltip explains it in plain language.
 
| ❌ Jargon | ✅ Plain |
|---------|---------|
| Crystallise your position | Close your trade to lock in your profit or loss |
| The contract has lapsed | Your trade has expired |
| Initiate a deposit | Deposit funds |
| The indicative price is non-deterministic | This price may change before your trade closes |
 
### 6. One job per string
Each label, message, or instruction does one thing. If copy is trying to explain two things at once, that's a flow problem -- flag it to the designer, don't solve it with longer copy.
 
---
 
## Character limits by element and view
 
Mobile is the primary trading surface for most Deriv users. Write for mobile first, then verify it holds on desktop.
 
### Hard limits (truncation or breakage if exceeded)
 
| Element | Mobile limit | Desktop limit | Notes |
|---------|-------------|--------------|-------|
| Push notification title | 30-50 chars | 50-65 chars | iOS truncates at ~50 chars on lock screen |
| Push notification body | 100-150 chars | 150-200 chars | Android shows ~2 lines; iOS ~3 |
| Button label (primary) | 16-20 chars | 20-28 chars | Shorter is always better. 2-3 words ideal. |
| Button label (secondary) | 12-18 chars | 18-24 chars | |
| Toast / snackbar | 40-60 chars | 60-80 chars | One line only. No punctuation if it's a single sentence fragment. |
| Modal title | 25 chars | 25 chars | Hard cap — applies across mobile and desktop |
| Modal body | 80-120 chars | 120-200 chars | One sentence on mobile. Two max on desktop. |
| Tooltip | 60-80 chars | 80-120 chars | One sentence. Never wrap to more than 2 lines on mobile. |
| Form field label | 15-25 chars | 20-35 chars | |
| Form field helper text | 50-70 chars | 70-100 chars | Appears below field. Keep to one line on mobile. |
| Empty state heading | 25-35 chars | 35-50 chars | |
| Empty state body | 60-80 chars | 80-120 chars | |
| Error message | 50-80 chars | 80-120 chars | Include what to do next within the limit. |
| Navigation label | 10-15 chars | 15-20 chars | |
| Tab label | 8-12 chars | 10-15 chars | |
| Page title / screen header | 15-25 chars | 20-35 chars | |
 
### Soft limits (best practice, not hard constraints)
 
| Element | Target | Notes |
|---------|--------|-------|
| Coachmark / tooltip (rich) | 100-140 chars | Expandable tooltips can go longer, but lead with the one-liner |
| Onboarding screen body | 80-120 chars | One instruction per screen |
| Success screen body | 60-100 chars | Confirm + what's next in two sentences max |
| Placeholder text | 20-30 chars | Hint, not instruction. Never use as a substitute for a label. |
| Inline warning | 60-90 chars | Appears inline in a form or panel -- keep shorter than an error |
 
### Mobile-specific rules
 
- **Line breaks matter.** On mobile, a 60-char tooltip wraps at roughly 30 chars. Write with natural break points -- don't let a key word wrap awkwardly.
- **No parentheses in tight UI.** They read as optional and get ignored. If the info matters, it gets its own line or tooltip.
- **Abbreviate only with approved forms.** "Deriv MT5" not "MT5." "CFDs" not "Contracts for Difference" -- but define on first use if it's a new user flow.
- **Tap targets need labels that work at a glance.** If the label only makes sense after reading surrounding context, it's too short or too abstract.
- **Numbers in tight spaces:** Use numerals always (5%, not five per cent). Use commas for 4+ digits (1,200 USD). Truncate large numbers with units only if the unit is obvious: "1.2K" only in charts, never in financial confirmations -- always show full amount.
 
---
 
## Copy patterns by element
 
### Buttons and CTAs
 
The button label is the contract between the product and the trader. It answers: *what happens when I tap this?*
 
**Rules:**
- Verb-first always: "Add account", "Verify identity", "Place trade"
- 2-3 words for primary actions. 4 words maximum -- after that, rethink the flow
- Match the label to the outcome, not the intent
- Never: "Click here", "Submit", "OK", "Yes", "No", "Proceed"
- Destructive actions: name what's being destroyed
 
| Context | ❌ | ✅ | Char count |
|---------|---|-----|-----------|
| Confirm account deletion | Yes, delete | Delete account | 14 |
| Cancel deletion | No | Keep account | 12 |
| Leave a flow | No, stay | Stay here | 9 |
| Confirm leaving | Yes, leave | Leave anyway | 12 |
| End session | Logout | Log out | 7 |
| Start onboarding | Get started | Create your account | 19 |
| Confirm a trade | Confirm | Place trade | 11 |
| Open position | Open | Open position | 13 |
| Retry after error | Try again | Retry | 5 |
| Activate deal cancellation | Enable | Cancel this trade | 17 |
| Close a trade early | Close | Close trade | 11 |
| Add funds | Add money | Deposit funds | 13 |
 
### Error messages
 
Errors are the most read copy in the product. Traders read them under stress and need an immediate next action.
 
**Structure:** What happened → What to do (→ Why, only if it helps)
 
**Deriv-specific error patterns:**
 
| Error type | ❌ | ✅ | Notes |
|-----------|---|-----|-------|
| Insufficient funds | Insufficient funds | Not enough funds. Deposit to continue. | Link "Deposit" if possible |
| Deal cancellation conflict | Stop loss unavailable | Stop loss is available once deal cancellation expires. | Positive framing -- not "not available" |
| Maximum stake reached (Accumulator) | Maximum aggregate open stake reached | New positions paused. Try again when the stake limit drops. | Plain language for a complex constraint |
| Position closed at stop-out | Stop-out triggered | Your position has been closed. The market reached your stop-out level. | Steady tone -- this is a loss event |
| Session expired | Session expired | Your session expired. Log in to continue. | Not "please log in again" -- just state and act |
| Network error | Network error | No connection. Check your internet and try again. | |
| Wrong credentials | Incorrect username or password | Wrong email or password. Try again or reset your password. | |
| System error | Something went wrong. Please try again. | We hit a snag. Try again or contact support. | |
| Trade failed | Trade failed | Your trade didn't go through. Try again. | |
| Indicative price changed | Price has changed | The price changed before your trade opened. Review and try again. | Don't say "indicative price" in the error -- say what happened |
 
**Tone rules:**
- Never blame: "You entered an invalid..." → "Enter a valid..."
- Never use error codes in the message body (logs only)
- For financial loss events: factual and steady, not apologetic or alarming
- Always include what to do next -- even if it's just "Try again"
 
### Tooltips and helper text
 
Tooltips translate Deriv's product terms into plain language. They're the bridge between the label (which uses official terminology) and the trader (who may not know it yet).
 
**Formula:** [What it does] + [Why it matters to the trader] -- in one sentence.
 
**Deriv product tooltips -- approved language:**
 
| Label | Tooltip | Char count |
|-------|---------|-----------|
| Growth rate | The percentage your payout grows for each tick within the barrier. Choose between 1% and 5%. | 92 |
| Deal cancellation | Cancel this trade within the chosen time frame and get your stake back. A fee applies. | 87 |
| Stop loss | Automatically closes your trade if losses reach this amount. | 57 |
| Take profit | Automatically closes your trade when you reach this profit. | 57 |
| Barrier | Your target price. The trade result depends on where the market ends up relative to this. | 89 |
| Barrier offset | The distance between your target price and the current market price. | 68 |
| Indicative price | Your estimated payout if you sell now. This may change as the market moves. | 75 |
| Multiplier | Amplifies your potential profit. Higher multiplier = greater gains and losses. | 76 |
| Buy price | The amount you pay to open this trade. With options, this is the most you can lose. | 84 |
| Payout per point | Your profit or loss for each point of price movement. You profit when payout exceeds your stake. | 95 |
| Leverage | Multiplies your market exposure. Higher leverage increases both potential gains and losses. | 91 |
| Entry spot | The market price when your trade opened. | 40 |
| Exit spot | The market price when your trade closes. | 41 |
| Deriv MT5 password | Used to log in to Deriv MT5. Different from your main Deriv password. | 70 |
| Account currency | The currency used for all trades, deposits, and withdrawals on this account. | 76 |
| Reference ID | A unique number for this transaction. Find all reference IDs in Reports. | 70 |
| High-water mark (Tokens) | A performance fee applies only when the token price rises above the previous highest value. | 91 |
| NAV / Account value (Tokens) | Your account value is calculated as cash + open positions, and updates live. | 76 |
 
**Rules:**
- One sentence. Full stop at the end.
- Don't repeat the label -- add what the label doesn't say
- For financial risk: always include the risk direction (higher = more risk)
- Mobile: keep under 80 chars so it fits in 2 lines without scroll
 
### Modals and confirmation dialogs
 
Modals interrupt the flow. The trader has to deal with this before they can do anything else. Earn that interruption.
 
**Structure:**
- **Title:** The decision being made. Not a question if it can be avoided. Max 25 chars.
- **Body:** The consequence, once. One sentence. Max 120 chars on mobile.
- **Primary button:** The action (specific verb). Never "Yes."
- **Secondary button:** The exit. Never "No." "Cancel" is fine. "Keep [thing]" is better.
 
| Scenario | ❌ | ✅ |
|----------|----|-----|
| Delete account -- title | Are you sure? | Delete your account? |
| Delete account -- body | This action cannot be undone. | Your account, history, and funds will be permanently removed. |
| Withdraw -- title | Confirm withdrawal | Withdraw [amount]? |
| Close trade -- title | Confirm close | Close this trade? |
| Deal cancellation active -- body | Deal cancellation is active. Stop loss and take profit are unavailable. | Stop loss and take profit are unavailable while deal cancellation is active. |
| Leave onboarding -- title | Are you sure you want to leave? | Leave this step? |
| Leave onboarding -- body | Your progress may be lost. | Your progress on this step won't be saved. |
 
### Success and confirmation states
 
Success copy confirms the action and, where relevant, tells the trader what's next. Two sentences maximum on mobile.
 
| Event | ❌ | ✅ |
|-------|----|-----|
| Deposit successful | Transaction successful | Deposit successful. Funds usually appear within a few minutes. |
| Withdrawal submitted | Request submitted | Withdrawal submitted. We'll process it within 1-3 business days. |
| Account verified | Your account has been verified | You're verified. You can now deposit and trade. |
| Password changed | Password changed successfully | Password updated. You're still logged in on all devices. |
| Trade placed | Order executed | Trade placed. |
| Deal cancellation activated | Done | Deal cancellation is active. Stop loss and take profit are paused. |
| Position closed (manual) | Position closed | Trade closed. Your final profit/loss has been recorded. |
 
### Push notifications
 
Push notifications are the only UX copy that arrives when the trader isn't looking at the product. They have one job: give the trader a reason to open the app.
 
**Hard format:**
- Title: 30-50 chars. Sentence case. No full stop.
- Body: 100-150 chars. One sentence. Specific. Actionable.
 
| Type | Title | Body |
|------|-------|------|
| Trade alert | Trade alert | A new opportunity in [market]. Open the app to trade now. |
| Stop loss triggered | Your trade has been closed | Your [asset] position reached your stop loss. Check your account. |
| Deposit confirmed | Deposit confirmed | [Amount] has been added to your account. You're ready to trade. |
| Withdrawal processed | Withdrawal sent | [Amount] is on its way. It usually arrives within [timeframe]. |
| Deal cancellation expiring | Cancellation window closing | Your deal cancellation expires in 5 minutes. Stop loss and take profit will be available after. |
| Verification required | Action required | Verify your identity to keep trading without interruption. |
| Account limit reached | Trading paused | You've reached your account limit. Visit your account settings to continue. |
 
### Empty states
 
Empty states tell a trader what's missing, why it matters, and what to do about it. They're not error states -- no apology needed.
 
**Structure:** What's missing (heading) + Why/what you can do here (body, 1 sentence) + CTA if relevant
 
| Screen | Heading | Body | CTA |
|--------|---------|------|-----|
| No trade history | No trades yet | Your trades will appear here once you start. | Place your first trade |
| No open positions | No open positions | You have no active trades right now. | Explore markets |
| No notifications | You're all caught up | We'll notify you when something needs your attention. | -- |
| No search results | No results for "[query]" | Try a different search or browse all options. | Browse markets |
| No funds in account | Your account is empty | Deposit funds to start trading. | Deposit funds |
| No tokens (Tokens) | No tokens yet | Explore the Marketplace to find tokens to buy. | Go to Marketplace |
 
### Onboarding and instructional copy
 
One action per screen. Tell traders what to do -- not what the process is.
 
**Rules:**
- Lead with the instruction, not the context
- Progress markers: always show step count ("Step 2 of 4")
- Explain why only when it removes hesitation
- Avoid "please" -- it adds length without adding warmth
 
| Context | ❌ | ✅ |
|---------|---|-----|
| ID upload | Please upload a valid government-issued ID | Upload a photo of your passport or national ID |
| Why it's needed | We are required by law to verify your identity | Required by financial regulations. Takes about 2 minutes. |
| Processing | Processing... | Checking your document -- this takes about 30 seconds |
| Step context | You are on step 3 | Step 3 of 5 |
| Completing KYC | You have successfully verified your identity | You're verified. You can now trade. |
 
---
 
## Deriv terminology -- hard rules
 
### Banned words
 
These are regulatory and brand rules. No exceptions.
 
| ❌ Never | ✅ Instead | Why |
|---------|-----------|-----|
| invest / investment | trade | Regulatory compliance |
| investor | trader | Regulatory compliance |
| win | earn / receive | Regulatory compliance |
| click here | descriptive verb + noun ("Visit the Help centre") | Accessibility and clarity |
| soon | specific timeframe ("within 2 business days") | Precision |
| a small fee | the actual fee amount | Specificity -- always show the number |
| not available in your country | available in selected countries | Positive framing -- hard rule |
 
**On "stake":** Allowed as a UI label for the input field and in trade mechanics context. The banned substitution ("initial capital") applies in regulatory/compliance-facing copy. If unsure, check with compliance.
 
### Banned words -- Deriv P2P
 
These apply specifically to Deriv P2P copy. They reflect agreed terminology with the P2P design team.
 
| ❌ Never | ✅ Instead | Why |
|---------|-----------|-----|
| hide ads | pause ads | "Hide" implies the ad disappears entirely. "Pause" correctly communicates that the ad still exists but is temporarily inactive. |
| advertisers | sellers | "Advertisers" sounds promotional and is too vague. Use "sellers" to match the opposing term "buyers" — the P2P marketplace is built around this buyer/seller pairing. |
 
**Note on "Ads":** The term "Ads" (capital A) is approved for use in Deriv P2P when referring to listings. The ban on "advertisers" does not extend to "Ads" itself — only to the word used for the people posting them.
 
### Restricted terms -- Deriv One
 
These apply on top of the global banned words above. Full details in `References/deriv-one-product-context.md`.
 
| ❌ Never in Deriv One copy | ✅ Instead | Why |
|---------------------------|-----------|-----|
| cTrader | (omit entirely) | Backend is cTrader, but the brand is Deriv One. Never expose the third-party name in user-facing copy. |
| demo account (MVP) | (omit entirely) | No demo in MVP. Don't reference until Phase 1.5. |
| deposit / withdraw (inside Deriv One) | Add funds via your Deriv account | No in-app cashier in MVP. Deep-link to Deriv Cashier. |
| pending order / limit order / stop order (MVP) | (omit entirely) | Only market orders in MVP. Don't reference unavailable order types. |
| forex / stocks / commodities (MVP) | Synthetic Indices | Only Synthetic Indices at launch. Don't mention markets that aren't live yet. |
 
**Note:** Items marked "(MVP)" will be removed from this list as those features ship. Check the product context file for the latest phase status.
 
### Platform names -- exact capitalisation
 
These appear in error messages, account selectors, help text, and onboarding across all surfaces. One wrong character damages consistency.
 
| ✅ Correct | ❌ Never |
|-----------|---------|
| Deriv MT5 | dMT5, MT5 alone, Deriv MT 5 |
| Deriv cTrader | Deriv Ctrader, DCtrader, ctrader |
| Deriv GO | Deriv Go, DerivGo |
| Deriv Bot | dBot, DerivBot |
| Deriv Trader | DTrader, dTrader |
| SmartTrader | Smart Trader, Smarttrader |
| Deriv Nakala | Nakala alone |
| Deriv P2P | DerivP2P, Deriv p2p |
| Deriv One | Deriv one, DerivOne, D1, Deriv 1, deriv one |
 
| Swap-free | Swap-Free, swap-free, SwapFree, Swap free |
| Zero Spread | Zero spread, zero-spread, ZeroSpread, zero spread |
 
### Trade type capitalisation
 
- Accumulator options (not "Accumulators")
- Digital options (not "Digitals")
- Multipliers (capital M as product name)
- CFDs (never "CFD's")
- Vanilla options, Lookbacks options -- lowercase "options"
- Rise/Fall, Higher/Lower, Ends Between, Stays Between -- as shown
 
### Derived indices -- use the right level
 
| Use | When |
|-----|------|
| Derived indices | Umbrella term for the whole category |
| Synthetic indices | The simulated subset (Volatility, Crash/Boom, Jump, etc.) |
| Basket indices | Currency basket products |
| Derived FX | Simulated forex products |
 
Never use "Synthetic indices" as a synonym for "Derived indices." They're a subset, not the whole.
 
### British English -- apply consistently
 
| ✅ British | ❌ American |
|----------|-----------|
| authorise | authorize |
| centre | center |
| colour | color |
| programme | program (unless proper noun: "Microsoft Program") |
| fulfil | fulfill |
| licence (noun) | license (noun) |
| practise (verb) | practice (verb) |
| realise | realize |
 
### Sentence case -- everywhere
 
Buttons, headings, labels, navigation, tab names, modal titles -- all sentence case. No Title Case except proper nouns and product/platform names.
 
✅ "Your account settings"
✅ "Deposit funds"
✅ "Trade on Deriv MT5"
❌ "Your Account Settings"
❌ "Deposit Funds"
 
---
 
## Copy bricks
 
Copy bricks are a repository of approved UX copy for Deriv products. Each brick is a real, shipped, or approved string — confirmed through design and compliance — so they are the highest-confidence source for copy decisions.
 
The bricks live in two reference files with identical data, just different column ordering:
- `References/copy-bricks-1.csv`
- `References/copy-bricks-2.csv`
 
Use whichever is easier to query for the task at hand.
 
### How to read a brick
 
Each row contains:
 
| Column | What it tells you |
|--------|-------------------|
| `✅ Preferred copy` | The approved string to use. Use this verbatim or as the authoritative model. |
| `❌ Less preferred copy` | Alternatives that have been rejected or ranked lower. Avoid these. May contain multiple options separated by `•` or `\n`. |
| `UX Element` | Where the copy appears — e.g. "Section title", "Action screen: title", "Ghost button", "Sub-section title" |
| `Component type` | The UI pattern — Page section, Modal / Bottomsheet, or Coachmark |
| `Component slot` | The role within the component — Title, CTA, Label, Body |
| `Description` | Context for when this brick applies — read this to confirm it's the right match |
| `Intent` | The purpose of the copy: **Guidance** (directs the user), **Success** (confirms a completed action), **Confirmation** (asks the user to verify before acting) |
| `Product` | Which Deriv product(s) this brick applies to — e.g. UAE, MT5, Wallets, P2P, Deriv GO, SmartTrader |
| `Status` | Done = shipped or approved; Not started = draft |
| `Unique ID` | Numeric ID for referencing a specific brick |
 
### How to use copy bricks
 
**1. Search by element and context first.** Match on `UX Element` + `Component type` + `Intent` + `Product`. A brick only applies if the description matches the user's context.
 
**2. Use the preferred copy.** If a matching brick exists with Status = Done, the `✅ Preferred copy` is the answer. Do not rewrite it unless the user explicitly asks for a variant.
 
**3. Flag less preferred copy.** If the user has submitted copy that matches a `❌ Less preferred copy` value, flag it and recommend the preferred alternative. Explain briefly why (e.g. passive voice, wrong framing, imprecise).
 
**4. No exact match? Write fresh — guided by the bricks.** If no brick covers the exact context, treat the closest bricks as tone and pattern references, then apply the writing principles in this skill.
 
**5. Templated bricks with placeholders.** Some bricks use `<variable>` syntax, e.g. `<amount> <currency> transferred from your <currency> Wallet.` Replace placeholders with the actual values or keep them as tokens if writing template copy.
 
### When bricks take precedence over your own writing
 
| Situation | Action |
|-----------|--------|
| Exact element + product + intent match, Status = Done | Use the preferred copy as-is |
| Close match but different product | Use as a strong pattern reference; adapt minimally |
| User submits copy matching a less-preferred brick | Flag it, recommend the preferred copy |
| No matching brick | Write from scratch using the principles in this skill |
| User wants to deviate from a preferred brick | Flag the deviation and confirm intent — bricks reflect approved decisions |
 
---
 
## Audit checklist
 
Run this before any copy ships:
 
**Clarity**
- [ ] Does it start with the most important word?
- [ ] Can any word be removed without losing meaning?
- [ ] Is the voice active?
- [ ] Is it free of jargon a first-time trader wouldn't know?
 
**Action**
- [ ] Does it tell the trader what to do, not just what happened?
- [ ] If it's a button: is the label a verb that matches the outcome?
- [ ] If it's an error: does it say what to do next?
- [ ] If it's a modal: does the title name the decision?
 
**Deriv rules**
- [ ] Does it avoid the banned words (invest, win, click here)?
- [ ] Are platform and product names capitalised correctly?
- [ ] Is it sentence case?
- [ ] Is it British English?
- [ ] Does it use positive framing for restrictions?
 
**Mobile**
- [ ] Is it within the character limit for its element and surface?
- [ ] Does it read clearly on a 5-inch screen at a glance?
- [ ] If it's a tooltip: does it fit in 2 lines without scroll?
- [ ] If it's a notification: is it specific and actionable without opening the app?
 
---
 
## Output format
 
**For single copy requests:**
**[Element type]:** `[Copy]`
*Why:* [One-line rationale -- only when reasoning isn't obvious]
 
**For audits:**
- Original: `[copy]`
- Issue: [one line]
- Revised: `[copy]`
 
**For full flows:**
Use a table with columns: Screen / Element / Copy / Char count / Notes
 
**Always flag:**
- If the copy is hitting its character limit and the message needs to be shorter
- If a flow problem is causing the copy to overload (more than one instruction per screen)
- If a Deriv product term appears that isn't in the glossary yet
 
---
 
## References
 
`References/copy-bricks-1.csv` — Repository of 295 approved UX copy strings across Deriv products. Columns: `✅ Preferred copy`, `❌ Less preferred copy`, `UX Element`, `Component type`, `Component slot`, `Description`, `Intent`, `Product`, `Status`, `Unique ID`. **Check this first for any copy request before writing from scratch.**
 
`References/copy-bricks-2.csv` — Same 295 copy bricks as copy-bricks-1.csv, with different column ordering. Use whichever is easier to query for the task at hand.
 
`References/product-glossary.md` — Deriv-approved definitions for all trade types, features, platforms, and markets. Includes Deriv One platform terms. Last updated April 2026. Each entry includes: **Topic** (product area), **Definition** (source of truth for tooltip and helper text copy), and **EU availability** (Available / Not available in EU — apply as described in the "Before you write" section above). **Read this before writing copy that involves any product term.**
 
`References/deriv-one-product-context.md` — Product context, MVP scope, and approved UX copy patterns for Deriv One. Includes: tooltips for info icons, error messages, empty states, push notifications, modals, onboarding/activation copy, connection states, and restricted terms. **Read this before writing any Deriv One copy.**
 
For formatting rules (dates, currency, abbreviations) and content-type constraints (email subject lines, push notification limits): refer to the Deriv Content Style skill.
