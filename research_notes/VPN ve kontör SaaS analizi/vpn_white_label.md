# White-Label / Reseller VPN Providers and Launching a Branded VPN SaaS (as of Nov 2026)

Research date: 2026-11-12. All figures in USD unless noted (Hetzner in EUR). "Confirmed" means stated on the vendor's own page at time of research; "third-party" means aggregator/blog; "estimate" means inference. Most sources in this space are vendor marketing, and several "independent" comparison pages are owned by a competing reseller (flagged below).

## 1. Which providers offer white-label / reseller VPN, what is included, and at what price?

### Takeaway
Only two providers publish concrete self-serve wholesale terms: **VPNresellers** ($1.99 per active account/month for 1-999, $0.99 from 1,000, down to $0.79; $0 setup; $39/mo optional branding; no contract) and, per third-party listings, **PureWL** (~$1.99 per active user, with a monthly minimum reported as $250 for SDK/API and $1,000 for the managed "Business-Ready" tier; PureWL's own page now says "custom quote"). **Windscribe** now has a white-label API (per-active-user, month-to-month, no published rate). Most other "reseller programs" are either affiliate-only (Surfshark, IPVanish) or unpublished-price wholesale. Realistic wholesale floor for a small founder: **~$1-2 per active user/month**.

### Cited Findings

**VPNresellers (vpnresellers.com) — most transparent public pricing (confirmed, vendor page, (c) 2026)**
- Wholesale per active account/month: $1.99 (1-999 accounts); $0.99 (1,000-24,999, rate applies to full base); further tiers down to $0.79 (250,000-499,999); 500,000+ custom. Intermediate tier rates not listed. — [VPNresellers cost page](https://www.vpnresellers.com/white-label-vpn-cost)
- $0 setup, $0 signup, $0 account minimum; billed daily on active accounts only from prepaid credit; $25 minimum top-up; no contracts. — [VPNresellers cost page](https://www.vpnresellers.com/white-label-vpn-cost)
- Custom branding (logo, app icon, brand colors): $39/month or $468/year paid upfront; requires $500 minimum credit balance; available on almost all platforms **except iOS**. — [VPNresellers cost page](https://www.vpnresellers.com/white-label-vpn-cost)
- Brandless "VPNclient" apps included free for Windows, macOS, iOS, Android, Linux, Android TV, Amazon Firestick. — [VPNresellers cost page](https://www.vpnresellers.com/white-label-vpn-cost)
- Network: 89 managed locations, 1 Gbps and 10 Gbps ports, up to 10 devices/account, no-logs, P2P allowed, full API. Protocols: OpenVPN (UDP/TCP), IKEv2, WireGuard, L2TP, PPTP, VLESS. — [VPNresellers cost page](https://www.vpnresellers.com/white-label-vpn-cost)
- Has a WHMCS module (API-key auth); third-party integrations exist (PayRequest, Blesta). A PayRequest guide confirmed the $1.99 / 1-999 tier "as checked on 3 October 2026". — [VPNresellers WHMCS](https://vpnresellers.pages.dev/whmcs-vpn-module); [PayRequest integration](https://payrequest.io/integrations/vpnresellers)
- Vendor's own ROI example: 250 accounts x $9.99 retail = ~$2,498 revenue, ~$498 wholesale, ~$2,000/mo profit, ~80% margin (excludes payment fees, churn, refunds, CAC). — [VPNresellers cost page](https://www.vpnresellers.com/white-label-vpn-cost)

**PureWL (PureVPN's white-label arm, purewl.com)**
- PureWL's pricing article (posted 9 Oct 2026, updated 24 Oct 2026) says pricing is **quoted per partner** based on delivery model, expected user base and platforms; no rate card. Product includes customized VPN apps, SDKs, web APIs, control panel, central billing; network described as KPMG-certified no-log. Example figures on that page ($2.00/active user, $1,000 monthly minimum) are explicitly hypothetical. — [PureWL pricing models](https://www.purewl.com/white-label-vpn-pricing/)
- Third-party/search-summary data: $250 monthly minimum + $1.99 per active user for SDK/API plan; $1,000 monthly minimum + $1.99/user for "Business-Ready" (fully managed branded apps). Not confirmed on PureWL's current site. — [WebSearch summary of PureWL pages, see PureWL VPNGN comparison](https://www.purewl.com/vpngn-alternatives/); [SaaSworthy PureWL pricing ($1.99/active user/mo)](https://www.saasworthy.com/product/purewl/pricing)
- PureWL case study: client used PureWL SDKs for Windows, Mac, Android and iOS. — [SaaSworthy PureWL](https://www.saasworthy.com/product/purewl)
- A competitor-owned listing says PureVPN Reseller has a monthly platform fee "starting at $99" and 65+ countries (unverified, competitor page). — [ResellVPN top 10 (owned by ResellPortal)](https://resellvpn.com/top-10-vpn-reseller-programs)

**Windscribe White-Label (windscribe.com/white-label-vpn) — confirmed, no public rate**
- API to create users, issue WireGuard/OpenVPN/IKEv2 configs, list servers, read per-user usage for billing, revoke access; includes R.O.B.E.R.T. DNS blocking and post-quantum encryption; SDKs and docs on signing. Windscribe can optionally build branded apps on its open-source clients. — [Windscribe white label](https://windscribe.com/white-label-vpn)
- Network: bare-metal servers in 69+ countries / 135+ cities, 10 Gbps in 85+ cities. — [Windscribe white label](https://windscribe.com/white-label-vpn)
- Billed per active user (users who connect that month), month-to-month, no annual contract, volume discounts; no per-user rate or setup fee published. API access immediate; typical integration ~2 weeks; custom app builds take longer. — [Windscribe white label](https://windscribe.com/white-label-vpn)

**VPNGN / VPNWholesaler**
- Per PureWL's (competitor) comparison: $250 monthly commitment, $1 per SDK user or $2 per monthly reseller renewal; pricing not published by VPNGN. — [PureWL VPNGN alternatives](https://www.purewl.com/vpngn-alternatives/)
- VPNWholesaler white-label access "open only to selected partners who proved that they can drive a good amount of daily sales and rebills." — [G2 VPNGN discussion](https://www.g2.com/products/vpngn/discuss)

**Others (less transparent)**
- ResellPortal: claims $0 platform fee, branded native apps Win/macOS/iOS/Android, 30+ locations, WireGuard/OpenVPN; its own blog posts conflict ($6/mo wholesale in one, $2/mo in an example elsewhere). Note: ResellVPN.com ranking pages are owned by ResellPortal LLC. — [ResellVPN top 10](https://resellvpn.com/top-10-vpn-reseller-programs); [ResellPortal resell VPN](https://resellportal.com/resell-vpn/)
- Golden Frog (VyprVPN) reseller program: desktop and mobile apps, API for billing/provisioning/support, dedicated account manager; no public prices. — [Golden Frog resellers](https://goldenfrog.com/resellers)
- SlickVPN: white-label reseller program with rebrandable Windows, Mac, mobile software. — [SlickVPN reseller](https://www.slickvpn.com/?p=1954)
- TorGuard reseller: wholesale rates (unpublished), semi-branded, API provisioning, Stealth/WireGuard; VPN.ac: volume license keys, manual distribution; JETVPN: customizable logo/colors; Ivacy, PrivateVPN: bulk/wholesale, no white label for PrivateVPN. All per a competitor-owned list; unverified. — [ResellVPN top 10](https://resellvpn.com/top-10-vpn-reseller-programs)
- Surfshark and IPVanish "partner" programs are affiliate-only (commission), not white label. — [ResellVPN top 10](https://resellvpn.com/top-10-vpn-reseller-programs)
- Billing platforms (HostBill, BillingServ/Upmind-type, Blesta, WHMCS) ship VPN-reseller modules, i.e., hosting companies/MSPs are a core buyer of these programs. — [HostBill VPN reseller](https://hostbillapp.com/feature/vpn-reseller/); [BillingServ blog](https://www.billingserv.com/blog/expand-your-offerings-introducing-our-whitelabel-vpn-service-for-resellers/)
- Vendor-authored market guide: "serious" white label VPN setup fees $1,000-$10,000, monthly base $500-$5,000, $1-$5 per active user (vendor guide, weigh accordingly). — [VPNCrafter guide](https://vpncrafter.com/best-white-label-vpn-service/)

### Inferences
- Three tiers emerge: (a) **self-serve reseller** (VPNresellers, ResellPortal): $0 upfront, ~$2/user, generic or lightly branded apps, launch in days; (b) **managed white label with fully branded apps in your own store accounts** (PureWL Business-Ready, Windscribe custom apps, VPNGN): monthly minimum ~$250-$1,000+ plus ~$1-2/user, launch in weeks; (c) **API/SDK-only** (Windscribe, PureWL SDK): you build/own apps, they run the network.
- Key limitation for a branded consumer product: VPNresellers' branding excludes iOS, so a true own-brand iOS app on that route means building your own WireGuard client against their API (feasible since they issue WireGuard configs) and publishing under your org developer account.
- "Per active user" definitions differ (connected that month vs provisioned vs per device); this materially affects cost when many annual subscribers go dormant. Windscribe bills only users who connect; VPNresellers bills "active accounts" daily (likely provisioned/enabled accounts — confirm).

### Gaps
- Could not find any public white-label/reseller program for **hide.me, StrongVPN, NordLayer, Surfshark (white label)** or "GoodVPN"; searches returned nothing. NordLayer is a B2B business VPN, not a white-label product (not verified this session).
- PureWL's current minimums ($250 / $1,000) are from search summaries/third-party, not the live PureWL site; PureWL now says "custom quote".
- Windscribe's wholesale rate unpublished; requires sales call.
- Did not research Outline, NetBird, Firezone, Headscale in this session. (Background, unverified here: these are open-source/self-hostable overlay or access tools aimed at teams/remote access; Outline is Shadowsocks-based and free; none is a turnkey consumer VPN business with billing/branded apps.)

## 2. Self-hosted alternative: servers, bandwidth, app development, store requirements

### Takeaway
Raw VPS cost for WireGuard nodes is small (~$4-6/node/month at Hetzner or DigitalOcean entry tiers) but location coverage, bandwidth on cheap clouds, IP reputation and especially **building and maintaining 4-5 native apps** dominate. Vendor estimate for building your own: $85k-$220k app/backend development and 6-12 months to first customer (vendor-biased upper bound). Apple requires VPN apps to come from an **organization** developer account and use NEVPNManager; Google Play requires a **VpnService declaration** with videos and in-app prominent disclosure.

### Cited Findings

**Hosting costs**
- Hetzner raised prices from 1 April 2026 (cloud ~+30-37% average) and again 15 June 2026 for new orders (moves of ~25% to 204% by type/location). — [Tom's Hardware](https://www.tomshardware.com/tech-industry/hetzner-to-raise-prices-by-up-to-37-percent-from-april-1); [WZ-IT June 2026](https://wz-it.com/en/blog/hetzner-price-increase-june-2026-cpx-ccx-alternatives/); [Findstack](https://findstack.com/resources/hetzner-price-increase-2026)
- Hetzner CX22 (2 vCPU / 4 GB) post-April price reported as ~€4.49/mo by one tracker and ~€3.79 by another (conflict, unresolved); CX23 reportedly moved from €2.99 to €5.49 and is unavailable to order. EU/US cloud plans include **20 TB/mo** outbound; overage ~€1-1.19/TB. — [Bitdoze](https://www.bitdoze.com/hetzner-cloud-cost-optimized-plans/); [agentdeals Hetzner 2026](https://agentdeals.dev/hetzner-pricing-2026)
- DigitalOcean cheapest Basic Droplet: $4/mo (1 vCPU, 512 MiB, 10 GiB SSD, **500 GiB** outbound transfer); 13 regions (SFO, Richmond, NYC, Kansas City, Atlanta, Memphis, Toronto, Amsterdam, London, Frankfurt, Bangalore, Singapore, Sydney). — [DigitalOcean droplet pricing](https://www.digitalocean.com/pricing/droplets)
- Vendor (VPNresellers) estimate for building own: servers $50-$200/server/month, 50+ locations $2,500-$10,000/mo; bandwidth $500-$5,000/mo; dedicated IP pool $100-$500/mo; minimum infra $3,100-$15,500/mo. Development: Windows $15-40k, macOS $15-35k, iOS $20-50k, Android $20-50k, backend/API $10-30k, website+billing $5-15k; total $85k-$220k; maintenance $5-20k/mo; 6-12 months to first customer. Example 500 customers: ~$18,000/mo (~$36/customer) vs ~$1,034/mo (~$2.07/customer) reselling. **Vendor has a strong incentive to inflate DIY cost.** — [VPNresellers build vs resell](https://www.vpnresellers.com/blog/vpn-reselling-vs-building-your-own-cost-comparison)

**App store requirements**
- Apple App Review Guideline **5.4 VPN Apps** (verbatim): "Apps offering VPN services must utilize the NEVPNManager API and may only be offered by developers enrolled as an organization. You must make a clear declaration of what user data will be collected and how it will be used on an app screen prior to any user action to purchase or otherwise use the service. Apps offering VPN services may not sell, use, or disclose to third parties any data for any purpose, and must commit to this in their privacy policy. VPN apps must not violate local laws, and if you choose to make your VPN app available in a territory that requires a VPN license, you must provide your license information in the App Review Notes field... Apps that do not comply with this guideline will be removed from the App Store and blocked from installing via alternative distribution and you may be removed from the Apple Developer Program." — [Apple App Review Guidelines](https://developer.apple.com/app-store/review/guidelines/)
- Google Play VpnService policy: only apps with VPN as core functionality (plus listed exceptions) may use VpnService; must submit Play Console declaration form; document VpnService use in listing; must encrypt device-to-tunnel traffic; provide a <=90-second video of the VPN in use plus a separate video of the prominent disclosure/consent flow; disclosure must be in-app; prohibited: undisclosed data collection, redirecting/manipulating other apps' traffic for monetization, ad manipulation; deceptive/undeclared use may cause suspension. — [Google Play VpnService policy](https://support.google.com/googleplay/android-developer/answer/12564964)

### Inferences
- Rough DIY infra for 30 locations at entry-tier VPS ($4-$10/node) is ~$120-$300/mo before bandwidth; but Hetzner covers only a handful of regions and DO 13, so 20-40 countries requires mixing providers (Vultr, Linode/Akamai, OVH, regional hosts) at higher per-node cost — a realistic small-scale estimate is ~$300-$1,000/mo for 25-40 nodes (estimate, not sourced). DO's 500 GiB cap is quickly exhausted by VPN users; Hetzner's 20 TB allowance is the outlier.
- With modern open-source WireGuard clients (official WireGuard apps are open source; Windscribe's clients are open source per its page) a lean single-codebase approach (e.g., Flutter/React Native wrapper over WireGuard tunnel libraries) could plausibly cost far less than the vendor's $85k-$220k, perhaps $20k-$60k for iOS+Android+desktop MVP — estimate, unsourced.
- The founder's existing eSIM business presumably already has an organization Apple developer account (required for 5.4), which removes one barrier; a separate VPN brand can be a separate app under the same org account.
- If launching in countries requiring VPN licenses (e.g., China, possibly others), Apple requires the license in review notes; simplest path is to exclude those storefronts.

### Gaps
- Vultr pricing page returned 403; Vultr/Linode/OVH per-node and bandwidth prices not collected.
- No independent (non-vendor) source for DIY app development cost.
- Official Hetzner price page not fetched; CX22 price conflict unresolved.

## 3. Unit economics: retail pricing, wholesale cost, margin, churn, refunds, CAC/affiliates

### Takeaway
Big brands sell 2-year plans at **~$2.29-$3.49/month effective** and monthly plans at **~$10-$16**. Wholesale at ~$1.99/active user leaves ~80% gross margin on monthly plans but very thin margin if a small brand tries to match long-term-plan pricing. Affiliates are the dominant acquisition channel, paying **~40% (Surfshark base) up to 100% of the first payment** (NordVPN monthly) plus ~30% recurring at Nord. Consumer subscription churn benchmarks are ~5-10%/month; VPN-specific data is weak.

### Cited Findings
- Retail 2-year effective pricing (2026): Surfshark ~$2.29-$2.49/mo; ExpressVPN ~$2.44-$2.99; Proton VPN ~$2.99; NordVPN Basic 2-year ~$3.49. Monthly plans: Proton ~$10; NordVPN/ExpressVPN ~$12.99-$14.99; Surfshark ~$15.45-$16.45. Renewal is often 2-3x first-term rate; NordVPN renews at $139.08/year (Toolradar). — [Cybernews cheap VPN](https://cybernews.com/best-vpn/best-cheap-vpn/); [Toolradar NordVPN](https://toolradar.com/tools/nordvpn/pricing); [Toolradar Proton](https://toolradar.com/tools/proton-vpn/pricing); [Windscribe VPN cost blog](https://windscribe.com/blog/vpn-cost/); [Costbench VPN 2026](https://costbench.com/stats/vpn-pricing-2026/)
- Resellers commonly charge $5-$12/month per user (ResellPortal-linked guide). — [ResellPortal resell VPN](https://resellportal.com/resell-vpn/)
- VPNresellers margin examples: $9.99 retail gives ~$8.00/customer margin at $1.99 wholesale, ~$9.00 at $0.99. — [VPNresellers cost page](https://www.vpnresellers.com/white-label-vpn-cost)
- Affiliate payouts: NordVPN reportedly up to 100% of first payment on monthly plans, ~40% on multi-year, 30% on renewals; Surfshark 40% base + performance bonuses ($100 min payout), one source claims 50%; sources conflict on recurring. All from affiliate blogs, not official terms pages. — [Authority Hacker](https://authorityhacker.com/vpn-affiliate-programs/); [LinkClicky 22 VPN affiliate programs](https://linkclicky.com/affiliate-programs/vpn/); [Referly Nord vs Surfshark](https://www.referly.so/affiliate-programs/compare/nordvpn-vs-surfshark)
- Churn: VPN reseller blog says VPN monthly churn ranges 5%-15%, target <5% (unsourced vendor claim). Consumer subscriptions broadly 5-10% monthly; Recurly-cited consumer category average 6.5%/mo vs 3.27% all-industry. — [VPNresellers churn blog](https://vpnresellers.pages.dev/blog/how-to-reduce-customer-churn-vpn-business); [Darkroom citing Recurly](https://www.darkroomagency.com/observatory/subscription-churn); [mean.ceo 2026 benchmarks](https://blog.mean.ceo/?p=10240)

### Inferences
- Illustrative unit economics (estimate): $9.99/mo retail, $1.99 wholesale, ~5% payment fees ($0.50) -> ~$7.50 contribution/user/mo (~75%). At 8% monthly churn, average lifetime ~12.5 months -> LTV ~$94 contribution. If paid via affiliate at 100% of first payment ($9.99), CAC is easily covered; but competitive affiliates prefer the big brands' high-EPC offers, so a new brand likely needs to offer above-market payouts (e.g., 100% first payment + recurring) to get placements.
- Annual plan at ~$49.99/yr (~$4.17/mo) still yields ~$2.18/mo gross over wholesale at $1.99 tier (~52%) before fees; matching big-brand 2-year prices (~$2.50/mo) would be roughly break-even on wholesale until the $0.99 tier (1,000+ actives). Per-connected-user billing (Windscribe) improves annual-plan economics since dormant annual subscribers cost nothing.
- Differentiation is the only viable lever against $2-3/mo incumbents: bundling with the founder's eSIM (travel VPN + data), travel-oriented pricing (weekly/7-day passes), or niche locales.
- App store purchases incur 15-30% Apple/Google commission (15% Small Business Program for <$1M) — background knowledge, not sourced this session; web checkout avoids it where permitted.

### Gaps
- No reliable VPN-specific refund or chargeback rate benchmark found.
- No sourced VPN CAC (paid search/social) figures found; affiliate rates are from affiliate blogs, not official program pages.
- No IndieHackers/Reddit founder revenue data collected in this session.

## 4. Market saturation and risks (payments, app stores, abuse, IP blocking)

### Takeaway
The consumer VPN market is saturated with heavily discounted incumbents ($2-3.50/mo on long plans) that dominate affiliate and review-site placements. Stripe's restricted list does **not** name VPNs, so a VPN subscription is not explicitly restricted there, but the list is non-exhaustive and country-specific. Main operational risks are app-store compliance, streaming-service IP blocking (Netflix blocks datacenter and even residential VPN IPs), and abuse complaints, which a white-label provider largely absorbs.

### Cited Findings
- Stripe's Prohibited and Restricted Businesses list does not mention VPNs, proxies, anonymizing services or IP masking (fetched Nov 2026). The list is "representative but not exhaustive", varies by country, and can change; restricted businesses may be supported with prior approval. — [Stripe restricted businesses](https://stripe.com/legal/restricted-businesses); [Stripe list FAQ](https://support.stripe.com/questions/prohibited-and-restricted-businesses-list-faqs?locale=en-GB)
- Apple: non-compliant VPN apps are removed and the developer may be removed from the Apple Developer Program; data may not be sold/used/disclosed to third parties. — [Apple guidelines 5.4](https://developer.apple.com/app-store/review/guidelines/)
- Google: deceptive/undeclared VpnService use may result in suspension; traffic redirection/ad manipulation for monetization banned. — [Google Play VpnService policy](https://support.google.com/googleplay/android-developer/answer/12564964)
- Netflix blocks IPs associated with commercial VPNs (since 2015) and in 2021 began blocking **residential** IPs used by VPNs (WeVPN first reported), with collateral damage to regular users. Reporting dated 2021; current 2026 state not confirmed. — [TechRadar](https://techradar.com/news/netflix-blocks-residential-ip-addresses-during-its-latest-vpn-crackdown); [TechSpot](https://www.techspot.com/news/90759-netflix-combats-vpn-region-bypassing-blocking-residential-ip.html); [Tom's Guide test](https://www.tomsguide.com/news/i-tried-using-five-vpns-to-unblock-netflix-and-its-not-good-news)
- VPNresellers allows P2P on its network (relevant to DMCA exposure; provider handles complaints at the network layer). — [VPNresellers cost page](https://www.vpnresellers.com/white-label-vpn-cost)

### Inferences
- A self-hosted VPN on Hetzner/DO IPs would be immediately flagged by streaming services and many sites (datacenter ASN); cheap clouds also act aggressively on abuse/DMCA complaints and may suspend accounts hosting a P2P-permitting VPN. White-label providers absorb this (their own ASNs/abuse handling) — a strong reason for a small founder to resell rather than self-host.
- Payment risk is more about chargebacks/fraud (VPN attracts card-testing and fraud from high-risk geos) and the reseller's MoR (Paddle etc.) policies than about Stripe category bans; Paddle policy unverified.
- Regulatory: VPN restrictions in some countries (China, Russia, UAE, Iran, Turkey-specific blocking of VPN sites/apps) — the founder (likely Turkey-adjacent given the folder name) should check local law; not researched here.

### Gaps
- Paddle / Lemon Squeezy VPN policy not found. (Stripe detail incl. US LLC verification is in section 6.)
- No 2026 data on streaming-unblocking success rates or on Turkish VPN regulation.

## 5. Step-by-step launch plan and timeline

### Takeaway
For a founder with existing web, payments and support, the fastest low-risk path is **white-label reseller first (days to ~4 weeks), own-brand apps later**. Windscribe cites ~2 weeks integration for API partners; VPNresellers claims launch in "a few hours" with $0 upfront; managed branded apps (PureWL/Windscribe custom) add weeks and a monthly minimum.

### Cited Findings
- Windscribe: API access immediate after signing; typical implementation ~2 weeks; custom app builds longer, scoped on first call. — [Windscribe white label](https://windscribe.com/white-label-vpn)
- VPNresellers: $0 upfront, time to market "a few hours", $25 minimum credit; branding needs $500 credit balance and $468/yr upfront. — [VPNresellers build vs resell](https://www.vpnresellers.com/blog/vpn-reselling-vs-building-your-own-cost-comparison); [VPNresellers cost page](https://www.vpnresellers.com/white-label-vpn-cost)
- DIY: 6-12 months before first customer (vendor estimate). — [VPNresellers build vs resell](https://www.vpnresellers.com/blog/vpn-reselling-vs-building-your-own-cost-comparison)
- PureWL recommends a pricing-model review and modeled quote before signing; negotiate minimum treatment, active-user definition, escalators, tier steps, true-up cadence. — [PureWL pricing models](https://www.purewl.com/white-label-vpn-pricing/)

### Inferences (proposed plan; estimates)
1. **Week 0-1: Positioning & vendor shortlist.** Niche angle (e.g., travel VPN bundled with eSIM). Request written quotes from Windscribe, PureWL, VPNresellers; confirm active-user definition, iOS branding, API features (provisioning, usage, revoke), SLA, abuse handling, data-processing terms.
2. **Week 1-2: MVP on VPNresellers** ($25-$500 credit) using its API + existing billing (WHMCS module or own Stripe integration); users install brandless VPNclient apps or WireGuard configs. Validate demand with existing eSIM customers.
3. **Week 2-6: Branding & legal.** Privacy policy committing to no data sale (Apple 5.4), no-logs alignment with provider, ToS/abuse policy, refund policy (30-day money-back is market norm — unsourced).
4. **Week 4-12: Own-brand apps.** Either managed branded apps (PureWL/Windscribe; ~$250-$1,000+/mo minimum) or build a WireGuard-based client against provider API. Submit iOS via org account (NEVPNManager, data declaration screen); Android VpnService declaration + 2 videos.
5. **Month 3+: Acquisition.** Cross-sell to eSIM base (cheapest CAC), launch affiliate program (40-100% first payment), SEO for travel/country-specific keywords.
6. **Month 6-12: Scale decision.** At 1,000+ actives, VPNresellers drops to $0.99; evaluate self-hosting select locations only once >several thousand users.
- Upfront cash estimate (reseller route, estimate): <$1k for MVP; ~$3k-$15k first year with managed branded apps (minimums) or own lightweight app build costs on top.

### Gaps
- No case studies/IndieHackers revenue reports of small white-label VPN brands were found in this session.

## 6. US LLC context (added on coordinator request): Stripe stance on VPN, Apple/Google developer accounts (D-U-N-S), provider onboarding of a non-US-owned US LLC

### Takeaway
Stripe does **not** list VPNs as prohibited or restricted (as of Nov 2026), so a VPN subscription is not categorically barred; the practical risk is fraud/dispute-driven freezes (VPN checkouts attract card-testing), and one VPN provider publicly reported a Stripe lock with EUR 2,000 withheld (2024). A US LLC can enroll in both Apple's and Google's developer programs as an **organization**, which requires a free **D-U-N-S number** (Google warns it can take up to 30 days) whose legal name/address must match; neither program states a nationality/ownership restriction. No white-label VPN provider publishes KYC rules for foreign-owned LLCs; self-serve resellers (VPNresellers) require only credit top-up, while managed programs (PureWL, Windscribe, VPNWholesaler) are sales-led and discretionary.

### Cited Findings

**Stripe**
- Stripe's Prohibited and Restricted Businesses list does not mention VPN, proxy, anonymizing or IP-masking services (fetched Nov 2026). The list is "representative but not exhaustive", country-specific, and changeable; restricted categories can be supported with explicit prior approval. — [Stripe restricted businesses](https://stripe.com/legal/restricted-businesses); [Stripe list FAQ](https://support.stripe.com/questions/prohibited-and-restricted-businesses-list-faqs?locale=en-GB)
- VPNHouse (a VPN provider) reported in June 2024 that after a surge of fraudulent transactions starting April 15, Stripe locked its account, a EUR 2,000 reserve top-up was never returned, and case reviews were closed within minutes; outcome unresolved at time of post. One company's account, not a verified pattern. — [DEV Community, VPNHouse (11 Jun 2024)](https://dev.to/vpn_house/our-frustrating-experience-with-stripe-withheld-2000-eur-and-no-support-for-2-months-ggp)
- AzireVPN moved from Stripe to Cleverbridge (May 2025) for reasons unrelated to Stripe policy (alignment with parent Malwarebytes, bookkeeping) — i.e., not evidence of Stripe hostility to VPNs. — [AzireVPN blog (26 May 2025)](https://blog.azirevpn.com/bye-stripe-hello-cleverbridge/)
- Stripe US verification: if the representative is not a US individual (no SSN/ITIN), Stripe expects a local non-US tax ID and documentation that the person is not a US taxpayer; owners provide SSN/ITIN last-4 where applicable; full 9-digit SSN/ITIN (or, for non-US resident owners, national ID/verification document) required at $500K lifetime payment volume. — [Stripe 2024 US verification FAQ](https://support.stripe.com/questions/2024-updates-to-us-verification-requirements-faq); [Stripe requirements for a US account](https://support.stripe.com/questions/requirements-for-having-a-us-stripe-account); [Stripe Business Rep/Owner Tax ID](https://support.stripe.com/questions/business-rep-owner-tax-id-requirements-for-us-companies)
- Third-party guides conflict: one says Stripe doesn't require an SSN for a non-US founder's US LLC; another says non-resident owners often stall at verification and should obtain an ITIN early. — [terms.law Stripe for foreign LLC](https://terms.law/Invest-USA/bank-compliance/stripe-for-foreign-llc.html); [Business Anywhere](https://businessanywhere.io/stripe-paypal-non-resident-us-llcs-what-to-know/)

**Apple Developer Program (organization)**
- Organization enrollment requires: a legal entity able to contract with Apple (no DBAs/trade names/branches; the legal entity name is shown as App Store seller); a **D-U-N-S Number** to verify identity, legal status and address; a public, functional website on a domain associated with the organization; a work email on that domain; Account Holder with legal binding authority (owner/founder/exec etc.); $99/year. The page states no nationality/ownership restriction. — [Apple enroll](https://developer.apple.com/programs/enroll/)
- Guideline 5.4 requires VPN apps to be offered only by developers enrolled as an organization (see section 2). — [Apple App Review Guidelines](https://developer.apple.com/app-store/review/guidelines/)

**Google Play (organization account)**
- Organizations must provide a D-U-N-S number ("You will not be able to create a developer account for an organization without one"); free from Dun & Bradstreet; "can take up to 30 days"; no exemptions/extensions; legal name and address in the Google payments profile must match the D&B profile; contact/developer email and phone verified by OTP; organization phone, website, contact name required. — [Google Play organization account requirements](https://support.google.com/googleplay/android-developer/answer/13628312)
- Google's VpnService policy page fetched did not state that VPN apps require an organization account (unlike Apple). — [Google Play VpnService policy](https://support.google.com/googleplay/android-developer/answer/12564964)

**White-label provider onboarding of a non-US-owned US LLC**
- No provider found publishing KYC/ownership rules for resellers. VPNresellers onboarding is self-serve with $0 signup and $25 minimum credit (no stated KYC). — [VPNresellers cost page](https://www.vpnresellers.com/white-label-vpn-cost)
- VPNWholesaler (VPNGN) limits white-label access to "selected partners who proved that they can drive a good amount of daily sales and rebills." — [G2 VPNGN](https://www.g2.com/products/vpngn/discuss)
- PureWL and Windscribe are quote/sales-call led (custom quote; "exact numbers come on the first call"). — [PureWL pricing](https://www.purewl.com/white-label-vpn-pricing/); [Windscribe white label](https://windscribe.com/white-label-vpn)
- Adjacent industry practice: proxy/network providers state reseller approval "is not automatic; commercial terms and KYC requirements depend on the proposed account", and list resellers as a KYC trigger. — [Databay reseller](https://databay.com/proxies/reseller); [Byteful KYC policy](https://documentation.byteful.com/general/kyc-policy)

### Inferences
- Since the founder already runs an eSIM SaaS on Stripe under the US LLC, the safest setup is a **separate Stripe account (or at minimum separate descriptor/product line)** for the VPN brand and explicit written confirmation from Stripe support that VPN subscriptions are acceptable — this protects the eSIM revenue if the VPN brand triggers fraud-driven review. Turn on Radar rules/3DS for high-risk geos and avoid cheap trial offers that attract card testers.
- If the eSIM app is already published on Apple/Google under the LLC's organization account, the D-U-N-S and organization verification are presumably already done; the VPN app can be published from the same account, though using the same account means a 5.4 violation could put the eSIM app's developer account at risk (Apple: "you may be removed from the Apple Developer Program"). A separate LLC/developer account is an option for risk isolation (cost/benefit judgment).
- White-label providers are generally non-US (PureVPN/PureWL is Hong Kong/BVI-linked; Windscribe is Canadian — background knowledge, not verified this session) and transact B2B on prepaid or invoiced terms, so a foreign-owned US LLC is unlikely to be a blocker; expect standard company docs (articles, EIN letter, owner ID) for sales-led programs.

### Gaps
- No official Stripe statement explicitly confirming or denying VPN subscription eligibility; recommend written confirmation from Stripe support.
- Paddle/Lemon Squeezy (MoR alternatives) VPN policies not verified.
- No provider-published KYC requirements for foreign-owned reseller entities; must be asked during sales calls.
