# B2B APIs for reselling international airtime top-ups, data bundles and digital gift cards, and launching a branded product on them (as of Nov 2026)

Scope note: research done 2026-11-12 with about 19 web calls. Several provider sites (dingconnect.com, mobilerecharge.com help) returned HTTP 403 to the fetcher, so some provider details come only from search snippets. Most providers do not publish commission rates, minimum prefunds or KYB rules; those are marked as gaps. Labels used below: **[confirmed]** means stated in a cited primary or vendor source. **[estimate]** means my inference or background industry knowledge, not verified in this session.

---

## Providers: products, coverage, onboarding, pricing model, API quality, white-label options

### Takeaway
For airtime and data, the realistic self-serve options for a small founder are **Reloadly** (free sign-up, card/crypto funding, per-operator discounts automatically netted, widget and WordPress plugin) and **DingConnect** (free sign-up, wallet funding by card or PayPal, commission per product). **DT One** (formerly TransferTo) and **Prepay Nation/Valuetopup** suit a more B2B/contracted setup: you onboard through sales or ops before production keys. Gift-card "incentive" platforms (Tremendous, Tango, Runa, Xoxoday Plum) are built for B2B rewards and payouts, not consumer resale at a margin. For reselling gift cards to consumers, **Reloadly Gift Cards**, **Bitrefill Business API** and distributors such as EzPin and Prepay Nation fit better. None of them publish commission tables publicly; you only see rates after sign-up.

### Cited Findings

