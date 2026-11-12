# BlueVPN and the "IPTV Player & VPN" bundle (BIEL LLC / Opus): competitor teardown, as of 12 Nov 2026

Scope note: the user plans a web-only SaaS VPN, not apps. Priorities were (1) revenue, (2) how the VPN is sourced, (3) website features and pricing, (4) web, desktop or config access versus mobile-only, plus lessons for a web SaaS. Collection date: 2026-11-12.

Two labels are used below:
- **[V] Verified** means it was observed directly in a primary source: a TrustMRR page, the Apple lookup API, a Google Play page, the companies' own websites, DNS, crt.sh, ipinfo, or an APK that was only unpacked and read, never run.
- **[I] Inference** means it is my reading of that evidence.

---

## 1. Revenue and sales data (TrustMRR, re-checked 2026-11-12)

### Takeaway
Both businesses are small and shrinking. BlueVPN is about $2.3k MRR from 248 subscriptions and is down about 50% from its May 2026 peak. The Opus IPTV+VPN bundle is about $11.7k MRR from 4,080 subscriptions; monthly revenue fell about 45% from January to October 2026. The bundle is for sale at $500k, which TrustMRR shows as 2.9x. Almost all of the bundle's money appears to come from the IPTV player, not the VPN.

### Cited Findings

