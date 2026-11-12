# Running a VPN business as a pure web SaaS, without building apps (as of Nov 2026)

Research date: 2026-11-12. Labels used: **[verified]** means read on the primary page. **[vendor claim]** means stated by the seller or vendor in marketing. **[seller-reported]** means from a marketplace listing. **[search snippet]** means seen only in a search summary, page not opened. **[estimate]** means my own reasoning, with no source.
Sibling notes (`vpn_build_models.md`) already cover wholesale pricing tiers, Flippa listings and the mobile-app "factory" model. This file covers the **app-free delivery** angle and repeats facts from them only where needed.

## Q1. Delivery models without own apps: pros, cons, examples

### Takeaway
There are three practical app-free models.
- **(a) Config/QR generation** for the official WireGuard/OpenVPN clients. This is the purest web SaaS. Indie examples exist (dzugg, AshVPN) but show weak traction.
- **(b) The wholesaler's own brandless apps.** VPNresellers ships "VPNclient" for 6 platforms. The customer gets credentials from your web dashboard.
- **(e) B2B dedicated/static-IP and team VPN.** The web dashboard is the natural product there, and prices are 3–10× consumer prices.

The other three are weaker or riskier. (c) VLESS/Shadowsocks keys work technically but carry the highest legal and abuse risk. (d) A browser extension is a mini-app, with store review and a proxy-only scope. (f) Reseller-to-hosting-company sales are a channel rather than a product.