**Reloadly (airtime, data bundles, gift cards, utility payments, prepaid Visa/MC)**
- Usage-based, pay-as-you-go pricing: "No contracts, no hidden fees". Developer accounts are free, with free credits and full API access to start. **[confirmed]** — [Reloadly Pricing](https://www.reloadly.com/pricing)
- Under $200k sent there is free platform access. At $200k or more, sales offers bulk discounts. **[confirmed]** — [Reloadly Pricing](https://www.reloadly.com/pricing)
- Funding options: wire, ACH, credit card or crypto. **[confirmed]** — [Reloadly Pricing](https://www.reloadly.com/pricing)
- Airtime covers 800+ operators in 170+ countries, with a customizable widget and a WordPress plugin. Gift cards cover 300+ brands and 14,000+ products, with bulk orders in about 5 seconds. **[confirmed, vendor claim, 2026 page]** — [Reloadly Pricing](https://www.reloadly.com/pricing). A separate Reloadly page/deck claims "3,000 gift card brands", which conflicts with the 300+ figure (the deck is likely older or counts differently) — [Reloadly about/presentation via search](https://www.reloadly.com/about/)
- Commission model: the operator discount is your commission and is netted automatically. Example: a $10.00 top-up to Vodafone Spain at 3.5% gives $0.35 commission and a $9.65 wallet debit. Commission is not paid out separately. **[confirmed; rates are illustrative and change]** — [Reloadly Support: how users receive commission](https://support.reloadly.com/how-do-reloadly-users-receive-commission)
- New accounts start on default commissions. Accounts that can do more than $5,000/month in sales can request a special-pricing review for target countries. **[confirmed]** — [Reloadly Support: request special pricing](https://support.reloadly.com/how-to-request-special-pricing)
- A promotional (Black Friday) list showed operator discounts of about 1.5% to 13%. These were time-limited and the post date is unclear. **[confirmed but dated]** — [Reloadly blog](https://www.reloadly.com/blog/?p=1960)
- The API exposes commission per operator through an endpoint (`get commission by operator id`) and a Discounts API. **[confirmed]** — [Reloadly Node docs](https://reloadly-node-docs.vercel.app/airtime/commissions/get-commission-by-operator-id.html); [apis.io Reloadly Discounts API](https://apis.io/apis/reloadly/reloadly-discounts-api/)
- Reloadly's support center has articles titled "Which rate do you use to convert money from one currency to another?" and "Pricing Table". So FX conversion is applied when the sender and destination currencies differ, but no markup figure is public. **[confirmed that an FX rate applies; markup unknown]** — [Reloadly Support: Airtime Pricing](https://support.reloadly.com/airtime-pricing)

**DingConnect (B2B arm of Ding; airtime, data, some vouchers)**
- Model: sign up for free, fund a wallet, start selling. Funding is self-funding by credit/debit card or PayPal (where the currency is supported) or by bank transfer to Ding. **[confirmed via search snippet of FAQ; page 403 to fetcher]** — [DingConnect FAQ](https://www.dingconnect.com/Api/Faq); [DingConnect Portal](https://www.dingconnect.com/Api/Portal)
- Each product exposes a `CommissionRate` field ("the rate of commission that will be applied for selling this product"). The portal says you "earn commission from day one". **[confirmed]** — [DingConnect PHP SDK Product model](https://github.com/parenthesislab/dingconnect-api-php/blob/master/docs/Model/Product.md); [DingConnect Portal](https://www.dingconnect.com/Api/Portal)
- The distributor contract provides web login and/or API credentials. An account manager gives a commercial proposal, including any discount, before the effective date. Instant SKUs settle immediately; batch-mode SKUs stay "Submitted" until polled. **[confirmed via search snippet]** — [DingConnect API Description](https://www.dingconnect.com/Api/Description)
- Ding powers Western Union's top-up product, and WU markets it as fee-free. **[confirmed]** — [Western Union: Ding](https://www.westernunion.com/dk/en/ding.html); [WU blog](https://www.westernunion.com/blog/en/how-does-ding-top-up-work/)
- Integration contact listed in the FAQ: an integrations email at dingconnect. **[confirmed]** — [DingConnect FAQ](https://www.dingconnect.com/Api/Faq)

**DT One (DTone; legacy TransferTo airtime business)**
- DVS API (Digital Value Services). API access requires registering a DT Shop account and then generating key pairs for production and pre-production. **[confirmed]** — [DT One DVS API docs](https://dvs-api-doc.dtone.com/); [DT One developers overview](https://developers.dtone.com/reference/overview)
- Coverage: 160+ countries and 875+ mobile operators and billers. Products include airtime, data bundles and bills. **[confirmed, vendor claim]** — [Why DT One](https://www.dtone.com/why-dt-one)
- DT Shop is a no-integration self-service portal for retailers and agents to resell and earn commissions. **[confirmed]** — [DT One Retail Networks](https://www.dtone.com/who-we-serve/retail-networks)
- Official Java and Node API clients exist on GitHub. **[confirmed]** — [DT One GitHub](https://github.com/dtone)
- A third-party repo (Oct 2026) shows active DVS pre-production integrations. It advises validating sandbox failure handling before real payments. **[confirmed; third-party]** — [GitHub PR](https://github.com/musafirpiruz/pgnt-asian-backend/pull/4)

**Prepay Nation / Valuetopup (airtime "RTR", PINs, bill pay, gift cards, eSIM)**
- REST/JSON with HTTP Basic auth. Product types: Pin, Rtr (real-time recharge), Bill Pay, Gift Card, eSim. Gift-card SKUs come from a separate paginated catalog. **[confirmed]** — [Valuetopup developer FAQ](https://developers-valuetopup-39b.pages.dev/docs/faq)
- Onboarding: email ops to get sandbox credentials. All APIs must be tested in sandbox before production access is granted. Accounts can be prepaid (shown as a negative available balance) or credit (shown as amount owed). **[confirmed]** — [Valuetopup FAQ](https://developers-valuetopup-39b.pages.dev/docs/faq)
- Features: a Mobile Number Lookup API (operator detection), Range vs Fixed products, per-SKU exchange rates, and Check Status by correlation ID. A timeout does not mean failure, and a successful transaction is charged. **[confirmed]** — [Valuetopup FAQ](https://developers-valuetopup-39b.pages.dev/docs/faq)
- Notable: it **also sells eSIM SKUs**. This is relevant for an eSIM SaaS founder, as a possible single supplier for both brands. **[confirmed product type]** — [Valuetopup FAQ](https://developers-valuetopup-39b.pages.dev/docs/faq)

**Sochitel**
- A platform for prepaid voucher lifecycle and distribution of airtime, data, e-gift cards and bill payments. **[confirmed]** — [Sochitel services](https://www.sochitel.com/services). No public pricing or API detail was found.

**Bitrefill (Business API; gift cards, plus top-ups on its consumer site)**
- Business API for "platforms, resellers, and enterprise integrations". It offers the full catalog including test products, BRGC batches (Bitrefill gift card bulk issuance), deposits via API (crypto deposit invoices), webhooks and custom volume pricing. **[confirmed]** — [Bitrefill Business API docs](https://docs.bitrefill.com/docs/Common%20Use%20Cases)
- Onboarding is not self-serve: contact BD, describe the use case, and receive an API ID and secret (Basic auth, `api.bitrefill.com/v2`). An Affiliate API exists for referral partners. **[confirmed]** — [Bitrefill Business API docs](https://docs.bitrefill.com/docs/Common%20Use%20Cases); [Bitrefill Resell flow](https://docs.bitrefill.com/docs/integration-flow); [Bitrefill help](https://help.bitrefill.com/hc/en-us/articles/8576552808722-Can-I-integrate-Bitrefill-and-sell-gift-cards-directly-from-my-website-or-app)
- Funding is documented only as a crypto deposit. That suits crypto-native founders but adds treasury/FX steps for a fiat business. **[confirmed for the documented flow]** — [Bitrefill docs](https://docs.bitrefill.com/docs/Common%20Use%20Cases)

**Gift-card incentive platforms: Tremendous, Tango (BHN), Runa, Xoxoday Plum**
- Tremendous: no API, setup or subscription fees, and most rewards cost face value. There is a 3% fee when funding by credit card, and a reported 4-6% on cash-type payouts (PayPal/bank). **[confirmed for "free/face value"; 4-6% from a vendor-competitor blog]** — [Tremendous Gift Card API](https://www.tremendous.com/gift-card-api/); [DEV.to (author is Head of Growth at GIFQ, May 2026)](https://dev.to/dalia_gifq/picking-a-gift-card-payouts-api-in-2026-p9o)
- Tango Card (Blackhawk Network): the self-serve portal is free. Bulk/API contracts go through sales, and rates are unpublished. One source cites about 3% for enterprise volume. Its API is described as "mature but legacy". **[mixed: unverified figures]** — [DEV.to (GIFQ-affiliated)](https://dev.to/dalia_gifq/picking-a-gift-card-payouts-api-in-2026-p9o); [Phaze: Tremendous alternatives](https://www.phaze.io/resources/tremendous-alternatives/)
- Runa: a free starter tier with a monthly minimum spend and a reported $0.10 issuance per code, plus tiered FX spreads. **[unverified, review blog]** — [Phaze best gift card APIs 2026](https://www.phaze.io/resources/best-gift-card-apis-fintech-rewards-platforms/); [DEV.to](https://dev.to/dalia_gifq/picking-a-gift-card-payouts-api-in-2026-p9o)
- Xoxoday Plum: quote-based pricing (wallet discounts, or a platform fee plus per-transaction fees). A 3.5% credit-card funding fee is reported. **[unverified, review blog]** — [WiserReview Xoxoday alternatives 2026](https://wiserreview.com/blog/xoxoday-alternatives/)
- Caveat: all of these comparison pages are vendor-authored (GIFQ, Phaze, Zendit, Rewordin) and sometimes conflict. — [Zendit](https://zendit.io/best-gift-card-platform-for-business/); [Rewordin](https://www.rewordin.com/blog/best-gift-card-api-providers-2026)

**EzPin**
- Public material describes tools for brands to activate and redeem cards (mobile app, POS, API), with roles for Brand, Store and Distributor. No public reseller pricing or API program details were found. — [EzPin solutions (mirror)](https://ezpininc.pages.dev/solutions)

**Other aggregators surfaced (not researched in depth):** Zendit (airtime, data, gift cards, eSIM API), Giftbit, Giftronaut (claims 4,300+ products, 225 countries, 51 currencies; affiliated commenter), GIFQ, Phaze, Tillo, PrepaidIQ, Euronet epay. — [Zendit](https://zendit.io/best-gift-card-platform-for-business/); [DEV.to comments](https://dev.to/dalia_gifq/picking-a-gift-card-payouts-api-in-2026-p9o); [PrepaidIQ](https://api.prepaidiq.com/); [Euronet](https://www.euronet.com/?p=339)

### Inferences
- **[estimate]** CSQ/TransferTo: TransferTo's airtime business became DT One (rebrand around 2019), and TransferTo's payments side became Thunes. Treat "TransferTo" as DT One for airtime. "CSQ" could not be identified as a current independent airtime API brand in this session.
- **[estimate]** Incentive platforms (Tremendous, Tango, Runa, Plum) sell at roughly face value, so there is essentially **0% resale margin**. Their terms are oriented to rewards and payouts, and many brand agreements forbid resale to consumers. They are the wrong supplier for a consumer gift-card shop. Use Reloadly Gift Cards, Bitrefill Business, Prepay Nation, EzPin or another distributor with explicit resale rights, and confirm resale rights per brand in writing.
- **[estimate]** Ranking for this founder: (1) Reloadly, which is fastest to start with self-serve, card funding, widget and data bundles; (2) DingConnect, a strong second supplier and fallback for routing and redundancy; (3) DT One or Prepay Nation once volume justifies a contract. Prepay Nation also carries eSIM SKUs.
- **[estimate]** API quality: all four airtime APIs (Reloadly, Ding, DT One, Valuetopup) provide the core primitives: catalog/products, operator lookup by MSISDN, send top-up, status by external ID, and balance. Reloadly and DT One have public sandboxes and SDKs. Valuetopup's sandbox needs an email request.

### Gaps
- Published minimum prefund amounts: none found for Reloadly, Ding, DT One, Prepay Nation or Bitrefill. Reloadly and Ding appear to allow small self-funded card top-ups, but no minimum was confirmed.
- KYB document lists per provider: not published. Expect company registration, UBO ID, proof of address, website review and AML policy, but this is unverified.
- FX markup percentages for any provider: not published.
- Full per-operator commission tables: visible only after login.
- Dedicated white-label consumer apps: only Reloadly's widget and WP plugin, and DT Shop's agent portal, were confirmed. Fully white-label app offers were not found.
- No data was found for "CSQ" or EzPin pricing, and no Sochitel API docs.

---

## Typical margins and retail competitor consumer fees

### Takeaway
Wholesale airtime discounts are typically low single digits, with one confirmed example of 3.5% and promotional peaks around 1.5-13%. Margin is often thin unless you add a consumer service fee or FX spread, which is what retail brands do (MobileRecharge charges a percentage processing fee with a $1 minimum). Recharge.com and Ding.com build fees into the displayed price, so no clean public % was found.

### Cited Findings
- Reloadly example: 3.5% operator commission (Vodafone Spain, $10 gives $0.35). **[confirmed, illustrative]** — [Reloadly Support](https://support.reloadly.com/how-do-reloadly-users-receive-commission)
- Reloadly promotional operator discounts: about 1.5%-13% (Black Friday, dated). — [Reloadly blog](https://www.reloadly.com/blog/?p=1960)
- MobileRecharge.com charges a percentage-based processing fee on every transaction, with a $1 minimum. **[confirmed from search snippet of help page; % not visible]** — [MobileRecharge help: processing fee](https://argentina.mobilerecharge.com/help_center/why-is-there-a-processing-fee)
- Recharge.com says the displayed offer includes "all ... costs associated with buying the credit ... including additional costs, such as service costs". The fee is embedded in the price and positioned as an intermediary. **[confirmed]** — [Recharge.com how it works](https://www.recharge.com/en/it/how-it-works)
- Ding.com: there is no public per-transaction fee table. Ding notes the customer's bank may add a 1-3% currency-conversion fee. App reviews list "high fees" among complaints. Western Union's Ding-powered top-up is marketed as fee-free. — [Ding support: currency conversion fee](https://support-checkout-western-union.ding.com/hc/en-us/articles/33772818332433-Currency-Conversion-Fee); [WU Ding](https://www.westernunion.com/dk/en/ding.html); [mwm.ai app summary](https://mwm.ai/ko/apps/ding-top-up-mobile-recharge/425228767)
- Gift-card incentive platforms: about face value, plus 3-3.5% if funded by card (Tremendous, Plum). — [Tremendous](https://www.tremendous.com/gift-card-api/); [WiserReview](https://wiserreview.com/blog/xoxoday-alternatives/)

### Inferences
- **[estimate]** Typical wholesale airtime discounts: about 2-8% for most corridors. Large incumbent operators (e.g. big markets) often sit at the low end, around 1-4%, and smaller operators or promotions go higher. Data bundles are similar.
- **[estimate]** Gift-card distributor discounts to resellers: about 1-5% on big brands (Amazon, Apple, Google Play, Steam are often thin or nil), and about 5-15% on long-tail or regional brands, gaming and some retail.
- **[estimate]** Retail economics on a €10 top-up:
  - Wholesale 4% gives €0.40.
  - A consumer service fee of €0.49-€0.99 (or 3-8%) adds €0.49-€0.99.
  - FX spread 0-2% adds €0-0.20.
  - Gross is about €0.90-€1.60.
  - Less card processing (EU cards about 1.5% + €0.25 on Stripe-like pricing, so about €0.40) and a fraud/chargeback reserve (about 0.5-1.5% of GMV) leaves **net about €0.30-€1.00 per order (3-10% of GMV)**.
  - Small tickets (€5) are often break-even, so set a minimum order or a flat fee.
- **[estimate]** For gift cards resold at face value with a 3% discount, net after about 1.5-2.9% card fees and fraud is close to zero or negative. This is why consumer gift-card resellers need either deeper-discount brands, service fees, crypto payments (Bitrefill model) or loyalty programs.

### Gaps
- Exact current service fees of Ding.com, Recharge.com, MobileRecharge and Bitrefill: not retrievable (403s, or fees shown only at checkout). Do a manual checkout comparison for 3-4 corridors (e.g. DE to Turkcell, TR to MTN Syria/Afghan operators).
- No public per-operator commission benchmarks across providers.

---

## Fraud and chargebacks, and processor acceptance

### Takeaway
Gift cards and top-ups are instantly delivered, irreversible, liquid "cash-like" goods. That makes them a prime cash-out route for stolen cards, and they appear on Stripe's restricted list (stored value and gift cards, and especially third-party stored value). Expect Stripe review or refusal unless the model is pre-approved. Plan for strict 3DS, velocity limits, device/IP scoring and possibly a high-risk acquirer.

### Cited Findings
- Stripe's own blog lists "stored value or gift cards" among restricted categories that are "consistently troublesome" even when legal. **[confirmed]** — [Stripe blog: why some businesses aren't allowed](https://stripe.com/blog/why-some-businesses-arent-allowed)
- Stripe Restricted Businesses List (as quoted by a tracker, record dated 2026-05-20): restricts "preloaded payment cards, gift cards, virtual credits, or other products ... in which a monetary value is stored". A separate clause restricts sale of stored value or credits "maintained, accepted, and issued by anyone other than the seller", which is exactly the reseller model. **[confirmed via third-party tracker; verify on stripe.com/legal/restricted-businesses]** — [ConductAtlas: preloaded/gift cards](https://conductatlas.com/platform/stripe/stripe-restricted-businesses-list/provision/CA-P-065554/preloaded-payment-and-gift-cards-restricted/); [ConductAtlas: third-party stored value](https://conductatlas.com/platform/stripe/stripe-restricted-businesses-list/provision/CA-P-065552/third-party-stored-value-sales-restricted/); [Stripe restricted businesses](https://stripe.com/en-gi/legal/restricted-businesses)
- A merchant-side help article says Stripe caps gift-card values below $2,000 and prohibits open-ended value cards. **[unverified secondary]** — [Walla help](https://support.hellowalla.com/en/articles/9337332-important-stripe-terms-of-service-compliance-guidelines-for-gift-cards-and-services)
- 33% of merchants surveyed experienced card-testing fraud in 2025 (MRC data via Chargebacks911). **[confirmed secondary of MRC]** — [Chargebacks911 gift card fraud stats](https://chargebacks911.com/gift-card-fraud-statistics-financial-impact/)
- Gift-card chargebacks arrive about twice as fast as physical-goods chargebacks (Riskified). **[vendor data]** — [Riskified gift card fraud schemes](https://www.riskified.com/blog/gift-card-fraud-schemes/); [Fintech Times / Riskified](https://thefintechtimes.com/riskified-retail-payments-the-growing-threat-of-digital-gift-card-fraud/)
- Digital-goods dispute ratio is cited at about 1.2-2.0% **[weak source]**, versus an all-industry average of about 0.26% **[secondary]**. — [chargebackcost digital goods 2026](https://chargebackcost.pages.dev/digital-goods-chargeback-rate); [chargeback.io stats 2026](https://www.chargeback.io/ru/blog/chargeback-statistics)
- Velocity rule example: block any email/device/IP that makes more than 10 gift-card attempts in 5 minutes. Also key velocity to customer attributes (email, device, IP). — [chargeback.io gift card fraud](https://www.chargeback.io/de/blog/gift-card-fraud-chargeback); [chargeback.io automated fraud](https://www.chargeback.io/de/blog/automated-fraud)
- Reloadly bundles "fraud protection" with its platform for payouts customers. This does not cover your own card acceptance. — [Reloadly Pricing](https://www.reloadly.com/pricing)

### Inferences
- **[estimate]** Card networks' monitoring programs trigger at about 0.9-1% dispute ratio (Visa VAMP thresholds were tightened in 2025). An unprotected top-up/gift-card shop can exceed this within weeks of launch. Target fraud-loss below 0.3% of GMV.
- **[estimate]** Required control stack:
  - 3DS2 forced on all first purchases and on any gift card, which shifts liability for authenticated transactions in the EU/UK under SCA.
  - Stripe Radar custom rules, or Sift/SEON/Fingerprint for device and email/phone intel.
  - Velocity caps: new users about €25-50 per day and €100-150 per week. Raise limits with account age and successful history.
  - BIN/IP/country mismatch blocks, disposable-email blocks, and SMS OTP for account sign-in.
  - Delay gift-card delivery (minutes to hours) for new accounts. Top-ups cannot be delayed meaningfully, so cap them instead.
  - Allowlist recipient MSISDNs per account.
  - KYC (ID check) above thresholds, e.g. over €150/month, which also supports AML obligations.
- **[estimate]** Processor strategy: disclose the model to the existing eSIM Stripe account's risk team **before** launch, or use a separate entity/account so the eSIM business is not jeopardized by a termination (MATCH listing risk). Alternatives that commonly underwrite top-ups: Adyen or Checkout.com (need volume), Paysafe/Worldline/Nuvei, specialist high-risk acquirers (about 3-6% MDR plus a 5-10% rolling reserve for 90-180 days), PayPal (where accepted), SEPA/Open Banking (Trustly, TrueLayer, GoCardless instant pay; near-zero chargeback risk), local methods (iDEAL, Sofort/Klarna, Papara/Turkish cards via iyzico/PayTR for TR), and crypto (the Bitrefill model).
- **[estimate]** Keep the eSIM and top-up merchant accounts separate. This is a core risk-isolation recommendation.

### Gaps
- No primary-source fraud rate specific to international top-up merchants was found.
- Stripe's exact current wording should be read on the official page. The tracker quoted May 2026.

---

## Working capital: prefunding and cash cycle

### Takeaway
All airtime aggregators work on a prepaid wallet: you must hold float before you can sell. Credit lines (post-paid) exist but only on contract (Prepay Nation explicitly supports both prepaid and credit accounts). Cash is out before card settlement arrives, so float is roughly 3-10 days of GMV, plus any rolling reserve from a high-risk acquirer.

### Cited Findings
- Reloadly: you must deposit the fiat you want to sell. Funding is by wire, ACH, card or crypto, and the wallet is debited net of commission. — [Reloadly blog](https://www.reloadly.com/blog/?p=1960); [Reloadly Pricing](https://www.reloadly.com/pricing); [Reloadly Support](https://support.reloadly.com/how-do-reloadly-users-receive-commission)
- DingConnect: fund the wallet by card, PayPal or bank transfer before selling. — [DingConnect FAQ](https://www.dingconnect.com/Api/Faq)
- Prepay Nation: prepaid accounts (negative available balance) vs credit accounts (amount owed). — [Valuetopup FAQ](https://developers-valuetopup-39b.pages.dev/docs/faq)
- Bitrefill Business: balance funded by crypto deposit invoice. — [Bitrefill docs](https://docs.bitrefill.com/docs/Common%20Use%20Cases)
- Tremendous: funding the balance by credit card costs 3%. Plum reportedly charges 3.5%. — [Tremendous](https://www.tremendous.com/gift-card-api/); [WiserReview](https://wiserreview.com/blog/xoxoday-alternatives/)

### Inferences
- **[estimate]** At €30k/month GMV, keep €5-10k float with the primary supplier and €1-2k with the backup. Add the acquirer reserve (if high-risk at 10% for 180 days, about €18k locked by month 6). Total working capital is about €10-30k. Funding the wallet with a credit card (where allowed) eases cash flow but costs about 2-3%. Use bank wire or ACH/SEPA.
- **[estimate]** Implement low-balance alerts and auto-pause SKUs when the wallet is under a threshold. Run a daily reconciliation of the supplier ledger against your order ledger.

### Gaps
- No provider-stated minimum first deposit found.

---

## Tech build: components, time, cost

### Takeaway
For a founder who already has web, payments and support from the eSIM SaaS, an MVP top-up/gift-card storefront on one aggregator is about 4-8 weeks of one developer. Most of the hard parts are idempotency/timeouts, reconciliation and fraud, not the catalog.

### Cited Findings
- Core API primitives exist across providers:
  - catalog/products with Range vs Fixed denominations;
  - operator lookup by mobile number;
  - send top-up;
  - status check by your correlation ID (a timeout does not mean failure);
  - notifications of SKU changes;
  - per-SKU FX rate.
  — [Valuetopup FAQ](https://developers-valuetopup-39b.pages.dev/docs/faq); [DingConnect API Description](https://www.dingconnect.com/Api/Description); [DT One DVS docs](https://dvs-api-doc.dtone.com/)
- Ding batch-mode SKUs stay "Submitted" and must be polled. — [DingConnect API Description](https://www.dingconnect.com/Api/Description)
- Bitrefill provides webhooks for delivery notifications and test products. — [Bitrefill docs](https://docs.bitrefill.com/docs/Common%20Use%20Cases)
- Reloadly claims a gift-card reseller API can be integrated "in 1 day" and offers a no-code widget and WordPress plugin. **[vendor claim]** — [Reloadly blog: gift card reseller API](https://www.reloadly.com/blog/gift-card-reseller-api/); [Reloadly Pricing](https://www.reloadly.com/pricing)
- Official SDKs: DT One (Java, Node). Community SDKs exist for Reloadly (Node, Go, PHP) and Ding (PHP). — [DT One GitHub](https://github.com/dtone); [packagist reloadly](https://packagist.org/packages/tobexkee/reloadly); [Ding PHP SDK](https://github.com/parenthesislab/dingconnect-api-php)

### Inferences
- **[estimate]** Components and effort for one experienced developer:
  1. Catalog sync job (operators, products, FX, commission), plus a pricing engine to apply retail markup and fees per corridor: 4-6 days.
  2. Phone input with libphonenumber and operator auto-detect through the lookup API, with manual override: 2-3 days.
  3. Checkout reusing the existing payments stack, with 3DS forced: 2-4 days.
  4. Order state machine (pending payment, paid, submitted, success/failed/unknown) with idempotent external IDs, retries and status polling for timeouts: 4-6 days.
  5. Auto-refund to the payment method on supplier failure, and a manual review queue for "unknown": 2-3 days.
  6. Gift-card code delivery (email/account vault, with masked display and reveal-on-auth) plus a delayed-release rule: 3-4 days.
  7. Fraud layer (Radar rules or SEON, velocity tables, limits by account age, KYC hook such as Sumsub/Veriff/Onfido): 4-7 days.
  8. Admin and ops: wallet balance alerts, supplier reconciliation, margin reports, SKU kill-switch: 3-5 days.
  9. Multi-language SEO landing pages per country/operator (e.g. "Turkcell kontör yükle", "MTN Syria recharge"): 3-5 days with templating.
  10. Optional second supplier with failover routing: plus 4-6 days.
- **[estimate]** Total: about 30-45 developer-days for the MVP. At a €400-600/day freelance rate that is about €12-27k cash. If the founder builds it, the cost is mostly time.
- **[estimate]** Running costs:
  - hosting about €50-200/month;
  - fraud tool: SEON from about €0-500/month at low volume, Sift is enterprise-priced, Radar for Fraud Teams is about $0.02/screened transaction on top of standard pricing;
  - KYC about €1-2 per check;
  - SMS OTP about €0.03-0.08 each;
  - legal/T&Cs and AML policy €1-3k one-off;
  - an entity separate from the eSIM company €1-3k.
- **[estimate]** Shortcut: launch week 1 with the Reloadly widget/WordPress plugin to validate demand, then move to the full API.

### Gaps
- Provider uptime/SLA and webhook support for airtime (vs polling) were not verified for Reloadly and Ding in this session.

---

## Customer acquisition: diaspora, SEO, partnerships

### Takeaway
Top-up is a remittance-adjacent, corridor-specific business. Winners pick 2-5 corridors and dominate local-language search and community channels there. Incumbents (Ding through Western Union, Recharge.com, MobileRecharge) own generic keywords, so niche corridors and languages are the opening.

### Cited Findings
- Ding positions top-up as an alternative or complement to cash remittances and partners with Western Union for distribution. That shows remittance-corridor partnerships are a proven channel. — [Ding community: top-up vs remittances](https://www.ding.com/community/international-top-up-versus-cash-remittances); [WU Ding](https://www.westernunion.com/dk/en/ding.html); [DingConnect industries](https://blog.dingconnect.com/en/industries)
- Recharge.com runs thousands of country/locale-specific pages (/en/hn/, /en/bo/, /en/rw/ and so on). This is a programmatic local SEO strategy. — [Recharge.com locale pages](https://www.recharge.com/en/hn/how-it-works)
- DT One's "retail networks" model (agents and corner shops via DT Shop) shows offline diaspora shops are a distribution channel. — [DT One Retail Networks](https://www.dtone.com/who-we-serve/retail-networks)

### Inferences
- **[estimate]** Corridors to test:
  - DE/NL/AT/FR to TR (Turkcell, Vodafone TR, Türk Telekom).
  - TR to SY/AF/IR/IQ (Syrian, Afghan, Iranian and Iraqi populations in Turkey). Check sanctions: Syria and Iran operators may be restricted by suppliers and acquirers, and OFAC/EU sanctions apply. Afghanistan needs a check too.
  - EU/TR to Central Asia (Uzbekistan, Kyrgyzstan, Turkmenistan).
  - Foreign students in TR/DE topping up home numbers.
- **[estimate]** Channels:
  - Programmatic SEO pages per operator and country in the sender's language, e.g. Turkish/German for DE to TR, Arabic/Dari/Persian for TR outbound.
  - Facebook/Instagram/TikTok community groups and WhatsApp/Telegram broadcast.
  - Referral credit.
  - Cross-sell to existing eSIM customers (travellers can top up their home SIM or buy gift cards).
  - Ramadan/Bayram/New Year operator promos, since suppliers push promo bonuses.
  - Partnerships with student associations, diaspora shops, money-transfer agents and mosque/community centres.
- **[estimate]** Plan for a high repeat rate (diaspora users top up monthly). Saved numbers, scheduled top-ups and loyalty are retention levers.

### Gaps
- No sourced CAC benchmarks for top-up apps.
- No sourced corridor volume data (DE to TR top-up volume, TR to SY/AF).

---

## Step-by-step launch plan

### Takeaway
Validate corridors with a low-code widget, isolate risk in a separate entity and merchant account, and only then build the full API product with a fraud stack and second supplier.

### Cited Findings
- Self-serve free sign-up and sandbox: Reloadly and DingConnect. Sandbox by request: Prepay Nation (production only after sandbox validation). DT One requires a DT Shop account before API keys. Bitrefill is by BD contact. — [Reloadly Pricing](https://www.reloadly.com/pricing); [DingConnect SignUp](https://www.dingconnect.com/SignUp); [Valuetopup FAQ](https://developers-valuetopup-39b.pages.dev/docs/faq); [DT One DVS](https://dvs-api-doc.dtone.com/); [Bitrefill docs](https://docs.bitrefill.com/docs/Common%20Use%20Cases)
- Reloadly special pricing becomes available above $5k/month. — [Reloadly Support](https://support.reloadly.com/how-to-request-special-pricing)
- Stripe restricts gift cards and third-party stored value. — [Stripe blog](https://stripe.com/blog/why-some-businesses-arent-allowed); [ConductAtlas](https://conductatlas.com/platform/stripe/stripe-restricted-businesses-list/provision/CA-P-065552/third-party-stored-value-sales-restricted/)

### Inferences
- **[estimate]** Plan:
  1. **Weeks 0-1:** Pick 2-3 corridors. Do manual price checks on Ding.com, Recharge.com and MobileRecharge checkouts. Open Reloadly and DingConnect accounts and compare commissions per target operator.
  2. **Weeks 1-2:** Form or choose a separate entity. Get a legal review: in the EU, airtime resale is generally outside PSD2 under the electronic-communications exclusion, with limits. Gift cards may touch the e-money "limited network" exclusion. AML/sanctions screening is needed (no SY/IR operators unless cleared). Write T&Cs and a refund policy.
  3. **Weeks 1-3:** Payments. Apply to Stripe with a full disclosure (or get a written OK), and in parallel apply to a high-risk acquirer and an open-banking provider. Set up SEPA instant and PayPal. For TR-based senders, use a local PSP.
  4. **Weeks 2-6:** Build the MVP (components above) on one supplier with 3DS forced and conservative limits. Launch top-ups first. Gift cards come later because of higher fraud and thinner margin.
  5. **Weeks 6-8:** Soft launch to eSIM customers plus 1 diaspora community. Monitor fraud daily, with a dispute-rate kill-switch at about 0.5%.
  6. **Months 3-6:** Add SEO pages for 50-200 operator/country pairs, a referral program, a second supplier failover, then request special pricing (over $5k/month) and add gift cards from a distributor with explicit resale rights.
- **[estimate]** Illustrative unit economics at €30k GMV/month and a €15 average order (2,000 orders):
  - Net margin of 4-8% gives about €1.2-2.4k/month contribution before marketing.
  - The business becomes meaningful at about €150k+ GMV/month (about €6-12k contribution).
  - Unless fees and corridor pricing are optimized, this is a volume game with thin margins.

### Gaps
- Exact regulatory classification per country (DE BaFin, TR BDDK/MASAK) for gift-card resale was not researched here. It needs legal input.
- No primary data on launch timelines or outcomes from founder posts (Reddit/IndieHackers threads were not retrieved in this session).