**BlueVPN** (RevenueCat API-verified; not merchant of record; not for sale) — [TrustMRR](https://trustmrr.com/startup/bluevpn) / [TrustMRR .md](https://trustmrr.com/startup/bluevpn.md)
- [V] Revenue: last 30 days $2,162 (−25.4%). MRR $2,321 (−16.2% over 30 days). Active subscriptions: 248.
- [V] Revenue by period: last 24h $45.55 · 7d $305 · 3 months $8,553 · 6 months $22,568 · 12 months $40,985 · all-time $72,857.
- [V] Monthly revenue:

  | Month | Revenue |
  |---|---|
  | Dec 2025 | $2,584 |
  | Jan 2026 | $2,452 |
  | Feb 2026 | $2,521 |
  | Mar 2026 | $3,403 |
  | Apr 2026 | $3,714 |
  | May 2026 | $4,902 (peak) |
  | Jun 2026 | $4,558 |
  | Jul 2026 | $4,803 |
  | Aug 2026 | $4,025 |
  | Sep 2026 | $3,241 |
  | Oct 2026 | $2,600 |
  | Nov 1–12 2026 | $820 |

- [V] Founder: blank. Founded date: blank. Country: blank. Estimated users: 4,100. Markets: Security, Utilities, Mobile Apps. Pricing text: "Free trial; premium… pricing may vary depending on location." TrustMRR rank #770. X followers: 0. The tech stack lists only RevenueCat.
- [V] The listing's "website" is the App Store link. TrustMRR still shows the old name "Fast VPN turbo IP Changer", version 4.3, bundle ID `com.app.connect.vpn.BlueVpn`, and 4.7 stars from 4,093 ratings.

**IPTV Player & VPN bundle**, shown as "Stealth Company" with founder "BIEL LLC" (RevenueCat API-verified) — [TrustMRR](https://trustmrr.com/startup/iptv-player-vpn-app-bundle) / [.md](https://trustmrr.com/startup/iptv-player-vpn-app-bundle.md)
- [V] Revenue: last 30 days $14,279 (−11.2%). MRR $11,740 (−1.6%). Active subscriptions: 4,080.
- [V] Revenue by period: 3 months $49,968 · 6 months $98,162 · 12 months $258,566 · all-time $1,168,052.
- [V] Monthly revenue:

  | Month | Revenue |
  |---|---|
  | Dec 2025 | $27,715 |
  | Jan 2026 | $29,150 |
  | Feb 2026 | $25,399 |
  | Mar 2026 | $26,242 |
  | Apr 2026 | $24,403 |
  | May 2026 | $16,999 (step down) |
  | Jun 2026 | $15,245 |
  | Jul 2026 | $19,143 |
  | Aug 2026 | $18,228 |
  | Sep 2026 | $17,478 |
  | Oct 2026 | $16,103 |
  | Nov 1–12 2026 | $5,193 |

- [V] Profit margin over the last 30 days: 93.0%. The description claims "$238K TTM profit and approximately 90% margin."
- [V] Country: US. Founded: 2022-09-01. Website traffic over the last 30 days: 565 visitors. Google impressions: 2,105. Revenue per visitor: $25.32. This means almost no revenue comes from the web; it is store-driven.
- [V] Tech stack: React Native, Objective-C and Swift on the front end; Node.js, Express, MongoDB and RevenueCat on the back end. Marketing channels listed: ASO, Blog, Content marketing, SEO, Google Ads, Word of mouth.
- [V] Sale terms:
  - Listed for sale on 2026-06-18 (Starter tier). Asking price $500,000, shown as 2.9x.
  - 1,890 recent buyer views and 11 offers.
  - Seller's message: "two cross-platform apps under the same brand: IPTV Player on iOS, tvOS, Android, Android TV, and VPN on iOS, tvOS, Android. Strong bundling and cross-sell potential, especially on tvOS, where VPN competition is limited. Sold only as one portfolio. Post-acquisition dev/UI-UX support available under separate contract."
  - No explicit reason for the sale is given.

### Inferences
- [I] **Revenue per subscription:**
  - BlueVPN: $2,321 / 248 ≈ $9.4 per subscription per month. That fits a weekly or short-term subscription model; the in-app purchases run $6.99–$49.99.
  - Opus: $11,740 / 4,080 ≈ $2.9 per subscription per month. That fits mostly $29.99/year plans.
- [I] **What the 2.9x multiple is based on:** $500k / ($14,279 × 12) ≈ 2.9x, so it is 30-day revenue annualized. Against the trailing 12 months it is ≈1.9x revenue, or ≈2.1x the claimed $238k profit.
- [I] **Profit claim versus revenue:** $238k profit against $258.6k revenue over the trailing 12 months implies about 92% margin. That is consistent with very low costs. It is plausible because store fees appear to be taken out before RevenueCat's "revenue" figure, or else the margin excludes them. Unverified.
- [I] **Why the bundle is likely being sold:** the decline from January to October 2026 (about −45%) and an unmaintained VPN app (see section 2) suggest the owners are exiting a declining asset.
- [I] **BlueVPN's 2026 pattern:** releases sped up from v2.0 (March 2026) to v4.4 (November 2026), the privacy policy was rewritten in February 2026, and revenue rose from March to July. This fits an acquisition and relaunch push by the new owner, after which revenue fell back once that push faded.

### Gaps
- The TrustMRR pages do not break down MRR, churn or ad spend. Those require a login.
- How much of the Opus revenue is VPN versus IPTV is not disclosed anywhere (see section 2 for the proxies).

---

## 2. Sourcing verdict: wholesale, own servers, or SDK?

### Takeaway
- **Opus VPN (BIEL LLC): own servers, run themselves. High confidence.** It uses open-source OpenVPN (via `react-native-simple-openvpn`) and IKEv2 on about 27 rented VPS and dedicated servers, under its own hostnames `*.ikev2.opusvpn.app`. A home-built API (`api.opusvpn.app`, endpoint `/v2/servers`) hands out the configurations. I found no white-label or wholesale SDK.
- **BlueVPN: could not be determined.** It is iOS-only, so there is no APK to inspect. Its website and policies name no network provider. The parent company is an app acquirer.

### Cited Findings

**Opus VPN** (Android `com.biel.opus.vpn` v1.2.5, build 44, from the APKPure mirror; unpacked and read only, never run)
- [V] It is a React Native app (RN 0.71.4, Expo SDK 48, Hermes). Its module list includes:
  - `react-native-simple-openvpn` 2.1.3
  - `react-native-purchases` 7.28.1 (RevenueCat)
  - `@react-native-firebase/analytics`
  - `react-native-fbsdk-next` (Meta)
  - `@sentry/react-native`
  - `@hexigames/react-native-apple-ads-attribution`
  - `@sparkfabrik/react-native-idfa-aaid`
  - `react-native-aws3`
  - in-house packages `monkeys-native-toolbox` and `monkeys-paywall-builder`

  Source: the APK's `assets/modules.json`.
- [V] Native libraries include `libopenvpn.so`, `libovpn3.so`, `libovpnexec.so`, `libovpnutil.so` and `libosslspeedtest.so`, plus `assets/pie_openvpn.*`. These are the standard open-source ics-openvpn and OpenVPN3 binaries.
- [V] The code mentions OpenVPN (137 times in classes2.dex) and IKEv2. It has RevenueCat (~1,700 references), Facebook SDK, OneSignal, AppsFlyer IDs and Sentry.
- [V] I found **no** strings for Atom/PureVPN/PureWL, Pango/AnchorFree, VPNresellers, Windscribe, WireGuard, V2Ray/Xray, sing-box, Shadowsocks, Outline or VPN Gate. The "hydra" hits were React's "hydration" code, not the Hydra SDK.
- [V] The JS bundle contains `api.opusvpn.app/announcements/`, a `/v2/servers` path and an `ovpnString` field. The app fetches server configurations from its own backend.
- [V] It also contains paywall endpoints `pw.monkeysteam.com/v1/client/{handshake,identify,attribution,fetch/placement,view/placement,purchase_cancel,set/attribute}`, paywall images at `monkeys-team.ams3.cdn.digitaloceanspaces.com/aso-studio/paywall/…`, short links `aso.st/vpnopus/offer`, `aso.st/opusmediaplayer`, and Freshdesk at `opusiptv.freshdesk.com`.
- [V] crt.sh shows 543 certificates for `opusvpn.app` since 2023-03-14, including about 27 server hostnames: `ams-1/2, bar-2, chicago-1, fra-1/2/3, ist-1/2, la-1/2, lon-1/2, mad-1, miami-1, nyc1, nyc-2, par-1/2, sao-2, sfo1, sgp1, sing-2, syd-2, tor-1/2, wash-1 .ikev2.opusvpn.app`, plus `api.` and `root.` — [crt.sh](https://crt.sh/?q=%25.opusvpn.app)
- [V] Where those servers sit, per ipinfo.io lookups on resolved A records ([ipinfo.io](https://ipinfo.io)):
  - **AS136258 BrainStorm Network**: about 20 hosts (AMS, BCN, FRA, LA, LON, MAD, MIA, NYC, PAR, SAO, SIN, SYD, TOR). The PAR hosts reverse-resolve to `lstn.net`, which is Limestone Networks.
  - **AS14061 DigitalOcean**: nyc1, sfo1, sgp1, and `root.opusvpn.app`.
  - **AS46475 Limestone Networks**: chicago-1.
  - **AS16276 OVH**: wash-1.
  - **AS206991 Iksir Internet, Istanbul**: ist-1, ist-2.
- [V] Domains: `opusvpn.app`, `api.opusvpn.app`, `biel.llc`, `monkeysteam.com` and `aso.st` all use the **same Cloudflare nameserver pair (algin/lila.ns.cloudflare.com)**, which points to the same Cloudflare account. `opusmediaplayer.com` and `opusiptv.com` are hosted on Hetzner (AS24940, Helsinki). `vpn.monkeysteam.com` resolves to a DigitalOcean IP. `monkeysteam.com` has certificates going back to 2017, with subdomains such as `football-api.apps`, `swagpunch`, `selffix`, `popback` and `clarux`. That pattern looks like an app studio — [crt.sh](https://crt.sh/?q=%25.monkeysteam.com)
- [V] The privacy policy at [api.opusvpn.app/privacy-policy.html](https://api.opusvpn.app/privacy-policy.html) (updated 2023-03-23) states "TLS 1.2 with perfect forward secrecy (ECDHE), 128-bit/256-bit AES GCM … ChaCha20 Poly1305". It also says "Separate from our consumer applications, BIEL LLC licenses its technology to third party partners." It names Google Analytics and MaxMind.
- [V] The terms at [api.opusvpn.app/terms-of-use.html](https://api.opusvpn.app/terms-of-use.html) accidentally say "iON VPN is not responsible…". They also state that servers and software "are owned by BIEL LLC."

**BlueVPN** (iOS `com.app.connect.vpn.BlueVpn`, App Store id 6444899367)
- [V] Seller: **HUMAN DATA SG PTE. LTD.** The seller URL is vpn-blue.info. Released 2022-12-20; v4.4 on 2026-11-11; 139 MB; 15–16 languages. The app has been **renamed "VPNN: Secure IP Changer"**; it was previously "Fast VPN turbo IP Changer", "Turbo VPN Proxy Master", and other names. Copyright: "© Blue VPN" — [Apple lookup API](https://itunes.apple.com/lookup?id=6444899367&country=us), [App Store](https://apps.apple.com/us/app/id6444899367)
- [V] The developer's other apps are a mixed portfolio of apparently acquired apps. Their bundle IDs carry other owners' prefixes:
  - Clone Armies (`com.clonearmies.elecube`)
  - EMI Calculator (`com.appaspect.loan.emicalculator`)
  - Huge Digital Clock
  - Verba (2026)
  - Cash Calculator (`com.appfactory.cashcalculator`, Nov 2026)

  Source: [Apple developer lookup](https://itunes.apple.com/lookup?id=1619123351&entity=software)
- [V] vpn-blue.info is a Vite/React single-page app with a Sanity CMS blog, Google Analytics ID G-V4YT1K976B, and Cloudflare in front (AS13335). crt.sh shows only `vpn-blue.info` and `*.vpn-blue.info`, first seen 2022-12-06. Every policy and contact page gives **contactus@kalagato.co** as the contact. Source: site JS bundle, read only, not run.
- [V] KalaGato describes itself as specializing in "mobile app acquisitions and growth strategies." A Clone Armies seller testimonial appears on its site — [kalagato.co](https://kalagato.co/). YourStory reports KalaGato as Singapore-headquartered, started in 2017 as a data-analytics firm, and committing $100M to buy apps — [YourStory 2022](https://yourstory.com/2022/10/mobile-app-buyout-firm-kalagato-commits-100-million/amp)
- [V] The privacy policy (updated 2026-02-24) is generic "no-logs" boilerplate. It says servers are "in highly secure data centers," and it names Google Analytics for Firebase and **Apphud**. Apphud is a subscription SDK, but TrustMRR verification uses RevenueCat. It names **no VPN infrastructure provider** — [vpn-blue.info privacy](https://vpn-blue.info/vpn-blue/privacy-policy/)
- [V] AppGoblin has not run an SDK scan on this app. Its estimates: about 344K installs, about 23K monthly active users, revenue under $10k/month, 100% in-app purchases — [AppGoblin](https://appgoblin.info/apps/6444899367)
- [V] There is no Google Play version; Play returns 404 for the bundle ID. So no APK exists to inspect.

### Inferences
- [I] **Opus: own infrastructure, high confidence.**
  - The servers sit under the brand's own subdomains and are spread across five unrelated hosting companies.
  - The naming is ad hoc: `nyc1` versus `nyc-2`, `sgp1` versus `sing-2`, `lon1` versus `lon-1`. That looks like servers added one at a time by hand. A wholesale network like PureWL or VPNresellers would normally give you *their* endpoints or a dedicated-server product, not this.
  - The protocols are open-source OpenVPN and IKEv2, set up by their own API.
  - BrainStorm Network (AS136258) is an IP-leasing and transit operator often seen behind budget dedicated servers and VPS. [I] This is not a white-label VPN provider.
  - Rough cost: about 27 servers at roughly $5–60 each per month comes to about $0.3k–1.5k/month. That fits the 93% margin.
  - The "licenses its technology to partners" line and the "iON VPN" slip are copy-pasted boilerplate from other VPNs' policies, not evidence of any partner relationship.
- [I] **Who runs Opus.** BIEL LLC uses a Delaware registered-agent address (2093 Philadelphia Pike #9239, Claymont, DE 19703, per Google Play), which suggests a non-US founder. The same Cloudflare account covers Opus, biel.llc and monkeysteam.com, and the app depends on the "Monkeys Team / ASO Studio" paywall SDK. There are Turkish UI strings ("AYLIK" = monthly, "E-Posta adresiniz" = your email) and Istanbul servers. Taken together, this strongly suggests a Turkish app studio, "Monkeys Team", operating through a US LLC. This is unconfirmed by any public statement.
- [I] **BlueVPN: unknown, but likely not built in-house by the current owner.**
  - BlueVPN appears to be a KalaGato-owned app. The developer account HUMAN DATA SG is likely KalaGato's original data-analytics entity (`humandatasystems.com`), and the contact email is KalaGato's.
  - The app was bought, not built. The original developer's infrastructure, whether self-hosted, a white-label, or a free-tier SDK, may have come with the purchase.
  - The 139 MB app size is large for a VPN. It *could* indicate bundled multi-protocol cores (sing-box or Xray libraries are tens of MB), but this is speculative.
  - Confidence that it uses a wholesale network: low. Confidence that it uses own servers: low. **Treat it as undetermined.**

### Gaps
- No IPA could be obtained for BlueVPN or the Opus iOS app, so I could not inspect their frameworks.
- I deliberately did not query the live `api.opusvpn.app/v2/servers` endpoint, since that goes beyond passive lookups. So the full server count and OpenVPN locations are unknown. The IKEv2 list above may be incomplete.
- No public statement from BIEL, Monkeys Team or KalaGato confirms ownership links.

---

## 3. Product, website, pricing and acquisition

### Takeaway
Both products are store-first apps with thin marketing websites. BlueVPN sells through an aggressive paywall: 3-day trial, then weekly or short plans, with in-app purchases from $6.99 to $49.99. Opus VPN is a cheap add-on, $1.99/week up to a $59.99 lifetime option. The Opus IPTV player is the main product, charging $2.99–$79.99 with device-count tiers.

### Cited Findings
**BlueVPN / VPNN**
- [V] Features listed on the App Store:
  - one-tap connect and pause
  - three "modes": Online Anonymity, Full Security, Fast Access
  - automatic nearest server
  - home-screen widgets
  - no registration needed
  - free trial, then a paid plan whose "price and trial length depend on the plan and your location"

  Source: [Apple lookup](https://itunes.apple.com/lookup?id=6444899367&country=us)
- [V] US in-app purchases: $6.99 (×4 variants), $9.99, $12.99, $15.99, $39.99 (×2), $49.99. They carry names like "Fake GPS", "Protection 360 Pro" and "Change location & ip changer" — [App Store](https://apps.apple.com/us/app/id6444899367)
- [V] The privacy label lists usage data used for tracking — [App Store](https://apps.apple.com/us/app/id6444899367)
- [V] Website claims contradict each other: "servers in over 150 countries", "50+ countries", "thousands of servers", and a hard-coded list of 12 countries totalling about 235 servers (US 50+, UK 30+, DE 25+, JP 20+, CA 20+, FR 18+, AU 15+, IN 15+, SG 12+, KR 12+, BR 10+, UAE 8+). It also claims "military-grade encryption", "kill switch" and "DNS leak protection". There is no pricing on the website; it only links to the App Store. The blog is empty ("Add your first blog post in the Sanity Studio dashboard") — [vpn-blue.info](https://vpn-blue.info/)
- [V] Search marketing appears in two places. The listing is renamed by country (e.g. "Turbo VPN Proxy Master", "Fast VPN Unlimited IP Changer", and others) — [AppFollow](https://apps.appfollow.io/ios/vpn-service-secure-ip-changer/6444899367?country=de), [App Store CM](https://apps.apple.com/cm/app/turbo-vpn-proxy-master-hide-me/id6444899367?l=en-GB). The website has the Google tag with Consent Mode, and the privacy policy mentions "Google Analytics and Adwords."

**Opus VPN (BIEL LLC)**
- [V] iOS app id 6446252310, released 2023-03-30. Last update v1.9.1 on **2025-04-22**. 58 US ratings at 4.3. Subtitle "Best School VPN for iPhone."
- [V] US in-app purchases: Weekly $1.99, Monthly $4.99, 3 months $11.99, 6 months $21.99, Yearly $17.99/$35.99/$49.99 in several versions, Lifetime $59.99. The description says "$17.99 per year."
- [V] Runs on iPhone, iPad, Mac (M1), **Apple TV (tvOS 17+)** and Vision.

  Sources: [App Store](https://apps.apple.com/us/app/id6446252310), [Apple lookup](https://itunes.apple.com/lookup?id=1578690529&entity=software)
- [V] Android `com.biel.opus.vpn`: released 2023-07-06, **100K+ installs (129,780)**, last update 2025-02-07, in-app purchases "$1.99–$29.99 per item", supports Android TV. Developer contact: hello@biel.llc and the Claymont, DE address — [Google Play](https://play.google.com/store/apps/details?id=com.biel.opus.vpn)
- [V] opusvpn.app is a generic landing page: "Join over +100k happy customers", placeholder testimonials, "© 2023 Biel LLC". It shows no server count and no pricing — [opusvpn.app](https://opusvpn.app/)

**Opus IPTV player** (main revenue driver)
- [V] iOS id 1592313576, released 2022-06-07, v2.0.0 on 2026-11-05 (adds a Mac app and QR-code device linking). 938 US ratings at 4.3.
- [V] Plans by number of devices: 2 devices $2.99/month, $7.99/3 months or $19.99/year; 5 devices $4.99/month, $12.99/3 months or $29.99/year; 10 devices $39.99/year or $79.99 lifetime.
- [V] The in-app purchase list also shows Weekly $4.99, Monthly $9.99 and a Special Offer Yearly at $14.99.

  Sources: [Apple lookup](https://itunes.apple.com/lookup?id=1578690529&entity=software), [App Store](https://apps.apple.com/us/app/id1592313576)
- [V] Android `com.biel.opus.media.player`: "Released on Jun 3, 2026", 10K+ installs (27,314), in-app purchases $2.99–$79.99 — [Google Play](https://play.google.com/store/apps/details?id=com.biel.opus.media.player)
- [V] The website lists iOS, iPadOS, Mac, Apple TV, Vision, Android, Android TV/Google TV, Fire TV and **Windows 10/11**. Samsung/Tizen is "coming soon." The free tier plays 15 minutes a day. Free web tools: an Xtream-to-M3U converter and an M3U editor. Footer: "powered by BIEL LLC" — [opusmediaplayer.com](https://opusmediaplayer.com/)
- [V] Cross-selling, seen in the APKs only (read, not run):
  - The IPTV app contains a Play link `details?id=com.biel.opus.vpn&…utm_source=opusiptv`, `vpn_button_pressed` and `vpn_active` events, product IDs `opusvpn_1`/`opusvpn_2`, and "OPUS VPN_URL".
  - The VPN app links to `aso.st/opusmediaplayer` and shows `tv_feature.png`/`devices.png` paywall art.
  - The IPTV app's App Store listing and in-app purchase list do **not** mention the VPN.

### Inferences
- [I] **How much of the bundle is VPN versus IPTV:**
  - US iOS ratings: 938 for IPTV versus 58 for the VPN.
  - The VPN app has not been updated since early 2025, while the IPTV app gets frequent releases.
  - Revenue per subscription (~$2.9/month) matches IPTV's $19.99–$29.99/year plans.

  My estimate is that the VPN is ≤10–20% of revenue. This is unverified; Android installs are the one exception (VPN 130K versus IPTV 27K on the new listing).
- [I] **The VPN is an add-on to the IPTV app.** IPTV users want to hide their streaming from their ISP or get around geo-blocks, so offering a VPN inside an IPTV player turns piracy-adjacent use into a cross-sale. The seller's point about tvOS is that there are few VPN apps on Apple TV.
- [I] **Legal and store risk is real.** The IPTV player's Android listing restarted in June 2026 ("Released on Jun 3, 2026"), which may mean an earlier listing was removed. This is unverified. The heavy "player only, no content" disclaimers and Xtream Codes support are typical of IPTV players that app stores periodically remove. A buyer, or anyone copying the model, takes on that risk.

### Gaps
- No Meta Ad Library, Apple Search Ads or founder social posts were checked; I dropped these to stay efficient after the scope change. TrustMRR lists Google Ads for Opus. BlueVPN's privacy policy mentions AdWords. The Opus VPN APK contains Meta SDK and Apple Ads attribution.
- No exact Google Play install count was found for any earlier Opus IPTV Android listing.

---

## 4. Web, desktop or config-based access versus mobile-only

### Takeaway
Neither product offers a web dashboard, browser extension, Windows/macOS VPN client, or downloadable WireGuard/OpenVPN configs. Both are app-store subscriptions. BlueVPN is Apple-only (iPhone, iPad, plus Mac and Vision Pro running the iPad app). Opus VPN covers iOS, Apple TV, Android and Android TV. Only the Opus IPTV *player* has a Windows app.

### Cited Findings
- [V] BlueVPN runs on iPhone, iPad, Mac (M1+, the iPad app) and Vision. There is no Apple TV or Android version, and the website has no account or config portal. "No registration or login required" — [App Store](https://apps.apple.com/us/app/id6444899367), [Apple lookup](https://itunes.apple.com/lookup?id=6444899367&country=us)
- [V] Opus VPN runs on iOS, iPadOS, Mac (M1, "Not verified for macOS"), tvOS 17+ and Android (including Android TV). The website has no pricing, no login and no configs — [App Store](https://apps.apple.com/us/app/id6446252310), [opusvpn.app](https://opusvpn.app/)
- [V] The Opus IPTV player supports Windows 10/11 and links devices by QR code — [opusmediaplayer.com](https://opusmediaplayer.com/)

### Inferences
- [I] Neither competitor serves desktop and web-first VPN buyers. Neither has a Stripe-billed web checkout, so both pay 15–30% to the app stores. That leaves room for a web-only competitor.

### Gaps
- None material.

---

## 5. Lessons for a web-only SaaS VPN

### Takeaway
Both businesses show that the VPN servers themselves are cheap: about 27 rented boxes support a business at roughly 93% margin. Both businesses are also store-driven and declining. A web-only SaaS gives up App Store search traffic, so it must find customers another way, through SEO, content, affiliates, or a niche such as configs for routers and TVs, while keeping the cheap self-hosted infrastructure.

### Cited Findings
- [V] Opus runs its VPN on about 27 servers across BrainStorm, DigitalOcean, OVH, Limestone and an Istanbul host, using only open-source OpenVPN and IKEv2, and reports 93% margin — sources in section 2 and [TrustMRR](https://trustmrr.com/startup/iptv-player-vpn-app-bundle.md)
- [V] Opus's website brings in only 565 visits a month against about $14k a month in revenue, so the business runs almost entirely on store traffic — [TrustMRR](https://trustmrr.com/startup/iptv-player-vpn-app-bundle.md)
- [V] BlueVPN makes about $9.4 per subscription per month by using trials and short-term plans on iOS — [TrustMRR](https://trustmrr.com/startup/bluevpn.md)

### Inferences
- [I] **Infrastructure:** you do not need a white-label reseller to start. A dozen to 30 VPS or dedicated servers running WireGuard, IKEv2 or OpenVPN, with a small API that hands out configs, costs hundreds of dollars a month. Use your own hostnames (`<city>-N.vpn.yourdomain`). Be aware that crt.sh exposes your whole server fleet; use a wildcard certificate if you want to hide it.
- [I] **Product gap:** neither competitor offers config downloads (WireGuard QR, `.ovpn`, IKEv2 profiles), router or Apple TV setup guides, or desktop coverage. A web SaaS can sell exactly that: "one account, configs for every device including TV and router." Apple TV customers want this, which is the opening Opus's seller points to.
- [I] **Pricing:** these app businesses use weekly plans of $1.99–$6.99 because of store paywall psychology. A web SaaS cannot copy weekly trials with store-managed billing. Expect monthly and annual plans (~$3–10/month) and lower conversion, but keep the 15–30% the stores would take.
- [I] **Acquisition:** Opus's free IPTV tools (an M3U converter and editor) are SEO bait for a specific audience. The web-SaaS version is free utilities such as "Is my VPN working?" (which opusvpn.app already has) or IP and leak tests. A niche audience (IPTV users, school and work network users, travellers) beats generic "fast VPN" pages.
- [I] **Risk:** avoid IPTV and piracy positioning; it brings app-store, payment-processor and legal risk. Payment processors are stricter than the App Store about this. Also avoid copy-pasted policies that name another VPN, like Opus's "iON VPN" slip, and inconsistent server claims like BlueVPN's "150+ countries" versus a 12-country list. Both damage trust and can create consumer-protection exposure.

### Gaps
- There is no direct cost data for either company's infrastructure. The cost figures above are estimates from typical VPS pricing.
