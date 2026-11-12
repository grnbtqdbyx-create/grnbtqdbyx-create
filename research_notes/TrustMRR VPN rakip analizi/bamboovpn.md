# BambooVPN: Competitor Teardown (as of 12 Nov 2026)

Method note: sources were the TrustMRR listing, bamboovpn.com (home, about, privacy, terms), the App Store listing, AppGoblin (third-party estimates), the Chrome Web Store, public DNS over HTTPS (dns.google), crt.sh, Verisign RDAP, and a **static** look inside the Android XAPK v2.18.0 (versionCode 371). The XAPK came from the APKPure CDN, `https://d.apkpure.net/b/APK/free.vpn.unblock.proxy.bamboovpn?version=latest`, sha256 `556dc4b231e7ef06e8a9ac91abe22c8260f0e9532ba46f5918ad4e036fd1f042`. I only unzipped it and ran `strings`/grep. Nothing was executed. I did not query the app's backend API: an attempt to make unauthenticated GETs to bk.bamboovpn.com was blocked by the session's permission policy. "Verified" below means it was observed directly in a source. "Inference" means my reasoning.

## 1. TrustMRR listing: revenue, sales, founder, sale status

### Takeaway
TrustMRR, re-checked on 12 Nov 2026, still shows $6,807 revenue in the last 30 days, $9,798 MRR, 1,490 active subscriptions and $179,017 all-time. The founder is "Jim Løining" (X slug `jimleevi`). He says he **acquired and rebuilt** an existing app rather than founding it. The Superwall data feed is stale: the API key expired and data was last updated 10 Nov 2026. No $800,000 asking price, and no 70% margin figure, was visible on this fetch.

