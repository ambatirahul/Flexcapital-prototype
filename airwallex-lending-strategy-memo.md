# Airwallex Lending: A Sequencing Strategy for Embedded and First-Party Credit
### Strategy memo — Staff Product Manager, Lending

*Note on scope: this is built from the job posting and public information only — no visibility into Airwallex's actual roadmap, risk appetite, or capital structure. The value here is the reasoning, not the specific numbers, which are directional.*

---

## The strategic question

Airwallex is building credit and lending capability across two distinct models — **embedded lending** (financing distributed through partner platforms) and **first-party lending** (credit products issued directly to Airwallex's own account holders). Both are on the table. The question a Staff PM needs to answer first isn't "which is better" — it's **which to prove out first, and why the sequencing itself is the strategy.**

## The bet: first-party before embedded

**Sequence first-party lending first**, using it as the proving ground for the underwriting and risk infrastructure that embedded lending will later depend on.

Reasoning:
- **First-party requires no external distribution deal to start.** Airwallex already owns the customer relationship and the transaction data (payments, payouts, account activity) needed to underwrite off live cash-flow signal rather than static credit history — the same logic behind an alternative-data eligibility model. That data access is immediate; a partner integration is not.
- **Embedded lending inherits first-party's risk models — not the reverse.** Whatever underwriting logic, pricing engine, and default-handling mechanics get built for first-party become the reusable core that gets embedded into partner platforms later. Building embedded first means building risk infrastructure and a partner integration simultaneously, with no proven baseline for either.
- **Compliance surface is smaller to start.** A first-party product in one or two markets is a contained regulatory scope. Embedded lending multiplies that scope by every partner platform's jurisdictional footprint. Prove the model where the compliance surface is smallest, then expand.
- **This mirrors how the two prototypes in this portfolio relate to each other**: a first-party working capital product (alternative-data eligibility, transparent pricing, revenue-share repayment with defined floors and an outside date) is the proving ground; a broader customer-facing forecasting and comparison layer is what that infrastructure could eventually power across both first-party and embedded surfaces once validated.

## Trade-offs this sequencing forces — and who needs to be in the room

| Trade-off | The tension | Who owns the call |
|---|---|---|
| Speed to market vs. balance-sheet exposure | Funding first-party advances off Airwallex's own balance sheet is fastest to launch but concentrates risk; a warehouse facility or forward-flow agreement with a capital partner is slower to stand up but de-risks scale | Finance/Treasury + Capital partners |
| Growth vs. portfolio quality | Loosening eligibility (thin-file, alternative-data) grows volume but needs default-rate discipline to avoid adverse selection | Credit Risk |
| Global consistency vs. market-specific modularity | A single global product is simpler to build; lending regulation is jurisdiction-specific by nature | Legal/Compliance, by market |
| Build vs. partner on underwriting | Building proprietary risk models is a durable asset but slow; partnering with an existing risk/data provider is faster but less differentiated | Risk + Data/ML, with Commercial input |

None of these are resolved in a memo — they're the decisions a Staff PM is expected to force to a conclusion with the right stakeholders, not decide alone.

## Indicative multi-quarter sequencing

| Horizon | Focus | Proof point |
|---|---|---|
| Q1–Q2 | First-party pilot, 1–2 markets, alternative-data underwriting on live transaction data, capped volume | Default rate and repayment behavior validated against risk appetite |
| Q3–Q4 | Automate underwriting at scale; move funding from balance sheet to a capital-partner structure (warehouse/forward-flow); expand to 2–3 additional markets | Cost of capital vs. yield spread proven at higher volume |
| Year 2 H1 | Launch embedded pilot with 1–2 platform partners in the lowest regulatory-complexity market, reusing the validated risk core | Embedded conversion and unit economics benchmarked against first-party |
| Year 2 H2 | Scale embedded across additional partners and markets; formalize a shared decisioning core so both surfaces draw on the same risk infrastructure with market-specific policy layered on top | Portfolio-level risk-adjusted return across both models |

## What "success" looks like at this level

Not feature adoption — portfolio-level and platform-level measures:
- Risk-adjusted portfolio yield (net of losses), not just origination volume
- Default/delinquency rate against a stated risk appetite, tracked as underwriting evolves from balance-sheet-funded to partner-funded
- Cost of capital vs. blended portfolio yield, as funding sources shift
- Time from pilot to reusable core: how much of the first-party risk/decisioning infrastructure is actually reused when embedded launches, not rebuilt
- Regulatory and market coverage achieved without a proportional increase in compliance headcount — a sign the "modular by market, centralized by capability" architecture is working

## Where this leaves the two prototypes

Neither is the strategy — they're proof-of-concept artifacts for pieces of it. The first-party working capital product demonstrates the underwriting and risk-safeguard thinking this sequencing depends on in Q1–Q2. The broader forecasting/comparison experience demonstrates what the customer-facing layer could look like once that infrastructure is proven and ready to scale — potentially across both first-party and embedded surfaces alike.