### Cited Findings
**(a) Config / QR into official clients**
- dzugg (an Indie Hackers product) is a small WireGuard VPN that "generates standard config files and QR codes for official open-source clients". The founder says finding customers who trust the product is harder than building it. [search snippet; the IH page returned 403 on fetch] — [Indie Hackers: dzugg](https://www.indiehackers.com/product/dzugg-vpn)
- AshVPN has no custom app. Users "receive configuration profiles by email" and connect with official WireGuard clients, buying "one-off 28-day access with no automatic renewal". It launched in 2026 (about 5 months before this check). On Product Hunt it has 6 followers, 2 upvotes and no reviews, with no revenue disclosed. Provider and infrastructure are not named. [verified] — [Product Hunt: AshVPN](https://www.producthunt.com/products/ashvpn)
- UpVPN launched without a Windows app and got its first paying customers from a Show HN post. The founder says Reddit moderators blocked self-promotion. [search snippet] — [Indie Hackers: UpVPN](https://www.indiehackers.com/product/upvpn)
- Windscribe, a mainstream consumer VPN, runs a public web "config generator" for OpenVPN, IKEv2 and WireGuard. WireGuard configs are downloaded from the account page. Build-A-Plan users only get configs for the locations they paid for. This shows that config-from-dashboard is an accepted UX pattern even at large providers. [search snippet of Windscribe's own pages] — [Windscribe config generators](https://windscribe.com/features/config-generators); [Windscribe KB](https://windscribe.com/knowledge-base/articles/where-do-i-access-my-wireguard-configs)
- A user analysis on the Privacy Guides forum found that Windscribe WireGuard configs were generated server-side. The commenter saw no way to delete a generated config to revoke its key. This is a revocation and key-management issue that config-based SaaS has to solve. [forum, user analysis, dated] — [Privacy Guides forum](https://discuss.privacyguides.net/t/windscribe-vpn-service/21923?page=4)
- BeetVPN (Flippa #12206301) was a web-only subscription. It ran on AWS serverless and JavaScript with Stripe. Its third-party VPN cost was "$1 per active user monthly". It had MRR of $361, 115 active subscribers and 10% churn, and was asking $8,000 (listing ended around Jan 2026). [seller-reported; "Verified" badge = Stripe/GA connected] — [Flippa](https://flippa.com/12206301) (details in sibling `vpn_build_models.md`)

**(b) The wholesaler's brandless apps + credentials from your site**
- VPNresellers: "Standard brandless VPNclient apps included with every reseller account". Protocols by platform:
  - Windows and macOS: OpenVPN UDP/TCP, IKEv2, WireGuard, L2TP, PPTP, Stealth
  - iOS (App Store) and Android (Google Play): OpenVPN and WireGuard
  - Android TV and Fire TV Stick: OpenVPN and WireGuard

  That is **6 platforms, not 7**. Custom branding is "available as an add-on". [verified] — [VPNresellers apps](https://www.vpnresellers.com/apps)
- Each VPNresellers account "gets a unique username and password". Accounts can be created in four ways: dashboard, WHMCS, WooCommerce or REST API. You can set an expiry, suspend or delete an account. [verified] — [VPNresellers help](https://www.vpnresellers.com/help/account-management/how-to-create-vpn-accounts)
- Third-party billing portals built on VPNresellers (PayRequest, Blesta) let the end customer see the username, manage the password, pick a server and **download a WireGuard config, an OpenVPN profile or a VLESS link**. So VPNresellers supports both model (a) and model (b) from the same account. PayRequest's post is dated 2026-10-03. [verified on PayRequest; Blesta via search snippet] — [PayRequest blog](https://payrequest.io/blog/sell-vpn-subscriptions-without-whmcs); [PayRequest integration](https://payrequest.io/integrations/vpnresellers); [Blesta module](https://blesta.club/extensions/vpn_resellers)
- PayRequest warns: "a branded billing portal does not automatically make the VPN apps custom-branded." Portal login and VPN credentials are separate. [verified] — [PayRequest blog](https://payrequest.io/blog/sell-vpn-subscriptions-without-whmcs)
- **Windscribe White Label** advertises "fully branded apps for Windows, macOS, iOS, and Android" plus a "Custom API for instrumentation, data syncing and optional postbacks". The post is dated 2024-11-25 and mentions no generic apps, no config generation and no public pricing. [verified] — [Windscribe blog](https://windscribe.com/blog/windscribe-white-label-vpn/)
- **PureWL**: in its developer docs, your app calls the Web Service API with VPN credentials and PureWL builds the tunnel, after the account is created through the API. A PureVPN White Label guide (Jun 2026) says the API "returns a server endpoint, port, and pre-shared configuration parameters". It also says "kill switch logic lives primarily on the client SDK". I found no documented config-file-only or generic-app mode. [verified for the guide; developer docs via search snippet] — [PureVPN WL API architecture](https://www.purevpn.com/white-label/white-label-vpn-api-architecture/); [PureWL developer docs](https://www.purewl.com/developer/?p=9950)
- WLVPN (now VIPRE / Ziff Davis): its guide describes an OpenVPN config with a separate login.conf holding the username and password. Its help center sits behind an Okta SSO wall, so I could not fetch it. [search snippet] — [WLVPN guided setup](https://vipre.helpjuice.com/en_US/wlvpn/wlvpn-guided-setup)

**(c) VLESS / Shadowsocks / Outline keys via web or Telegram bot**
- VPNresellers offers "VLESS via API for custom applications". This makes key-style delivery possible on top of wholesale capacity, without running your own servers. [verified] — [VPNresellers home](https://www.vpnresellers.com/)
- The typical self-hosted pattern: a Telegram bot calls a Marzban or 3x-ui panel API, takes crypto payments and sends a subscription link. Open-source bots exist (e.g., Mirza Bot). The content comes mostly from a VPS vendor's blog, and **no verified revenue figures** were found. [vendor-adjacent] — [Valebyte blog](https://valebyte.com/en/blog/telegram-bot-for-vless-keys-on-your-vps/); [GitHub i4amed/bot](https://github.com/i4amed/bot)
- Legal precedent: a Chinese court convicted a defendant who sold Shadowsocks services to bypass the national firewall of "providing tools for intruding into or controlling computer systems". This is one jurisdiction only. [secondary, search snippet] — [China Digital Times](https://chinadigitaltimes.net/chinese/578242.html)
- A 2025 study of VPN apps found families sharing hard-coded Shadowsocks passwords, a sign of a low-quality ecosystem. — [OTF report (PDF)](https://www.opentech.fund/wp-content/uploads/2025/09/Linking-Suspicious-and-Insecure-Apps-in-the-VPN-Ecosystem.pdf)

**(e) B2B: dedicated/static IP, team VPN** (see Q4 for pricing)
- B2B products are dashboard-centric. GoodAccess charges per user plus a "dedicated gateway". NordLayer offers a dedicated IP server add-on. PureVPN Teams has per-user static IP whitelisting or a "Team Server" with 1 IP for up to 50 members. [search snippet] — [GoodAccess](https://www.goodaccess.com/lp/small-business-vpn-solution-for-teams); [ExpressVPN Teams](https://www.expressvpn.com/order/teams)
- WHMCS/WISECP modules from PUQ provision WireGuard VPN with a "client area: VPN client details, WireGuard config + QR". They run on your own MikroTik/WireGuard servers. [search snippet] — [WHMCS Marketplace: PUQ WireGuard](https://marketplace.whmcs.com/product/6679-puq-wireguard-vpn-provisioning-module); [PUQ Business VPN](https://marketplace.whmcs.com/product/6631-puq-business-vpn-provisioning-module)

**(f) Selling to hosting companies and IT providers**
- VPNresellers markets a "Best-rated WHMCS plugin" with "full lifecycle automation including provisioning, renewals and suspensions", plus WooCommerce and REST API. Hosting companies can add VPN as a product line. [verified, vendor claim on quality] — [VPNresellers](https://www.vpnresellers.com/)
- Time4VPS publishes an open-source VPN WHMCS module on GitHub. This shows hosting companies already sell VPN through WHMCS. — [github.com/time4vps/vpn-whmcs](https://github.com/time4vps/vpn-whmcs)

### Inferences
- **(a) Config/QR is the "purest" web SaaS but the weakest consumer funnel.** Every indie example found (dzugg, AshVPN, UpVPN) shows low traction, and the founders blame trust and distribution, not technology. It suits technical buyers (developers, router users, teams, Linux), not mass consumers.
- **(b) VPNresellers brandless apps is the best consumer compromise.** The customer installs "VPNclient" from the official store and logs in with credentials from your dashboard. You never touch app code. The downside is that the app name is not your brand, which can confuse buyers and weaken trust. Branded apps are an add-on, and per the sibling notes branding is not available on iOS.
- **(c) should be avoided by a Stripe-dependent founder with a US LLC and Turkish residency.** These keys are mainly bought in censorship markets (RU/IR/CN/TR). That clashes with the decision to avoid Turkish users, and with the high-risk-jurisdiction rules (see Q3).
- **(d) Browser extension** [estimate, no source]: a proxy-only Chrome/Firefox extension is far less work than native apps (roughly 1–3 weeks of JS), but it still means store review and maintenance, and it does not protect the whole device. It is a reasonable add-on later, not an MVP.
- **(e) B2B fits a web dashboard best.** Buyers expect configs, IP allowlisting and admin seats, and they pay $5–49+/mo per seat or gateway. Model (a) works there without friction.

### Gaps
- I found no conversion-rate data comparing config-file onboarding with one-tap app onboarding.
- I could not confirm whether VPNresellers' own reseller panel (not the third-party portals) gives end users WireGuard/OpenVPN config downloads, or whether the reseller must build that through the API. Its API docs were not fetched.
- I could not find any Windscribe or PureWL "generic/unbranded app" program. Both appear to be branded-apps/SDK only.
- Browser-extension VPN resale examples were not researched (time limit).

## Q2. Which wholesale providers support each model, and pricing

### Takeaway
VPNresellers is the only provider found with public pricing that supports app-free models (a), (b), (c) and (f) at once:
- (a) WireGuard/OpenVPN/VLESS artifacts via API or portals
- (b) brandless apps on 6 platforms
- (c) VLESS via API
- (f) WHMCS, WooCommerce and a REST API

It costs $1.99/active account/mo, falling to $0.99 at 1,000+, billed daily, with a $25 minimum top-up. Windscribe WL and PureWL are branded-app/SDK programs sold by sales call, so they do not fit the "no app" constraint.

### Cited Findings
- **VPNresellers**:
  - Pricing: "from $1.99 per active VPN account per month", $0.99 for 1,000–24,999, down to $0.79. Billed daily from credit, "No signup fees, no minimums, no contracts", top-ups from $25.
  - Network: 89 server locations with 1 and 10 Gbps ports.
  - Protocols: WireGuard, OpenVPN, IKEv2/IPsec, Stealth, VLESS, L2TP/IPsec and PPTP.
  - Integration: REST API, WHMCS plugin, and an MCP server that can "generate setup links".

  [verified, Nov 2026] — [VPNresellers](https://www.vpnresellers.com/); [VPNresellers apps](https://www.vpnresellers.com/apps)
- From the sibling note: custom branding is $39/mo, needs a $500 credit balance and is not available on iOS. The vendor's own example is 250 accounts at $9.99, giving $2,000 profit (80.1%). [vendor claim] — [VPNresellers cost page](https://www.vpnresellers.com/white-label-vpn-cost)
- **PayRequest**, a billing layer on VPNresellers API 4.1, charges "2% per successful payment, capped at €25". It is an alternative to WHMCS. The fictional example price is $7.99/mo. Its product rules: billing monthly or yearly only, no free trials, no quantity selection. [verified, 2026-10-03] — [PayRequest blog](https://payrequest.io/blog/sell-vpn-subscriptions-without-whmcs)
- **Windscribe WL**: branded apps for Windows, macOS, iOS and Android, plus an instrumentation/postback API. "No multi-year lock-ins". No public price. [verified, post dated 2024-11-25] — [Windscribe blog](https://windscribe.com/blog/windscribe-white-label-vpn/)
- **PureWL**: API + SDK model, with the tunnel and kill switch on the client SDK. From the sibling note, the lowest paid plan is about $250/mo (G2 snapshot 2026-05). [verified/aggregator] — [PureVPN WL](https://www.purevpn.com/white-label/white-label-vpn-api-architecture/); [G2](https://www.g2.com/products/purewl/pricing)
- **WLVPN (VIPRE)**: supports OpenVPN config + login.conf credentials and an SDK. Docs are behind SSO and pricing is not public. [search snippet] — [WLVPN guide](https://vipre.helpjuice.com/en_US/wlvpn/wlvpn-guided-setup)
- **Self-host via WHMCS modules** (PUQ): WireGuard config + QR in the WHMCS client area, on your own servers. [search snippet] — [WHMCS Marketplace](https://marketplace.whmcs.com/product/6679-puq-wireguard-vpn-provisioning-module)

### Inferences
- For a no-app founder, the shortlist is VPNresellers (wholesale, zero infrastructure) or self-hosted WireGuard plus a WHMCS/PUQ module (own VPS, own abuse handling). PureWL and Windscribe WL assume you ship apps.
- VPNGN was not researched in this pass. The sibling notes say it is sales-call priced.

### Gaps
- VPNresellers API endpoint list (config download, QR, server list) was not verified from the docs.
- VPNGN, Pango/Hydra and Windscribe WL per-user prices are not public.

## Q3. Stripe, chargebacks/fraud, and abuse (DMCA, torrent, spam): who handles what

### Takeaway
Stripe's restricted-business list (updated 2026-09-22) does **not** name VPNs or proxies, so a consumer/B2B VPN is not banned per se. Dealings with high-risk/sanctioned jurisdictions and "evasion of chargeback monitoring" are prohibited, though. With VPNresellers, **the reseller owns support, refunds, consumer law, and liability for end-user abuse it "should have known of"**. VPNresellers handles abuse complaints first at the individual account level.

### Cited Findings
- Stripe's restricted list does not mention VPN, proxy, anonymizer or circumvention. Its prohibited uses include "Evasion of card network chargeback monitoring programs" and using false or misleading identity information. Last updated 2026-09-22. [verified] — [Stripe restricted businesses](https://stripe.com/legal/restricted-businesses)
- The list also prohibits dealings, directly or indirectly, with high-risk jurisdictions and persons. [search snippet, third-party summary] — [ConductAtlas summary](https://conductatlas.com/platform/stripe/stripe-restricted-businesses-list/provision/CA-P-065433/dealings-with-high-risk-jurisdictions-prohibited/); [Stripe sanctions on Russia/Belarus](https://support.stripe.com/questions/sanctions-on-russia-and-belarus)
- VPNresellers Terms (last updated 2026-09-24):
  - VPNresellers "does not act as the merchant, retailer, or direct VPN provider to a Reseller's customers" (s.1).
  - "You are responsible for activity performed through VPN accounts that you create or manage" (s.5). The reseller is liable for violations it "knew or reasonably should have known of" and must indemnify VPNresellers (s.52).
  - Resellers own "customer support, complaint handling, billing, refunds, and consumer-law compliance" (s.4).
  - Resellers must check legality, including "local VPN restrictions" (s.32).
  - The terms have no DMCA procedure and do not name torrent/P2P. They prohibit systematic or commercial IP infringement and spam (s.23).
  - On abuse complaints, VPNresellers may contact the reseller or restrict a specific account (s.24). It will "attempt to address abuse affecting a specific End User account before restricting an entire Reseller Account" (s.5).
  - VPNresellers keeps no historical activity logs identifying end users (s.24).

  [verified] — [VPNresellers Terms](https://www.vpnresellers.com/terms)

### Inferences
- With wholesale, the reseller's abuse workflow is: receive a forward from VPNresellers, suspend that end user through the API, and refund or ban. Because nothing is logged, attribution happens only at account level. Selling one account per customer (no shared accounts) is therefore essential.
- Chargeback and fraud risk for VPNs is commonly described as elevated (card testing, stolen cards from anonymity-seekers). I found **no sourced data** on this. [estimate] Mitigations: Stripe Radar rules, 3DS, no free trials (PayRequest already disallows them), blocking sanctioned countries at checkout, and clear refund terms.
- Being Turkish-resident with a US LLC: geo-blocking TR at checkout plus Stripe country rules reduces both BTK exposure and Stripe risk. Note this is an inference, not legal advice.

### Gaps
- No Stripe-specific statement on VPN merchants' MCC/reserve treatment was found.
- No public VPN chargeback-rate benchmark was found.

## Q4. Real examples with revenue; B2B dedicated-IP pricing benchmarks

### Takeaway
Public revenue figures for web-only/config VPNs are tiny. BeetVPN had $361 MRR [seller-reported]. dzugg and AshVPN show no revenue and minimal traction. No verified Telegram-bot VPN P&L was found. B2B static-IP pricing is the strongest evidence of willingness to pay:
- Consumer dedicated-IP add-ons: $3.75–5.83/mo
- SMB team VPN: $7–10/user/mo
- Dedicated gateway/server: $39.99–49/mo

### Cited Findings
- BeetVPN: $361 MRR, $177 profit, 115 subscribers, $1/active-user wholesale cost, Stripe, AWS serverless. [seller-reported] — [Flippa](https://flippa.com/12206301)
- A Telegram-bot VPN with 8 paying users, from the sibling notes. [founder-reported] — see `vpn_build_models.md`
- Dedicated IP add-on prices (article dated 2026-04-28) [affiliate-style source]:
  - Surfshark: $3.75/mo
  - Private Internet Access: about $4/mo (the article's prose and cheat sheet are inconsistent)
  - CyberGhost: about $5/mo
  - NordVPN: about $70/yr, roughly $5.83/mo
  - TorGuard and PureVPN: bundled into the plan

  — [CM Alliance](https://www.cm-alliance.com/cybersecurity-blog/most-affordable-dedicated-ip-vpns-for-smbs-in-2026)
- Team/business VPN pricing [search snippets, vendor pages]:
  - GoodAccess: $7/user/mo (5-user minimum) + $49/mo per dedicated gateway
  - NordLayer: from $8/user/mo annual (5-user minimum), dedicated IP server from $40/mo
  - LimeVPN: $9.99/user/mo including a static IP
  - Proton VPN: dedicated server from $39.99/mo
  - Connectaserv: $290/mo for 50 seats
  - Windscribe: datacenter static IP about $2/mo (pooled)

  — [GoodAccess](https://www.goodaccess.com/lp/small-business-vpn-solution-for-teams); [LimeVPN](https://limevpn.com/vpn-for-business); [Connectaserv](https://connectaserv.com/vpn.html); [softcircles comparison](https://autodiscover.softcircles.com/blog/static-ip-vpn-providers-price-comparison-2026)

### Inferences
- An unbranded wholesale consumer VPN at $5–8/mo competes with Surfshark/Nord promotions of about $2–4/mo. A web-SaaS reseller cannot win on price. Niche positioning (static IP, teams, bundle) is required.

### Gaps
- No TrustMRR-verified web-only VPN found in this pass. The sibling note `bamboovpn.md` may cover one.
- No verified Telegram VLESS bot revenue numbers were found. No Flippa listing of a pure config-based VPN other than BeetVPN was found.

## Q5. Customer experience friction, support burden, MVP stack and running costs

### Takeaway
App-free onboarding adds friction in three places: installing a third-party client, importing a file or QR, and a mismatch between brand and app. The founders of config-only VPNs cite trust and acquisition as their main hurdle. No conversion data exists publicly. The leanest MVP is either a custom site plus provider API, or an off-the-shelf billing layer on the VPNresellers API.

### Cited Findings
- PayRequest's flow:
  1. Payment queues a VPN account.
  2. The customer goes to "My services → VPN" and picks a protocol and server.
  3. The customer downloads the config and imports it into a compatible client.

  The doc warns that WireGuard, OpenVPN and VLESS artifacts "have different client requirements". [verified] — [PayRequest blog](https://payrequest.io/blog/sell-vpn-subscriptions-without-whmcs)
- Portal login and VPN credentials are separate, so resetting one does not reset the other. That is a predictable source of support tickets. [verified] — [PayRequest blog](https://payrequest.io/blog/sell-vpn-subscriptions-without-whmcs)
- VPNresellers has a help article titled "My customer forgot their VPN password", which shows credential support is the reseller's job. [verified] — [VPNresellers help](https://www.vpnresellers.com/help/account-management/how-to-create-vpn-accounts)
- Saily (Nord Security's eSIM) bundles virtual location, ad block and web protection. NordVPN comes only with "Saily Ultra". Saily's own blog says the tools work only on Saily cellular data, not on public Wi-Fi. This is the closest eSIM+VPN-bundle competitor. [search snippets; conflicting third-party claims about "automatic VPN"] — [Saily blog](https://saily.com/blog/travel-vpn/); [TechRadar](https://techradar.com/pro/phone-communications/can-saily-become-more-than-just-an-esim-its-new-privacy-and-security-tools-suggest-so)

### Inferences (estimates, not sourced)
- **Stack option 1: fastest, about 1–3 days.** PayRequest (2% capped at €25) on VPNresellers API 4.1. The founder's Stripe account stays the payment provider. Running cost: about $1.99/active user plus 2% plus hosting.
- **Stack option 2: about 2–4 weeks for a solo dev.** Next.js or Laravel plus Stripe Billing webhooks driving the VPNresellers REST API (create, suspend, delete). Offer QR/config display or a deep-link to the VPNclient apps. The founder can reuse the eSIM SaaS codebase, auth and Stripe setup. Running cost: Vercel/VPS about $0–25/mo plus wholesale per user plus Stripe fees (about 2.9% + $0.30 US card; not sourced here).
- **Stack option 3:** WHMCS licence plus the VPNresellers WHMCS plugin. It suits model (f) and hosting-style buyers, but the UX is dated.
- **Friction reducers:** a QR shown on desktop for the phone, a one-click .conf download, per-OS illustrated guides, and links to official clients.
- **Niche positioning** for an existing eSIM business:
  - "eSIM + VPN" travel bundle: upsell at checkout, priced against Saily Ultra
  - Static/dedicated IP for remote workers, ad-account managers and agencies: priced at $8–15/mo against $3.75–5.83 consumer add-ons and $39–49 gateways
  - Expats needing a home-country IP (geo restrictions)

  All of these suit a dashboard plus config or VPNclient credentials.

### Gaps
- No published support-ticket rate or conversion benchmark for config-file VPNs.
- No VPNresellers dedicated/static IP product price was confirmed. That matters for the static-IP niche and needs checking on their pricing page or with sales.
- VPNresellers' allowed retail pricing and limits on multiple devices per account were not checked.