### Cited Findings
- Revenue: "$6,807 in the last 30 days". MRR $9,798. All-time $179,017. Active subscriptions 1,490. Rank #473 on TrustMRR — [TrustMRR](https://trustmrr.com/startup/bamboovpn)
- Founded "September 2025". Categories: Mobile Apps / Security / Utilities. B2C, ~500,000 users. Domain Rating 16/100 — [TrustMRR](https://trustmrr.com/startup/bamboovpn)
- Pricing on the listing: Weekly $3.99, Yearly $51.99 — [TrustMRR](https://trustmrr.com/startup/bamboovpn)
- Tech stack shown: Superwall. The page also shows the notice "Superwall API key expired. Data last updated Nov 10, 2026." — [TrustMRR](https://trustmrr.com/startup/bamboovpn)
- Founder: Jim Løining, 𝕏 slug "jimleevi", 108 followers. No country is listed — [TrustMRR](https://trustmrr.com/startup/bamboovpn)
- Founder notes, paraphrased:
  - "Acquired and rebuilt this 6 months ago."
  - "Growth has been consistent and 100% organic."
  - Spends under 2 hours a week on it.
  - A developer can stay on after a sale.
  - "iOS - 80% revenue Playstore - 20% revenue."
  - macOS, Windows and Chrome versions are built but described as not yet released.
  - Untapped levers: email marketing, paid ads, upsells.
  - Reason for selling: "Selling because I'm out of time, not out of belief, too many other projects."
  — [TrustMRR](https://trustmrr.com/startup/bamboovpn)
- On this fetch the page showed **no asking price/multiple ($800k not found) and no profit-margin figure**. Both had been recorded in earlier research — [TrustMRR](https://trustmrr.com/startup/bamboovpn)
- No revenue chart data points or traffic figures could be extracted (the chart is not available as text) — [TrustMRR](https://trustmrr.com/startup/bamboovpn)

### Inferences
- "Founded Sept 2025" is almost certainly the **acquisition date**, not product inception. The Android app was released 2021-10-18 and iOS 2022-04-20 (see §3). The iOS version history also shows a gap from v2.4.9 (Jan 2025) to v2.4.12 (25 Sep 2025), and the site's privacy policy and terms are dated 3 Oct 2025. Both fit a hand-over in Sept 2025.
- The $800k ask and the 70% margin may have been edited out, or may sit in a part of the page my fetch did not render. Treat them as "previously reported, not re-confirmed on 12 Nov 2026".
- $800k ÷ ($9,798 × 12) ≈ 6.8× ARR. That is high for a sub-$10k MRR consumer VPN, especially with founder-reported 80% iOS concentration.
- The MRR ($9.8k) is well above 30-day revenue ($6.8k). That gap is consistent with annual plans being normalized monthly, and/or with revenue reported before or after store fees.

### Gaps
- Revenue trend chart, monthly series, churn, trial conversion: not machine-readable.
- Founder's country and real identity are not confirmed. The searches "Jim Løining" and "jimleevi" returned nothing relevant ([search](https://trustmrr.com/startup/bamboovpn) cross-check failed). No X, Reddit or IndieHackers posts from him were found.

## 2. Product: features, servers, platforms, pricing, legal entity

### Takeaway
BambooVPN is a Flutter one-tap VPN sold under the US shell entity **Viral Apps LLC** (Sheridan, WY registered-agent address). It offers WireGuard (added Jun 2026) with OpenVPN fallback, and claims "50+ locations". Premium features include Secure Core multi-hop, dedicated IPs, an ad/tracker-blocking "BambooShield", a kill switch and split tunneling. The free tier is ad-supported and the paid tier uses weekly and annual subscriptions. No VPN infrastructure partner is named anywhere.

### Cited Findings
- Website features:
  - One-tap connect, zero-log claim, streaming/gaming/social "special servers", unlimited bandwidth.
  - "50+ global server locations". Named or flagged: USA (Dallas), Russia, France, China, Australia, Mexico, Canada, Japan, UK, Turkey, India, UAE, Singapore, Brazil.
  - Platforms: Windows (Setup 2.1.0 direct download), macOS (Mac App Store), iOS, Android, Chrome.
  - Pricing: $4.99/week or $51.99/year ("$0.99/week, Save 80%").
  — [bamboovpn.com](https://bamboovpn.com)
- About page: "Viral Apps LLC makes BambooVPN", launched on the App Store in 2022. It lists WireGuard and OpenVPN, plus Secure Core multi-hop as a Pro feature. It does not say who owns the servers — [About](https://bamboovpn.com/about)
- Legal entity: **Viral Apps LLC, 1309 Coffeen Avenue STE 1200, Sheridan, WY 82801, USA**, phone +1 (573) 207-3684.
  - The privacy policy names no third-party processors, SDKs or hosting/VPN providers. It refers only to generic "trusted third-party service providers".
  - It claims no logging of IPs, timestamps, DNS queries or traffic. Last update Oct 3, 2025.
  — [Privacy Policy](https://bamboovpn.com/legal/privacy-policy)
- Terms: governed by **California** law (the address is in Wyoming). Billing goes through the app stores. No VPN network provider is named. Last update Oct 3, 2025 — [Terms](https://bamboovpn.com/legal/terms-and-conditions)
- App Store description: WireGuard (introduced in v2.10.00) with OpenVPN fallback. Free servers to start. Countries listed: US, UK, AU, CA, ES, IN, BR, EE, FI, IT, JP, NL, PL, SA, SE — [App Store](https://apps.apple.com/us/app/id1617533959)
- In-app feature strings found in the APK (static strings in libapp.so):
  - "Secure Core" routes, including "This Secure Core route is at capacity".
  - "BambooShield works on premium servers". It blocks banner and video ads.
  - "Kill Switch", "Auto-reconnect kill switch", "Split Tunneling".
  - Dedicated IP ("A dedicated IP address is a unique internet protocol address assigned exclusively to you"), linked to `https://myaccount.bamboovpn.com/dashboard/dedicated-ip`.
  - "WireGuard & OpenVPN protocols".
  — Static analysis of APK v2.18.0 (source: APKPure CDN, link above)
- The APK contains `StripeStoreIdentifiers`/"STRIPE" strings (RevenueCat's Stripe web-billing support) and a `usdt_text.svg` image asset — static analysis

### Inferences
- The free tier is ad-supported: Google Mobile Ads/AdMob is bundled, and the App Store age rating says "contains advertising". The paid tier is Superwall-paywalled.
- Stripe/USDT hints, together with the myaccount.bamboovpn.com dashboard, suggest web or off-store payments for desktop, extension or dedicated IPs. This is unconfirmed.
- The location claims are inconsistent across surfaces: the App Store lists 15 countries, the website says "50+", and the flags include China and Russia. The real list is served from the backend (see §4) and could not be retrieved.

### Gaps
- Full server/location list and server count: served dynamically from `bk.bamboovpn.com/api/servers`, not retrieved.
- Free-trial terms and refund FAQ answers are not rendered on the site.
- Dedicated IP pricing was not found.

## 3. App Store / Google Play / Chrome listings and developer footprint

### Takeaway
On Android (`free.vpn.unblock.proxy.bamboovpn`, publisher Viral Apps LLC) the app has about 824K installs and 4.2★ from 7.3K ratings. iOS (id1617533959) is small by rating count: 137–251 ratings at about 4.5★. The iOS developer account "interactiveecommercellc" also publishes a calorie tracker and a knitting app, which looks like a small app-portfolio owner. The Chrome extension publisher is Interactive Apps LLC at the same Sheridan WY address, with contact email per@markusakerlund.com.

### Cited Findings
- **iOS listing:**
  - "Bamboo VPN : Speedy & Private", subtitle "Fast, Unlimited & Secure VPN".
  - Developer "interactiveecommercellc", seller Viral Apps LLC, © 2025 Viral Apps LLC.
  - 4.5★ from 137 ratings, version 2.16.01 (Oct 2), 115.8 MB, 19 languages.
  - Also runs on Mac (macOS 12+) and visionOS.
  — [App Store](https://apps.apple.com/us/app/id1617533959)
- **iOS IAPs:**
  - Premium Weekly $4.99 (×2) and $3.99.
  - Premium Annual $45.99 (×2) and $51.99.
  - One Month $3.99; "Pro – Monthly (Trial)" $12.99; 1 Year $22.99; 3 month $8.99.
  - Many SKUs suggest legacy plus A/B-tested price points.
  — [App Store](https://apps.apple.com/us/app/id1617533959)
- **iOS version history:**
  - 2.2.7 (Mar 2023) … 2.4.9 (01/10/2025), then 2.4.12 (09/25/2025).
  - 2.4.14 (11/22/2025), 2.4.15 (12/14/2025), 2.4.16 (Jan 14), 2.8.00 (Feb 17), 2.10.00 (Jun 8), 2.12.00 (Jul 6), 2.16.01 (Oct 2).
  — [App Store](https://apps.apple.com/us/app/id1617533959)
- **iOS privacy labels:** data used to track: Contact Info, Identifiers, Usage Data. Purposes include third-party advertising — [App Store](https://apps.apple.com/us/app/id1617533959)
- Other iOS apps by the same developer: "Macromascot: Calorie & Fasting Tracker", "WoolStep: Learn to Knit" — [App Store](https://apps.apple.com/us/app/id1617533959)
- **AppGoblin, iOS** (third-party estimates):
  - Release 2022-04-20, 251 ratings at 4.24★, ~13K installs, ~835 MAU, revenue <$10K/mo, split "30% IAP, 70% ads".
  - SDKs: AdMob, Flutter, nanopb, Firebase, Adjust, RevenueCat, Superwall.
  — [AppGoblin iOS](https://appgoblin.info/apps/1617533959)
- **AppGoblin, Android:**
  - Developer Viral Apps LLC, released 2021-10-18, updated 2026-10-16.
  - ~824K installs, 4.21★ from 7.3K ratings, ~36K MAU, revenue <$10K/mo.
  - SDKs: AdMob, Facebook, Flutter, Kotlin, Firebase, Superwall.
  - Revenue split shown as 100% IAP / 0% ads. A search snippet of the same site said "IAP 37% · Ad 63%" with 790.4K installs.
  — [AppGoblin Android](https://appgoblin.info/apps/free.vpn.unblock.proxy.bamboovpn) (internally inconsistent)
- The Google Play page could not be parsed by the fetch tool. The install bucket was not directly confirmed — [Google Play](https://play.google.com/store/apps/details?id=free.vpn.unblock.proxy.bamboovpn&hl=en&gl=US)
- **Chrome extension "BambooVPN":**
  - Publisher Interactive Apps LLC, 1309 Coffeen Ave Ste 1200, Sheridan WY; email per@markusakerlund.com; D-U-N-S 139246808; self-declared EU "trader".
  - 1,000 users, 2.3★ (3 ratings), v2.0.3, updated Oct 14, 2026.
  — [Chrome Web Store](https://chromewebstore.google.com/detail/bamboovpn/kbcmkoncjllgdeanokoafadafhgflfmm)
- The same publisher's only other extension is "Funnel Studio Image Picker" — [Chrome publisher page](https://chromewebstore.google.com/publisher/interactive-apps-llc/u0de25391ed9589325ca4d51b0fbfc307)

### Inferences
- **Install base vs. revenue:** ~824K Android installs plus a small iOS footprint fit the "~500k users" claim only as cumulative installs. AppGoblin's ~36K Android MAU suggests a much smaller active base.
- **Platform split conflicts:** AppGoblin's iOS estimates (13K installs, 835 MAU) are hard to square with "iOS = 80% of revenue" and 1,490 subs. Third-party estimates for small iOS apps are unreliable. Trust the Superwall-verified TrustMRR numbers over AppGoblin.
- **Desktop status:** the founder says desktop and Chrome are "not yet released", yet a Chrome extension updated Oct 2026 and a Windows installer link exist. They have probably shipped since the note was written.
- **Ownership:** three entity names appear — Viral Apps LLC (iOS seller, Play developer, website), Interactive Apps LLC (Chrome), and "interactiveecommercellc" (Apple developer string). All share a commercial registered-agent address in Sheridan, WY, commonly used by non-US founders forming Wyoming LLCs. This looks like one owner or group running a small multi-app portfolio, not a large app factory. The links between Jim Løining, the per@markusakerlund.com contact and the LLCs are **not established**.
- The Apple developer account may not have been transferred to the buyer: "interactiveecommercellc" is unchanged and © is still Viral Apps LLC. This is unverified.

### Gaps
- Google Play exact install bucket, IAP range and data-safety section: the Play page was not parseable.
- Android developer's other apps: not retrieved.
- An APKMirror listing for "Bamboo VPN" under developer "billion" exists. Whether it is the same package or an older or unrelated app was not verified (403) — [APKMirror](https://www.apkmirror.com/apk/billion/bamboo-vpn/bamboo-vpn-1-5-2-release/bamboo-vpn-1-5-2-android-apk-download/)

## 4. How the VPN is built/sourced (fingerprinting)

### Takeaway
There is **no evidence of a white-label or wholesale VPN SDK**. The APK contains no Atom/PureVPN, Pango/Hydra/AnchorFree, VPNresellers, Windscribe, VPN Gate, Outline/Shadowsocks or V2Ray/Xray/sing-box code. Instead the app uses open-source tunnels: `wireguard_flutter`/`libwg-go` and ics-openvpn (`de.blinkt`) with bundled OpenVPN binaries. Its own custom backend (`bk.bamboovpn.com`) hands out server lists, OpenVPN configs and pooled WireGuard peers. This architecture points to **self-operated servers, most likely rented VPS/bare metal, managed by their own panel**. Confidence: moderate to high on "own backend, not SDK"; moderate on "own servers rather than imported wholesale configs".

### Cited Findings (all from static analysis of APK v2.18.0 unless otherwise linked)
- **VPN engines present:**
  - `libwg-go.so`, `libwg.so`, `libwg-quick.so` (official WireGuard Android backend) and the Flutter package `wireguard_flutter`.
  - `assets/pie_openvpn.*` and `nopie_openvpn.*` binaries, plus 197 `de.blinkt` strings (the open-source ics-openvpn library).
- **SDK keyword grep (hit counts across dex plus Dart snapshot):**
  - purevpn 0, pango 0, hydra 0, anchorfree 0, vpnresellers 0, windscribe 0, vpngate 0, softether 0.
  - ikev2 0, strongswan 0, v2ray 0, xray 0, sing-box 0, shadowsocks 0, trojan 0, vless/vmess 0.
  - The "atom" hits (139) contain no `atom*sdk`/`atomvpn` package names; they are generic words. The "outline" hits (104) are UI strings.
- **Custom backend API base `https://bk.bamboovpn.com`** (string: "Backend URL: https://bk.bamboovpn.com"). Endpoints:
  - `/api/servers`, `/api/servers/go-to-servers`, `/api/categories`, `/api/server-profiles/`, `/api/server-requests`
  - `/api/wireguard-peers/acquire-peer`, `/api/wireguard-peers/heartbeat`, `/api/wireguard-peers/release-peer`
  - `/api/secure-core/routes`, `/api/shield/availability/`, `/api/shield/preference`, `/api/user/dedicated-ips/my-ips`
  - `/api/auth/*` (including `save-revenuecat-alias`, `save-superwall-alias`), `/api/subscription/{status,sync,history,link-transaction}`
- **Config-handling strings:**
  - "has neither WireGuard nor OpenVPN config", "server(s) have valid OVPN configs", "defaulting to WireGuard".
  - "This route's entry server has no OpenVPN config. Contact support.", "OpenVPN servers usually require authentication!", "This Secure Core route is at capacity".
- **Other bundled pieces:**
  - The Flutter package `dart_ping` (client-side latency checks).
  - `get.geojs.io` (IP geolocation) and `1.1.1.1`.
  - Amazon Root CA certs in assets. These are typically bundled by AWS-dependent SDKs; no `amazonaws` hostnames were found.
- **Monetization and analytics stack:**
  - `superwallkit_flutter`, `purchases_flutter` (RevenueCat; entitlement "Bamboo VPN Pro"), `adjust_sdk`, `tenjin_plugin`, `mixpanel_flutter`.
  - Firebase (Analytics, Crashlytics, Messaging; project `bamboovpn-19a3f`), `google_mobile_ads`, `crisp_chat`, `google_sign_in`, `in_app_review`/`in_app_update`.
  - The AppsFlyer (12) and AppLovin (12) hits appear only inside Tenjin/mediation constants; no SDK packages were found.
- A legacy **Adapty** fallback paywall JSON (paywall "Bamboo", products one-month/three-month/one-year) is still bundled. Its `paywall_updated_at` decodes to 2024-03-11, which is pre-acquisition. The current stack is Superwall plus RevenueCat.
- **DNS:**
  - bamboovpn.com A records are 172.67.215.129 and 104.21.37.238 (Cloudflare). NS are brodie/christina.ns.cloudflare.com. MX is Google Workspace (smtp.google.com). SPF uses Google.
  — [dns.google](https://dns.google/resolve?name=bamboovpn.com&type=A)
- **Certificate transparency subdomains:** `admin`, `bk`, `myaccount`, `staggingbk`, `www`, plus a wildcard. `admin`, `bk` and `myaccount` all resolve to the same Cloudflare-proxied IPs, so the origin hosting is hidden — [crt.sh](https://crt.sh/?q=%25.bamboovpn.com)
- **WHOIS/RDAP:** bamboovpn.com was registered 2024-07-31 via **Hostinger operations, UAB**. Expires 2027-07-31; last changed 2026-10-23 — [Verisign RDAP](https://rdap.verisign.com/com/v1/domain/bamboovpn.com)
- AppGoblin lists **no VPN SDK** for the Android app — [AppGoblin Android](https://appgoblin.info/apps/free.vpn.unblock.proxy.bamboovpn)

### Inferences
- **Not an SDK white label.** Atom SDK, Pango/Hydra and similar SDKs ship their own client libraries and API hosts; none are present. VPN Gate, Outline and V2Ray-family stacks are also absent.
- **Self-built panel with self-hosted nodes is the most likely model.** The `acquire-peer` / `heartbeat` / `release-peer` design leases pre-provisioned WireGuard peers from a finite per-server pool. That pattern is typical of self-run WireGuard servers driven by a custom admin panel (`admin.bamboovpn.com`). Wholesale APIs such as VPNresellers usually issue per-user account credentials instead.
- The staging backend (`staggingbk`) and the "server-requests" endpoint (users requesting locations) indicate in-house tooling. The developer the founder mentions likely built this during the 2025–26 "rebuild" (WireGuard arrived in v2.10.00, Jun 2026).
- **Cannot rule out mixed sourcing.** OpenVPN configs are stored per server, and the string "OpenVPN servers usually require authentication!" would also fit .ovpn files imported from a wholesale or reseller provider with username/password auth. Some locations (e.g. China, Russia, Saudi Arabia) may be cheap VPS or, for "virtual" locations, mislabeled. This could not be verified without retrieving the server list.
- **Pre-acquisition.** The Adapty-era app (2024) may have used a different server source. The current architecture appears to be a post-acquisition rebuild.

### Gaps
- Actual VPN server IPs, ASNs and hosting providers (e.g. Hetzner, OVH, DigitalOcean, M247) were not obtained. The server list is fetched at runtime from the authenticated backend. Unauthenticated probing of bk.bamboovpn.com was blocked by session policy, and the app was not executed. This is the key missing proof for "own servers vs. wholesale configs".
- Origin hosting of bk/admin is hidden behind Cloudflare.
- iOS IPA not inspected (no public mirror attempted).

## 5. Marketing / acquisition

### Takeaway
The founder claims 100% organic growth: ASO on a keyword-stuffed Android package name (`free.vpn.unblock.proxy.*`) and titles like "Turbo Fast VPN" / "Speedy & Private", with no paid ads, email or upsells. The SDK stack nonetheless includes Adjust and Tenjin attribution, which is the kind of tooling used for paid UA. No ad campaigns or founder build-in-public posts were found.

### Cited Findings
- "Growth has been consistent and 100% organic". Email marketing, paid ads and upsells are listed as untapped — [TrustMRR](https://trustmrr.com/startup/bamboovpn)
- Title and keyword targeting:
  - Android "BambooVPN: Turbo Fast VPN" with package `free.vpn.unblock.proxy.bamboovpn` — [AppGoblin Android](https://appgoblin.info/apps/free.vpn.unblock.proxy.bamboovpn)
  - iOS "Bamboo VPN : Speedy & Private"; one listing variant was titled "BambooVPN - Secure VPN Proxy"; the description says "Use the Turbo VPN proxy with a single tap" — [App Store](https://apps.apple.com/us/app/id1617533959)
- Attribution and analytics SDKs: Adjust, Tenjin, Mixpanel, Firebase Analytics. AppGoblin lists Facebook among the ad SDKs — static APK analysis; [AppGoblin Android](https://appgoblin.info/apps/free.vpn.unblock.proxy.bamboovpn)
- The site has an Affiliate Program page and a Blog — [bamboovpn.com](https://bamboovpn.com)
- The app is localized into 19 languages, and the App Store lists 18 more besides English — [App Store](https://apps.apple.com/us/app/id1617533959)
- Searches for BambooVPN founder, Reddit or X posts returned nothing relevant ([search results incl. App Store only](https://apps.apple.com/us/app/id1617533959))

### Inferences
- Using "Turbo VPN" in the copy borrows a high-volume competitor's brand term, a common ASO tactic.
- Tenjin and Adjust may be left over from a previous owner's paid UA, or be groundwork for future ads. Their presence alone does not prove current ad spend.

### Gaps
- Meta Ad Library and TikTok Creative Center were not checked (JS-only interfaces), so ad activity is unverified.
- Apple Search Ads and keyword rankings: AppGoblin's keyword tab returned no data.
- No social accounts were identified.

## 6. Verdict: sourcing model, cost per user, margin consistency

### Takeaway
Best-evidence verdict: **own servers behind an in-house backend** (open-source WireGuard plus OpenVPN, custom panel). It is not an SDK white label or a free-server scraper.

| Hypothesis | Confidence | Basis |
|---|---|---|
| Own servers | moderate (~60–70%) | Custom backend, WireGuard peer-pool leasing, no vendor SDK |
| Wholesale OpenVPN/WireGuard configs imported into their own panel, for some or all locations | ~25–35% | Per-server OpenVPN configs with auth could come from a reseller |
| SDK white label (Atom/Pango/etc.) | <5% | No SDK code or API hosts in the APK |
| Free/VPN Gate/Outline servers | <5% | None of those stacks present |

The 70% margin claim is plausible under the self-hosted model.

### Cited Findings
- Supporting evidence is in §4: WireGuard/ics-openvpn, the `bk.bamboovpn.com` API with `wireguard-peers/acquire-peer`, no vendor SDK strings, and `admin`/`staggingbk` subdomains — static APK analysis; [crt.sh](https://crt.sh/?q=%25.bamboovpn.com)
- Revenue base: $6,807 per 30 days, 1,490 subs, $3.99/week or $51.99/year — [TrustMRR](https://trustmrr.com/startup/bamboovpn)

### Inferences (illustrative arithmetic, not sourced vendor prices)
- **Revenue per subscriber:** $6,807 / 1,490 ≈ $4.57 per sub per 30 days. That implies a mix weighted toward annual plans ($51.99/yr ≈ $4.33/mo). An all-weekly base would gross about $17/mo per sub.
- **Store fees:** at a 15% (small-business) store fee, net ≈ $5.8k per 30 days. A 70% margin then implies roughly $1.7k–2.0k/mo of total costs (servers, the developer, tools such as Superwall and RevenueCat).
- **Server cost per user, assuming roughly $1,000/mo of servers:** ≈ $0.67 per paying sub per month. Spread over about 36K Android MAU plus iOS free users (AppGoblin estimate), it is about $0.02–0.03 per active user per month.
- A fleet of ~20–40 VPS/dedicated nodes (needed for "50+ locations" with some reuse) would plausibly fit under about $1,000/mo. A per-account wholesale model typically costs more per paying user, but can still fit at this scale. Either way the 70% margin is arithmetically consistent.
- **Free tier:** free users are monetized with AdMob. This offsets bandwidth on free servers.
- **Risks for a buyer or competitor:**
  - Founder-reported 80% iOS revenue concentration.
  - Unclear transfer of developer accounts and LLC entities (the listings still sit under Viral Apps LLC / interactiveecommercellc).
  - Location claims vary across surfaces (15 countries vs "50+").
  - The Superwall feed has expired.
  - The founder-stated 2 hours a week depends on a retained developer who runs the backend.

### Gaps
- No direct evidence of hosting providers or ASNs for VPN nodes. To settle the own-vs-wholesale question, connect the app on a test device and resolve the endpoint IPs via ipinfo or bgp.he.net. This was not done because it requires running the app.
- No disclosed cost breakdown from the founder. The 70% margin was previously reported and was not visible on the 12 Nov 2026 fetch.

## 7. Web, desktop or config-based access: is BambooVPN mobile-only?

### Takeaway
BambooVPN is **not mobile-only**, but it is **app-only**. The download page offers iOS, Android, Mac (via the Mac App Store), a Windows installer and a Chrome/Edge/Brave extension. It mentions no manual WireGuard/OpenVPN config downloads, no Linux, no router support and no web checkout. The web account portal (`myaccount.bamboovpn.com`) is a login-only dashboard and does not show plans or configs. Mobile apps remain the business: the founder reports 80% iOS and 20% Play revenue.

### Cited Findings
- The download page lists five options:
  - iPhone/iPad (iOS 15+)
  - Android (Google Play)
  - Mac (the same App Store ID, id1617533959)
  - Windows 10+ (`https://bk.bamboovpn.com/downloads/BambooVPN-Setup-2.1.0.exe`, v2.1.0, served from the backend host)
  - Chrome extension (Chrome, Edge, Brave)
- The page also says "One subscription covers up to 10 devices at once." It does not mention Linux, Firefox, routers, manual WireGuard/OpenVPN config files, a web dashboard, or how desktop users pay — [Download page](https://bamboovpn.com/download)
- `myaccount.bamboovpn.com` is a "Welcome back / Sign in" login page (portal v1.0.20). No plans, checkout or config download are visible without logging in — [myaccount](https://myaccount.bamboovpn.com)
- The Android app links to `https://myaccount.bamboovpn.com/dashboard/dedicated-ip`. It also contains RevenueCat Stripe-store identifiers and a `usdt_text.svg` asset — static APK analysis (§4)
- The Chrome extension has 1,000 users and a 2.3★ rating from 3 ratings — [Chrome Web Store](https://chromewebstore.google.com/detail/bamboovpn/kbcmkoncjllgdeanokoafadafhgflfmm)
- Founder note: iOS ~80% of revenue, Play ~20%. Desktop and Chrome are described as built but not yet released — [TrustMRR](https://trustmrr.com/startup/bamboovpn)

### Inferences
- Revenue from desktop, extension and web is likely negligible today. All 1,490 Superwall-verified subscriptions run through App Store and Play billing. Desktop and extension users likely log in with the same account and get a cross-device entitlement (RevenueCat aliasing, "up to 10 devices").
- The Stripe and USDT hints point to web or off-store checkout that is planned or in partial use, likely for dedicated IPs or desktop. It is not visible publicly.
- **Their market position:** BambooVPN does **not** compete in the web-only "account plus downloadable configs" niche, where users buy on a website and import WireGuard/OpenVPN profiles into the official open-source apps. That niche is open relative to this competitor.

### Gaps
- Whether a user can buy on the web, export raw WireGuard/OpenVPN configs or use the official WireGuard app is unknown: the dashboard is behind login.
- The Windows installer was deliberately not downloaded or inspected.

## 8. Lessons for a web-only SaaS VPN (user will not build mobile apps)

### Takeaway
BambooVPN shows that a small team can run an own-server VPN on open-source WireGuard/OpenVPN with a custom backend and reach about $10k MRR at a claimed ~70% margin. The growth engine, though, is App Store/Play search plus mobile paywalls (Superwall, weekly plans). A web-only SaaS cannot copy that distribution. It can copy the infrastructure model and must replace distribution with web channels.

### Cited Findings
- Infrastructure is open-source WireGuard plus ics-openvpn with a custom panel. The backend uses the WireGuard peer-pool endpoints `acquire-peer` / `heartbeat` / `release-peer`, and no vendor SDK was found — static APK analysis (§4)
- Distribution and monetization:
  - About 824K Android installs; founder-reported "100% organic" and 80% iOS revenue.
  - Weekly $3.99–4.99 and yearly $51.99 subscriptions behind a Superwall paywall.
  - The free tier is ad-funded.
  — [TrustMRR](https://trustmrr.com/startup/bamboovpn); [AppGoblin Android](https://appgoblin.info/apps/free.vpn.unblock.proxy.bamboovpn); [bamboovpn.com](https://bamboovpn.com)
- The website itself monetizes nothing directly: download links only, a login-only portal, no web pricing checkout found — [Download page](https://bamboovpn.com/download); [myaccount](https://myaccount.bamboovpn.com)

### Inferences (recommendations, not sourced facts)
1. **Copy the backend pattern, not the apps.**
   - A WireGuard peer-pool panel (acquire/release/heartbeat), per-server OpenVPN configs and a server list API are all buildable as a web service.
   - For a web-only product, deliver **downloadable WireGuard/OpenVPN configs and QR codes** that users import into the free official WireGuard/OpenVPN clients on every OS.
   - This removes app development and app-store fees. The ~15–30% store fee is a margin BambooVPN gives up.
2. **Self-hosted servers are viable at this scale.** BambooVPN's numbers suggest a ~$1–2k/mo cost base is enough for about 1.5k paying users. Wholesale configs (e.g. VPNresellers-style) can fill exotic locations. BambooVPN may itself mix the two (unverified).
3. **Pricing reference:**
   - $3.99–4.99/week, which is mobile-paywall pricing.
   - $51.99/year (≈$4.33/mo).
   - About $4.57 revenue per subscriber per 30 days.
   Web buyers typically compare monthly and annual prices, so a weekly plan is a mobile-paywall artifact that may not translate to web.
4. **Distribution is the hard part.** BambooVPN's organic engine is ASO with keyword-stuffed listings ("free vpn unblock proxy", "Turbo VPN"). It has a website, blog and affiliate page, yet DR is only 16 and there is no web checkout. Web-only needs SEO, affiliates, communities and possibly crypto/Stripe checkout. BambooVPN's USDT/Stripe hints suggest even app-first players see demand for this.
5. **Differentiators BambooVPN already ships** that a web SaaS can match server-side: dedicated IPs, multi-hop "Secure Core", DNS-level ad blocking ("BambooShield"), 10 devices per subscription. Kill switch and split tunneling rely on the client; the official WireGuard apps provide basic equivalents.
6. **Risks:** be careful with location claims; BambooVPN shows inconsistent location lists across its own channels. Expect support load from manual-config users. Payment processors are cautious about VPN merchants; this is a general consideration, not verified here.

### Gaps
- No public data on BambooVPN web-sourced revenue. All verified revenue is from app stores via Superwall.
- Wholesale per-account prices and VPS costs were not researched in this task. See the separate build-models notes (`vpn_build_models.md`) if available.
