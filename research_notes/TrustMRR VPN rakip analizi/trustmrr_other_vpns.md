# TrustMRR: other VPN, proxy, privacy and ad-block startups (beyond the 9 already known), as of 12 Nov 2026

Scope note (added after the user's update): the user will not build mobile apps and wants a web-delivered SaaS VPN. Web or SaaS-delivered listings (proxy-as-a-service, browser extensions, web dashboards) get the deeper teardowns. Mobile-only VPNs get revenue and a short sourcing verdict.

All TrustMRR figures come from each startup's public Markdown profile (`https://trustmrr.com/startup/{slug}.md`), fetched 12 Nov 2026. TrustMRR states that revenue, MRR and subscription numbers come from the payment provider's API, and that descriptions, pricing and insights are founder-supplied and unverified ([llms.txt](https://trustmrr.com/llms.txt)).

## Q1. How was the TrustMRR inventory searched, and how complete is it?

### Takeaway
Searching TrustMRR beyond slug-grepping turned up **5 new VPN-type or adjacent listings** and **1 VPN listing that has been removed**: VIPN/CHOP VPN, Stella Proxies, GeoSpoof, Nomoads, the stealth eSIM+VPN "ricardo" listing, and a probable identification of "VPN For Chrome". Still, there is **no way to do a complete keyword search of TrustMRR without an API key**, and about 450 anonymised "Stealth Company / Private Venture / Anonymous Startup" listings cannot be screened by name. Those listings are how the IPTV+VPN bundle and the B2C/B2B proxy company were hidden.

### Cited Findings
- TrustMRR says it lists "over 15,000 startups" and "over 3,000 startups for sale" ([llms.txt](https://trustmrr.com/llms.txt)). The sitemaps hold only 12,445 unique `/startup/` slugs (startup-sitemap.xml, sitemap-0.xml and sitemap-1.xml combined, fetched 12 Nov 2026), so about 2,500 or more listings are not in any sitemap. Example: VIPN was in search results but was never in the sitemap.
- The official API (`/api/v1/startups`, with filters for `category`, `onSale` and revenue ranges) requires a `tmrr_` Bearer key. Without one it returns `{"error":"Missing or invalid API key..."}` ([API docs](https://trustmrr.com/docs/api/list-startups)). The public `/api/ai/discovery` endpoint returns only fixed snapshots of 25 startups and has no search ([llms.txt](https://trustmrr.com/llms.txt)).
- TrustMRR's llms.txt says: "Do not scrape the website for full marketplace access … filtering and pagination require the authenticated API" ([llms.txt](https://trustmrr.com/llms.txt)). I started a bulk crawl of the startup page headers, then **stopped it after about 1,600 of 12,445 pages** to respect this rule. Recommendation: get a free TrustMRR account and API key, then run `GET /api/v1/startups?category=security|utilities|mobile-apps|productivity` across all pages. That is the only complete method.
- Category pages render only the **top 30** startups by revenue. `?page=2` and `?page=3` return the same 30, because more results load on the client side. Example: Security says "Discover 197 startups" but shows 30 ([category/security](https://trustmrr.com/category/security)). `/search?q=vpn` is also rendered on the client and returns no server-side results.
- What I tried, all on 12 Nov 2026:
  - Top-30 pages for the categories security, utilities, mobile-apps, productivity, travel, entertainment, developer-tools, saas, social-media, marketplace, games and community.
  - The `/recent` page (50 startups).
  - The tech pages `/tech/revenuecat`, `/tech/swift`, `/tech/kotlin` and `/tech/flutter` (30 each). `/tech/superwall`, `/tech/appstore` and `/tech/wireguard` return 404.
  - `/acquire`, which loads on the client side (0 server-side links).
  - A broad regex over the slug list (block, guard, privat, secur, shield, tunnel, dns, brows, ghost, spoof, fast, wifi and similar) and about 25 hand-checked `.md` profiles.
  - Web searches: "site:trustmrr.com VPN" (the site filter was ignored and no TrustMRR results came back), "trustmrr VPN app verified revenue", "\"trustmrr.com/startup\" vpn", ad-blocker / smart DNS / secure-browser variants, X/Twitter variants, and WireGuard / dedicated IP / business VPN variants.
  - Wayback CDX: the connection was reset, so it could not be used.
- Brand names suggested in the brief ("Tunnelly", "Shieldr"): **no such slugs exist** in the sitemap. The only "tunnel" slugs are clawtunnel (an AI-agent control plane) and papertunnel (online fax/mail), and neither is a VPN ([clawtunnel.md](https://trustmrr.com/startup/clawtunnel.md), [papertunnel.md](https://trustmrr.com/startup/papertunnel.md)).

### Inferences
- The highest-revenue VPN-type listings in the Security, Utilities and Mobile Apps top-30 lists are already known (BambooVPN, BlueVPN, the IPTV+VPN bundle). A VPN listing missing from those top-30s probably has 30-day revenue below the 30th-ranked startup in those categories. Exceptions are anonymised listings or listings filed under other categories.
- Stealth listings are the main remaining blind spot. Two of the nine known VPN or proxy listings were stealth listings found through search engines.

### Gaps
- I did not screen the ~450 stealth or anonymous listings, or the ~2,500 listings missing from the sitemap. This needs an authenticated API key.
- I found no TrustMRR listing for a web-dashboard, WireGuard-config, "team VPN", dedicated-IP or Smart DNS business, apart from the proxy businesses. The narrower searches returned no TrustMRR hits.

## Q2. Complete inventory of VPN-type listings found, with revenue (12 Nov 2026)

### Takeaway
On TrustMRR, the money in this space is in **B2B proxies** (HypeProxies, Stella Proxies, the stealth proxy reseller, Frontproxy) and in **mobile VPN subscriptions** (the IPTV+VPN bundle, BambooVPN, BlueVPN, VIPN). Web-delivered consumer VPNs are almost absent: the only one is VPN For Chrome, at about $12 a month.

### Cited Findings
"30d" is revenue over the last 30 days. "All-time" is total verified revenue. NEW marks a listing not in the brief's known list.

| # | Listing (slug) | Type / delivery | 30d revenue | MRR | All-time | Active subs | Processor | Founded / country | For sale | Source |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | HypeProxies (`hypeproxies`) | B2B ISP proxy, web dashboard | $239,377 | $0 | $12,010,864 | 0 | Stripe | 2019-10 / US | No | [md](https://trustmrr.com/startup/hypeproxies.md) |
| 2 | Stealth "B2C/B2B proxy company" (`b2c-b2b-proxy-company`) | Residential/ISP/mobile proxy reseller via "two tier-1 upstream providers" | $21,569 | $12,496 | $348,187 | 366 | Stripe | 2023-07 / – | $400,000 | [md](https://trustmrr.com/startup/b2c-b2b-proxy-company.md) |
| 3 | Stealth "IPTV Player & VPN bundle" (`iptv-player-vpn-app-bundle`) | Mobile/TV apps | $14,279 | $11,740 | $1,168,052 | 4,080 | RevenueCat | 2022-09 / US | $500,000 | [md](https://trustmrr.com/startup/iptv-player-vpn-app-bundle.md) |
| 4 | Frontproxy (`frontproxy`) | Unlimited residential proxy, flat monthly price | $9,061 | $9,861 | $77,774 | 6 | Stripe | 2019-11 / EE | No | [md](https://trustmrr.com/startup/frontproxy.md) |
| 5 | BambooVPN (`bamboovpn`) | Mobile VPN (also has a Chrome extension) | $6,458 | $9,798 | $179,017 | 1,490 | Superwall | 2025-09 / – | $800,000 | [md](https://trustmrr.com/startup/bamboovpn.md) |
| 6 | Visible Privacy (`visible-privacy`) | Privacy SaaS, €7–55/mo tiers | $2,705 | $1,811 | $35,979 | 78 | Stripe | 2024-08 / ES | No | [md](https://trustmrr.com/startup/visible-privacy.md) |
| 7 | BlueVPN (`bluevpn`) | iOS VPN ("Fast VPN Turbo IP Changer") | $2,162 | $2,321 | $72,857 | 248 | RevenueCat | – | No | [md](https://trustmrr.com/startup/bluevpn.md) |
| 8 | ProxyHunter (`proxyhunter`) | Per-GB proxy (DC $0.55, Resi $1.10, Mobile $2.40/GB) | $746 | $0 | $13,773 | 0 | Stripe | 2025-02 / TR | No | [md](https://trustmrr.com/startup/proxyhunter.md) |
| 9 | VPN For Chrome (`vpn-for-chrome`) | Chrome extension(s) | $11.56 | $0 | $21.86 | 0 | Dodo Payments | – / – (founder Thanh Bui, 822 X followers) | No | [md](https://trustmrr.com/startup/vpn-for-chrome.md) |
| 10 | **NEW** Stealth "ricardo" (`ricardo`) | Travel eSIM marketplace that also sells "VPN and etc" | $119,331 | $0 | $2,255,637 | 0 | Stripe | 2023-08 / CA | No | [md](https://trustmrr.com/startup/ricardo.md) |
| 11 | **NEW** GeoSpoof (`geospoof`) | Location/timezone/WebRTC spoofing extension plus iOS app (VPN complement) | $9,948 | $3,485 | $19,881 (available history) | 2,160 | App Store (direct) | 2026-05 / US | No | [md](https://trustmrr.com/startup/geospoof.md) |
| 12 | **NEW** Stella Proxies (`stella-proxies`) | B2B residential/ISP/sneaker/ticket proxy, web dashboard | $0 | $636 | $4,248,649 (12-month: $198,719) | 6 | Stripe | 2021-04 / US | No | [md](https://trustmrr.com/startup/stella-proxies.md) |
| 13 | **NEW** Nomoads (`nomoads`) | iOS/Android ad and tracker blocker using an on-device "local VPN" | $230 | $113 | $672 | 26 | RevenueCat | 2026-08 / – | $15,000 (5.4x) | [md](https://trustmrr.com/startup/nomoads.md) |
| 14 | **NEW, removed** VIPN: Secure Fast VPN, now "CHOP VPN" (`vipn-secure-fast-vpn`) | iOS/Android/Mac VPN with an AI assistant | not verifiable (page returns 404 today) | – | – | – | RevenueCat (per its privacy policy) | – | – | [vipn.io/privacy](https://vipn.io/privacy) |

- **VIPN on TrustMRR:** a web search on 12 Nov 2026 returned `trustmrr.com/startup/vipn-secure-fast-vpn?metric=mrr`, and the search tool's summary said it was RevenueCat-verified and "tracked since Apr 29, 2026", with about $77k 30d revenue, $92k MRR and $1.4M total ([search hit URL](https://trustmrr.com/startup/vipn-secure-fast-vpn?metric=mrr)). **I could not confirm these numbers.** The page and its `.md` both return 404 now, and Wayback was unreachable. Treat them as unverified; the summary may have mixed in numbers from other pages.
- **Adjacent listings checked and excluded:**
  - NullPrint: antidetect browser, $177 in 30d, $22,430 all-time, Stripe, GB ([md](https://trustmrr.com/startup/nullprint.md)). Relevant to proxy buyers, but not a VPN.
  - APXY: developer debugging proxy, $0 ([md](https://trustmrr.com/startup/apxy-modern-network-proxy-for-devs-ai-agents.md)).
  - GhostSim: virtual SMS numbers, $76.92 in 30d ([md](https://trustmrr.com/startup/ghostsim.md)).
  - SafeBrowz: phishing checker, $23 ([md](https://trustmrr.com/startup/safebrowz.md)).
  - Blurweb: screen-share blur tool, $239 ([md](https://trustmrr.com/startup/blurweb-app.md)).
  - SecureLint, CShield, VibeShield, ScamsShield: all $0, and none is a VPN.

### Inferences
- Among consumer VPNs on TrustMRR, all meaningful revenue is in mobile apps billed through app stores (RevenueCat or Superwall). Revenue for web-delivered offerings is concentrated in B2B proxies billed through Stripe.
- Stella Proxies shows how fragile the sneaker/ticket proxy niche is: $4.25M all-time, but $0 in the last 30 days and only $198.7k over 12 months.

### Gaps
- Founded date and country are blank on several profiles (BambooVPN country; BlueVPN; VPN For Chrome).
- I could not identify the real brand behind "ricardo". Its founder is Ricardo Pinho (3,914 X followers), and the listing claims about 1M users and plans "starting from $1.50".

## Q3. Teardowns of the newly found listings (web/SaaS ones first), with a sourcing verdict for each

### Takeaway
None of the new listings is a web-delivered consumer VPN of the kind the user wants to build. The closest web or SaaS models are: (a) **Stella Proxies**, a proxy sold through a web dashboard and resold from upstream pools; (b) **GeoSpoof**, a browser extension that complements a VPN and earns VPN affiliate revenue; (c) **VPN For Chrome / Oneproxy**, a free proxy-based Chrome extension. VIPN/CHOP is mobile-only and appears to run its own VPS fleet.

### Cited Findings

**A. Stella Proxies: B2B proxy-as-a-service, web dashboard (priority: web/SaaS)**
- Website: stellaproxies.com.
- Pricing: residential **$10/GB**, ISP **$1.35/proxy**, sneaker $1.35/proxy, ticket $1.80/proxy. The site also offers a free trial, "Servers", support over Discord, and claims of "Tier-1 ISP" IPs from "Sprint, CenturyLink, Comcast, Windstream, AT&T" ([stellaproxies.com](https://stellaproxies.com/)).
- Target users per TrustMRR: scraping, ad verification, social media management, SEO and botting ([md](https://trustmrr.com/startup/stella-proxies.md)).
- Delivery: customers get proxy credentials (host:port:user:pass) and use them in their own tools. There is no app and no VPN client.
- The site footer still says "© 2024 Stella Proxies LLC" ([stellaproxies.com](https://stellaproxies.com/)).
- The website is served from AWS Global Accelerator, AS16509 (IP 35.71.142.77, per ipinfo.io). This says nothing about where the proxy exit IPs come from.
- **Sourcing verdict:** wholesale plus markup. The residential pool is most likely resold from an upstream residential network, and the ISP IPs are leased from US carrier-announced ranges. **Inferred, medium confidence**: the per-GB residential pricing and the "Tier-1 ISP" language are typical of resellers, but I could not see the exit-IP ASNs.

**B. GeoSpoof: browser extension plus iOS app that complements a VPN (priority: extension)**
- Free extension for Chrome, Firefox, Edge, Brave and Safari, plus an iPhone/iPad/Mac app.
- Features: it spoofs `navigator.geolocation`, timezone (Date, Intl, Temporal) and WebRTC; "VPN sync" detects the VPN exit region and matches it; GeoSpoof GPS is a desktop companion that sets the iPhone's system GPS.
- Pricing: Pro "from $1.99/mo — or $24.99 lifetime".
- Company: GeoSpoof LLC, New York. It claims 50,000+ users ([geospoof.com](https://geospoof.com/)).
- The homepage banner is a **Proton VPN affiliate link** ("Black Friday: Proton VPN up to 75% off … Affiliate link") ([geospoof.com](https://geospoof.com/)).
- Revenue is verified directly from the App Store: $9,948 in 30d, +16.4% growth, MRR $3,485, 2,160 subscriptions, 84% profit margin ([md](https://trustmrr.com/startup/geospoof.md)).
- **Sourcing verdict:** no VPN infrastructure at all. It runs client-side on the user's device and earns extra money from VPN affiliate referrals. **Verified** from the website text.

**C. VPN For Chrome / extension.vn (re-fetched as requested)**
- TrustMRR profile:
  - Description: "We create Chrome extensions that help thousands of users work faster and stay productive."
  - Claims about 200,000 users; pricing listed as "Free".
  - Paid through Dodo Payments.
  - Revenue: $11.56 in 30d, $21.86 all-time, no subscriptions.
  - Domain Rating 12. Markets: Productivity, Utilities, Security.
  - ([md](https://trustmrr.com/startup/vpn-for-chrome.md); [page](https://trustmrr.com/startup/vpn-for-chrome)).
- extension.vn and proxy.extension.vn returned HTTP 502 on 12 Nov 2026. Both sit behind Cloudflare.
- A Chrome extension called "**Oneproxy – Free Vpn Proxy**" (ID bcgmniaoakfcmjbhcjpknnegmfddobla) has its privacy policy at extension.vn/privacy-policy.
  - About 5K users, version 1.0.0.7.
  - Features: "Powered by a global network of proxy servers", WebRTC leak protection, GPS spoofing, bypass list, and manual add of custom proxies.
  - ([chromeboard listing](https://chromeboard.com/extension/oneproxy-–-free-vpn-proxy-bcgmniaoakfcmjbhcjpknnegmfddobla)).
- **Inferred, medium confidence:** this is the "VPN" product behind the TrustMRR listing. The developer's name is not shown on the listing.
- **Sourcing verdict:** a browser proxy extension (chrome.proxy API with HTTP/SOCKS endpoints), not a full-device VPN. The proxy source is unknown; it could be resold proxies or free public proxies. **Low confidence.**
- Revenue is negligible, so this listing does not show that a web VPN can make money.

**D. "ricardo" stealth listing: travel eSIM marketplace with VPN add-on (web plus mobile)**
- Value proposition: "Affordable data in 200+ destinations … Plans starting from $1.50". Built with React, React Native and Next.js; Stripe; team of 11–25; bootstrapped; claims about 1M users.
- Revenue: $119,331 in 30d, $1,286,732 over 12 months, $2,255,637 all-time, MRR $0 (one-off purchases). Not for sale.
- ([md](https://trustmrr.com/startup/ricardo.md)).
- The VPN is a side product. The description names "esim, VPN and etc".
- **Sourcing verdict: unknown.** Bundling a white-label VPN with eSIM is a known pattern; PureWL markets an eSIM+VPN offering ([PureWL](https://www.purewl.com/?p=14003)). This is not verified for this company.

**E. VIPN / CHOP VPN: mobile-only, brief entry**
- App Store listing id6759218609, now titled "CHOP: Secure Fast VPN Proxy", seller Smart Soft Engineering LLC.
  - In-app purchases: $9.99/month and $69.99/year. The site shows $9.99/month plus a discounted annual plan with a 7-day trial.
  - Features: an AI assistant with voice and chat control, kill switch, AES-256, and a built-in browser.
  - 4.6★ from 93 ratings. Runs on iPhone, iPad, Mac and visionOS, plus a separate Android app.
  - ([App Store](https://apps.apple.com/app/id6759218609); [vipn.io](https://vipn.io/); [pricing](https://vipn.io/pricing)).
- Privacy policy details ([vipn.io/privacy](https://vipn.io/privacy)):
  - Retains "configuration allocation and download events, connection and disconnection timestamps, and associated server or configuration identifiers".
  - Third parties named: RevenueCat, Firebase, AppMetrica, Telegram (support), Cloudflare (speed test and protection), and **Yandex Ads and Google AdMob** (free tier with rewarded ads).
- Infrastructure: `api.vipn.io` resolves to 2.31.78.76, which is **Hetzner (AS24940), Falkenstein, DE** (ipinfo.io). crt.sh lists api2, dev, staging and railway-staging subdomains, but no per-server hostnames.
- The TrustMRR page is now 404.
- **Sourcing verdict:** own rented servers (VPS), most likely a self-hosted WireGuard/Xray-type config-allocation setup. **Inferred, low-to-medium confidence**: the API on Hetzner plus "configuration allocation" language point this way, but the exit IPs were not tested. The Yandex Ads and AppMetrica stack suggests a CIS-market focus (inferred).

**F. Nomoads: mobile-only, brief entry**
- On-device ad and tracker blocker for iOS and Android. It "uses a local VPN to filter DNS requests on your device", with 600K+ domains in its blocklists and per-app exclusions.
- Pricing: free Basic tier; Premium from $2.99/month.
- Privacy policy names only Google Firebase (opt-in analytics, Crashlytics).
- ([nomoads.com](https://nomoads.com/); [privacy](https://nomoads.com/privacy)).
- Listed for sale at $15,000 ([md](https://trustmrr.com/startup/nomoads.md)).
- **Sourcing verdict:** no servers; it is an on-device packet-tunnel DNS filter. **Verified** from its own documentation.

**Own app or generic client (WireGuard/OpenVPN)?**
- Stella Proxies: generic proxy credentials. Customers use their own tools; no app.
- VPN For Chrome / Oneproxy: its own Chrome extension.
- GeoSpoof: its own extension and app; no tunnel.
- VIPN/CHOP and Nomoads: their own native apps.
- None of the new listings offers downloadable WireGuard or OpenVPN config files.

### Inferences
- **For a web-based SaaS VPN, TrustMRR has no proven comparable.** The web-delivered revenue that exists is B2B proxy billed through Stripe: HypeProxies at $239k in 30d, the stealth reseller at $21.6k, and Frontproxy at $9k. Proxy-as-a-service is the nearest model with demonstrated revenue.
- GeoSpoof (about $10k in 30d from a free extension upsold to a $1.99/month app, plus VPN affiliate income) shows that an extension that complements a VPN can monetise without running any servers. That is a cheap entry point compatible with a web-first approach.
- The only consumer "VPN" extension listed (VPN For Chrome) earns about $12 a month. Free proxy-extension VPNs monetise poorly unless there is a paid tier.

### Gaps
- No exit-IP or ASN fingerprinting was done for Stella Proxies, Oneproxy or VIPN, because that requires purchasing or installing the product. The server-list match against VPNresellers, PureWL or Pango could not be done for any new listing.
- The extension.vn site was down (HTTP 502), so the full product line and pricing of VPN For Chrome could not be checked.
- I could not confirm whether any stealth listing hides a web-dashboard or WireGuard-config VPN SaaS. This needs authenticated API access.
