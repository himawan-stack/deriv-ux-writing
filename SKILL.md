[SKILL (2).md](https://github.com/user-attachments/files/27468043/SKILL.2.md)
---
name: deriv-ux-writing
description: "Write, audit, or rewrite UX copy for Deriv products - buttons, error messages, empty states, tooltips, modals, onboarding flows, form labels, success/failure states, notifications, and microcopy. Use when writing interface copy, auditing UI text, naming buttons, drafting error messages, or writing tooltips for Deriv product terms. Trigger on: write a button label, what should this error say, rewrite this tooltip, UX copy, microcopy, UI text, in-app copy, or any request involving words inside a product interface. Always fetch the live Deriv glossary before writing copy involving any Deriv product term, trade type, or feature name."
---

# Deriv UX writing

Write interface copy that earns trust, reduces friction, and drives action. Every word in a product is a design decision. This skill makes those decisions good ones -- in Deriv's voice, with Deriv's terminology, and within the constraints of the screens where traders actually use them.

---

## Before you write: check the glossary

**Always read `References/product-glossary.md` first** if the copy involves any of these:

- A trade type (CFD, Accumulator options, Multipliers, Digital options, Vanilla options, etc.)
- A Deriv-specific feature (Deal cancellation, Growth rate, Stop loss, Indicative price, etc.)
- A platform name (Deriv MT5, Deriv cTrader, Deriv GO, SmartTrader, etc.)
- A proprietary market (Derived indices, Synthetic indices, Crash/Boom indices, etc.)
- A Deriv Tokens term (Creator, Buyer, NAV, High-water mark, Minting, etc.)

The glossary covers Deriv's own terminology only. For third-party platforms Deriv references in its UI -- App Store, Google Play, HUAWEI AppGallery, and similar -- the rules live in this skill (see "App store names" under "Deriv terminology -- hard rules"). If a third-party name isn't covered there either, ask the brand team before writing.

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
- Verb forms: write the action as two words when it's a verb. "Log out", "Log in", "Sign up", "Sign in" -- not "Logout", "Login", "Signup", "Signin." (Noun forms keep the one-word version: "the login screen", "your sign-up details.")

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
| Download iOS app | Download | Get it on the App Store | 23 |
| Download Android app | Download | Get it on Google Play | 21 |
| Download Huawei app | Download | Get it on HUAWEI AppGallery | 27* |
| App download (store-agnostic) | Download | Download Deriv GO | 17 |

\* "Get it on HUAWEI AppGallery" exceeds the 20-char mobile primary button limit. Use it on desktop or where the button can wrap to two lines. For tight mobile slots, use a generic "Download Deriv GO" CTA above the three store badges instead.

**Where the "the" rule does and doesn't apply in CTAs:**

- ✅ Body copy and self-written CTAs: "Available on the App Store, Google Play, and HUAWEI AppGallery." (62 chars -- body copy, not a button)
- ✅ Self-written button: "Get it on the App Store"
- ❌ Self-written button without "the": "Get it on App Store"
- ⚠️ Official store badges: use the locked-up badge text as supplied -- do not edit. The "the" rule applies only to copy you write.

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
| advertiser / advertisers (Deriv P2P) | seller / sellers | Deriv P2P pairs sellers with buyers. "Advertiser" is too vague and reads promotional. See "Deriv P2P -- role terminology" below. |

**On "stake":** Allowed as a UI label for the input field and in trade mechanics context. The banned substitution ("initial capital") applies in regulatory/compliance-facing copy. If unsure, check with compliance.

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

### Account-type modifiers -- placement

Modifiers like "real" and "demo" go before the full Deriv platform name, never inside it. The platform name is a locked proper noun and must not be split.

| ✅ Correct | ❌ Never |
|-----------|---------|
| real Deriv cTrader account | Deriv real cTrader account |
| demo Deriv MT5 account | Deriv demo MT5 account |
| real Deriv GO account | Deriv real GO account |
| demo Deriv Bot account | Deriv demo Bot account |

The modifier itself is lowercase ("real", "demo") -- it's a descriptor, not part of the product name. Capitalise only when it begins a sentence:

- ✅ "Real Deriv cTrader account is available"
- ✅ "Activate your real Deriv cTrader account now"
- ❌ "Activate your Real Deriv cTrader account now"

This rule applies to all Deriv platforms: Deriv MT5, Deriv cTrader, Deriv GO, Deriv Bot, Deriv Trader, SmartTrader, Deriv Nakala, Deriv P2P.

### Deriv P2P -- role terminology

Deriv P2P is a peer-to-peer marketplace where users exchange Deriv funds for local currency. The platform is built around two roles: **sellers** and **buyers**. Use these terms consistently across all Deriv P2P copy.

| Role | Definition | Use this | Never use |
|------|-----------|----------|-----------|
| Seller | A user who posts an ad to sell their Deriv funds for local currency | seller / sellers | advertiser / advertisers |
| Buyer | A user who responds to an ad to buy Deriv funds | buyer / buyers | -- |
| Listing | The post a seller creates with their rate, limits, and payment methods | ad / ads (capital A when starting a sentence) | advertisement, listing, post |

**Why "sellers" and not "advertisers":**

- **It pairs.** "Sellers" sits naturally opposite "buyers" -- the marketplace is built on this pairing. "Advertiser" has no clean opposite.
- **It's specific.** "Advertiser" is vague -- in most contexts it implies someone running a marketing campaign. "Seller" tells the user exactly what the person does.
- **It's not promotional.** "Advertiser" reads like marketing language. Deriv P2P is a transactional marketplace, not a promotional surface.

**Roles are reversible.** The same user can be a seller on one transaction and a buyer on another. Don't write copy that assumes a user is permanently one or the other -- e.g. avoid "as a seller, you will..." in onboarding. Frame role-specific guidance around the action: "When you sell, ..." / "When you buy, ..."

**On "ads":**

- The term `ads` (and `Ads` at the start of a sentence) is the approved word for listings on Deriv P2P. The ban on "advertiser" does not extend to "ad" or "ads."
- Capitalise as `Ads` only when it begins a sentence or is a navigation/tab label following sentence case rules. Inline, it's lowercase: "Browse ads," "your active ads."

**Examples in context:**

| ❌ | ✅ |
|----|-----|
| See when advertisers were last online | See when sellers were last online |
| Top-rated advertisers in your region | Top-rated sellers in your region |
| You have 3 active advertisements | You have 3 active ads |
| Become an advertiser on Deriv P2P | Post your first ad on Deriv P2P |
| Advertiser rating: 4.8 | Seller rating: 4.8 |
| Block this advertiser | Block this seller |

> **Source note:** This subsection reflects guidance surfaced in the Deriv P2P workspace. If a Deriv P2P feature spec uses "advertiser" in upstream documentation (engineering tickets, API responses, designer files), translate to "seller" at the UI layer -- internal naming and user-facing copy don't have to match.

### App store names -- exact capitalisation and article use

These appear in download CTAs, footers, onboarding, and "get the app" prompts. Both the spelling and the article ("the") are part of the rule.

#### Spelling and capitalisation

| ✅ Correct | ❌ Never |
|-----------|---------|
| App Store | Apple Store, App store, Appstore, App Storage, iOS Store |
| Google Play | Play Store, Google Store, Google play, GooglePlay, Google Play Store |
| HUAWEI AppGallery | Huawei App Gallery, Huawei AppGallery, HUAWEI App Gallery, AppGallery alone |

"App Store" and "Google Play" use Title Case as proper nouns -- this is one of the few exceptions to the sentence case rule. "HUAWEI" is always all caps; "AppGallery" is one word with a capital A and capital G.

#### The "the" rule

Always use **"the"** before an app store name. When two or more app store names appear in the same list, "the" goes on the first name only -- not repeated before each one.

| Scenario | ✅ Correct | ❌ Never |
|----------|-----------|---------|
| Single store -- App Store | Download from the App Store. | Download from App Store. |
| Single store -- Google Play | Get it on the Google Play. | Get it on Google Play. |
| Single store -- AppGallery | Find it on the HUAWEI AppGallery. | Find it on HUAWEI AppGallery. |
| Two stores | Available on the App Store and Google Play. | Available on the App Store and the Google Play. |
| Three stores | Available on the App Store, Google Play, and HUAWEI AppGallery. | Available on App Store, Google Play, and HUAWEI AppGallery. |
| Three stores -- repeated "the" | Available on the App Store, Google Play, and HUAWEI AppGallery. | Available on the App Store, the Google Play, and the HUAWEI AppGallery. |
| Mid-sentence | Find Deriv GO on the App Store. | Find Deriv GO on App Store. |

#### Exception: badge CTAs and lockups

Official download badges are graphic lockups -- not editable copy. Use them as supplied by Apple, Google, and Huawei without modification. Two things to know:

- The "the" rule applies to body copy, button labels you write yourself, and surrounding text -- not to the locked-up badge artwork.
- Some official badges use forms that wouldn't pass this skill's rules in body copy (for example, Huawei's badge reads "Explore it on AppGallery" without "HUAWEI" and without "the"). That's fine *inside the badge* because it's brand artwork. The moment you write the same phrase in body copy or a custom button, the standard rules apply: "HUAWEI AppGallery" with "the."

#### Edge cases

- **Possessives:** Avoid "the App Store's policy" in UI copy -- rephrase as "App Store policy" or "policy on the App Store." Possessives of proper nouns with "the" read awkwardly.
- **Starting a sentence:** "The" stays lowercase mid-sentence and is capitalised only when it begins a sentence: "The App Store version is updated weekly."
- **Headings and button labels:** The "the" rule still applies. ✅ "Get it on the App Store" -- ❌ "Get it on App Store." If character limits force a cut, switch to a generic CTA (e.g. "Download Deriv GO") rather than dropping "the" or shortening the store name -- both are part of the brand rule.
- **Plural / generic reference:** When referring to app stores generically (not by name), lowercase and no special article rule: "available in major app stores." The rule only applies when naming a specific store.
- **Spacing in lists:** Use a single space after each comma. Never two spaces, never a missing space. ✅ "the App Store, Google Play, and HUAWEI AppGallery" -- ❌ "the App Store,  Google Play, and HUAWEI AppGallery" or "the App Store ,Google Play, and HUAWEI AppGallery."

### Trade type capitalisation

- Accumulator options (not "Accumulators")
- Digital options (not "Digitals")
- Multipliers (capital M as product name)
- CFDs (never "CFD's")
- Vanilla options, Lookbacks options -- lowercase "options"
- Rise/Fall, Higher/Lower, Ends Between, Stays Between -- as shown

### Derived Indices -- use the right level

| Use | When |
|-----|------|
| Derived Indices | Umbrella term for the whole category |
| Synthetic Indices | The simulated subset (Volatility, Crash/Boom, Jump, etc.) |
| Basket Indices | Currency basket products |
| Crypto Indices | Cryptocurrency-based indices |
| Derived FX | Simulated forex products |

Never use "Synthetic Indices" as a synonym for "Derived Indices." They're a subset, not the whole.

Note: These category names use Title Case as proper nouns -- one of the exceptions to the sentence case rule, alongside platform names and app store names.

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

### Currency names -- lowercase

Currency names are common nouns, not proper nouns. Lowercase the currency word even when the country/region prefix is capitalised or abbreviated.

| ✅ Correct | ❌ Incorrect |
|-----------|-------------|
| US dollar | US Dollar |
| Australian dollar | Australian Dollar |
| euro | Euro |
| pound sterling | Pound Sterling |
| Japanese yen | Japanese Yen |

This applies to body copy, labels, tooltips, and modal text. For tight spaces, use the ISO code instead (USD, EUR, GBP, JPY, AUD).

### Sentence case -- everywhere

Buttons, headings, labels, navigation, tab names, modal titles -- all sentence case. No Title Case except proper nouns and product/platform names.

Proper nouns include Deriv product/platform names ("Deriv MT5", "Deriv GO"), Deriv indices category names ("Derived Indices", "Synthetic Indices", "Basket Indices", "Crypto Indices"), and third-party platform names ("App Store", "Google Play", "HUAWEI AppGallery"). These keep their official capitalisation even mid-sentence.

✅ "Your account settings"
✅ "Deposit funds"
✅ "Trade on Deriv MT5"
✅ "Get it on the App Store"
❌ "Your Account Settings"
❌ "Deposit Funds"
❌ "Get it on the app store"

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
- [ ] If "real" or "demo" appears with a platform name: is the modifier placed before the full platform name (e.g. "real Deriv MT5 account"), not splitting it?
- [ ] If app store names appear: is each one spelled correctly (App Store, Google Play, HUAWEI AppGallery) and is "the" used before the first one only?
- [ ] If the copy is for Deriv P2P: does it use "seller / buyer" (never "advertiser") and "ads" (never "advertisements")?
- [ ] Is it sentence case?
- [ ] Is it British English?
- [ ] Are currency names lowercase (US dollar, euro, yen) unless using the ISO code?
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

`References/product-glossary.md` — Deriv-approved definitions for all trade types, features, platforms, and markets. Last updated March 2026. Each entry includes: **Topic** (product area), **Definition** (source of truth for tooltip and helper text copy), and **EU availability** (Available / Not available in EU — apply as described in the "Before you write" section above). **Read this before writing copy that involves any product term.**

For formatting rules (dates, currency, abbreviations) and content-type constraints (email subject lines, push notification limits): refer to the Deriv Content Style skill.
