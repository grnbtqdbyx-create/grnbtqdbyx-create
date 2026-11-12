# Turkey-based founder (with existing US LLC + Stripe): legal, regulatory, payments and tax landscape for (a) a branded VPN subscription and (b) international mobile top-ups / digital gift cards (as of Nov 2026)

Research date: 2026-11-12. About 22 searches and fetches. Many sources are secondary (law-firm blogs, accounting columns, VPN-industry blogs), and this is flagged where it matters. **Nothing here is legal or tax advice.** Points marked [NEEDS PROFESSIONAL ADVICE] need a Turkish lawyer (BTK/5651/6493) or a mali müşavir/YMM (tax).

---

## 1. VPN in Turkey: legality, BTK authorization, Law 5651, blocking actions, app stores, and risk of selling to Turkish vs. international users

### Takeaway
As of Nov 2026, no Turkish law bans VPN *use*, and there is no VPN-specific licensing regime in force. Since Nov 2023, however, BTK has had ISPs block the major commercial VPNs, relying on Law 5651 Art. 6(1)(ç); that legal basis is being challenged at the Council of State. An April 2026 **draft** amendment to Law 5809 would create a "sanal ağ hizmeti" category. It would require VPN providers to set up a Turkish AŞ/Ltd, obtain BTK authorization, and face fines of TRY 1M–30M plus up to 95% throttling. If the draft passes, a branded VPN marketed to Turkish users would be squarely in scope. Selling only to non-Turkish users carries much lower regulatory risk.

### Cited Findings
**Legal status of use and operation**
- Turkish law contains no provision prohibiting access through alternative means or VPN use — [İFÖD EngelliWeb 2025, ch. 11 "VPN Blockings"](https://ifade.org.tr/en/reports/engelliweb-2025/11-vpn-blockings/)
- Turkish law-firm blogs likewise say no statute bans VPN use. Liability arises only if the content accessed or the activity through the VPN is itself illegal — [Harbiye Hukuk](https://www.harbiyehukuk.com/?p=12080); [or.av.tr "VPN kullanmak yasak mı?"](https://or.av.tr/vpn-kullanmak-yasak-mi/); [Kadim Hukuk](https://kadimhukuk.com.tr/makale/vpn-kullanmak-yasak-mi-cezasi-nedir/)
- The general principle of Law 5809 (Elektronik Haberleşme Kanunu) is that electronic communications services are provided by operators BTK has authorized. The sources do not settle whether a VPN provider currently falls within "elektronik haberleşme hizmeti" requiring yetkilendirme — [Hukukçular Evi – BTK yetkilendirme 5809](https://hukukcularevi.com/danismanlik/btk-yetkilendirme-elektronik-haberlesme-5809/); BTK's own authorization-regime pages: [BTK authorization regime](https://btk.gov.tr/en/authorization-regime), [BTK – services not subject to authorization](https://www.btk.gov.tr/en/yetkilendirmeye-tabi-olmayan-elektronik-haberlesme-hizmet-sebeke-ve-altyapilari)
- BTK published a VPN-related document in 2017 (Telkoder-hosted "BTK_VPN_02.02.2017"). Its content was not retrieved — [Telkoder PDF](https://telkoder.org.tr/wp-content/uploads/2017/07/BTK_VPN_02.02.2017.pdf)

**April 2026 draft VPN law (NOT enacted as of sources found)**
- Webtekno, 21 Apr 2026, citing İFÖD, describes the draft as follows:
  - It is "henüz taslak aşamasında" (still at draft stage).
  - It would add "sanal ağ hizmeti" (virtual network service) and "sanal ağ hizmet sağlayıcı" (virtual network service provider) to Law 5809.
  - VPN providers would have to operate through a Turkish **anonim or limited şirket** with "tam yetkili temsilciler" (fully authorized representatives), under **BTK authorization**.
  - Unauthorized operation would carry an administrative fine of **TRY 1 million – 30 million**.
  - If the fine is unpaid and obligations are unmet within 6 months, bandwidth could be **throttled up to 95%**, or the provider's apps and sites blocked.
  - Source: [Webtekno](https://www.webtekno.com/vpn-duzenlemeye-dair-yeni-detaylar-h215785.html)
- İFÖD confirms the draft would add a new Art. 60/17 to Law 5809 allowing throttling of up to 95% or blocking of a VPN provider's apps and sites for late fine payment. İFÖD calls it an attempt to give statutory footing to existing practice — [İFÖD EngelliWeb 2025](https://ifade.org.tr/en/reports/engelliweb-2025/11-vpn-blockings/)
- Other coverage of the draft licensing regime: [Reclaim The Net "Turkey to Ban Anonymous VPNs"](https://reclaimthenet.org/turkey-to-ban-anonymous-vpns); [Diken – Akdeniz: "VPN servislerini zapturapta almayı deneyecekler"](https://www.diken.com.tr/?p=1713990)

**Blocking actions 2023–2026 (Law 5651)**
- BTK circular letter of **23.11.2023** (no. E-34817124-421.99-72342) told access providers to block **16 VPN services**, including:
  - Proton VPN, Surfshark, IPVanish, CyberGhost, PureVPN, TunnelBear, Hotspot Shield, NordVPN, ExpressVPN
  - Psiphon, Hola, Turbo VPN, HideMyAss, Touch VPN, PIA, Secure VPN
  - Source: [İFÖD](https://ifade.org.tr/en/reports/engelliweb-2025/11-vpn-blockings/)
- Legal basis cited by BTK: **Law 5651 Art. 6(1)(ç)**, the duty of access providers to take "alternative-access-prevention measures" for content already under a blocking decision — [İFÖD](https://ifade.org.tr/en/reports/engelliweb-2025/11-vpn-blockings/)
- EngelliWeb identified **454 server addresses across 26 VPN services** blocked as of 2023. The largest counts were Hotspot Shield (116), NordVPN (75), VPN Unlimited (74) and ExpressVPN (37). Mullvad, IVPN and VyprVPN are also listed as blocked on some ISPs — [İFÖD](https://ifade.org.tr/en/reports/engelliweb-2025/11-vpn-blockings/)
- The litigation is still open:
  - İFÖD sued BTK on 28.02.2024.
  - Ankara 17th Administrative Court dismissed the case on 24.10.2024.
  - Ankara Regional Administrative Court reversed that dismissal on jurisdictional grounds on 30.12.2025.
  - The case is now **pending before the Danıştay** (Council of State) as court of first instance.
  - Source: [İFÖD](https://ifade.org.tr/en/reports/engelliweb-2025/11-vpn-blockings/)
- Secondary sources report a further wave in **Aug 2024** of about 27 VPN services, including NordVPN, ExpressVPN and Surfshark. They also report DPI-based dropping of standard VPN protocol signatures, with obfuscated protocols as the main workaround. These are travel and VPN-marketing sites of lower reliability — [Nomad Istanbul (tested Oct 2026)](https://nomadistanbul.com/kb/what-is-blocked-in-turkey-vpn/); [TechRadar](https://www.techradar.com/pro/vpn/after-instagram-turkey-blocks-access-to-popular-vpn-apps); [VPN blocking – Wikipedia](https://en.wikipedia.org/wiki/VPN_blocking)
- BTK separately blocked international **eSIM** providers (Airalo, Holafly, Saily, Nomad) from July 2025 — [FTN News](https://ftnnews.com/travel-news/news-from-turkey/turkeys-2025-esim-vpn-restrictions-what-travelers-should-know/); [Alertify](https://alertify.eu/turkey-vpn-ban/). This is relevant to the top-up/eSIM business line.

**App stores**
- A VPN vendor blog, citing The Moscow Times, says that as of June 2025 **14 VPN apps** were unavailable in the Turkish Apple App Store, against 113 in Russia. This is secondhand — [Mysterium VPN](https://www.mysteriumvpn.com/news/app-store-censorship)
- Apple has removed other apps from the Turkish App Store after Turkish access bans, for example Discord and Ekşi Sözlük, and Hornet in 2021. This shows Apple complies with Turkish removal orders — [Türkiye Today – Discord](https://www.turkiyetoday.com/business/discord-removed-from-turkiyes-app-store-following-access-ban-67319); [SCF – Ekşi Sözlük](https://stockholmcf.org/?p=61013); [Hornet support](https://hornet.com/contributors/support/article/hornet-removed-from-turkey-app-store)

### Inferences
- **Selling to Turkish users** brings three exposures today:
  - The brand's domains, apps and servers can be added to BTK's 5651 Art. 6(1)(ç) block lists without notice. İFÖD says users and providers were never notified.
  - Apple is likely to remove the app from the TR storefront if ordered.
  - If the April 2026 draft is enacted, the operator would need a Turkish company plus BTK authorization, or face TRY 1–30M fines and throttling.
- A Turkey-resident founder running an *unauthorized* VPN aimed at Turkish users would be far easier to enforce against than foreign providers. This is the main structural risk.
- **Selling only to non-Turkish users** removes most BTK/5651 exposure. Two cautions remain:
  - The founder is still a Turkish tax resident, so tax points below apply.
  - If the draft is enacted, its wording should be checked to see whether it reaches Turkish-resident operators serving only foreign users.
- A cautious go-to-market would geo-exclude Turkey at signup and checkout, avoid Turkish-language marketing of the VPN, and avoid TR-based servers. [NEEDS PROFESSIONAL ADVICE]

### Gaps
- No primary text of the April 2026 draft (TBMM kanun teklifi number) was found. Its enactment status as of Nov 2026 is not confirmed; the latest sources describe it only as a draft.
- No BTK primary document states whether a pure VPN/proxy service currently needs yetkilendirme (bildirim) under the 5809 framework. The 2017 BTK VPN document was not read.
- No primary Apple or Google transparency data was found for VPN removals in Turkey in 2025–2026. Nothing at all was found on Google Play.
- Law 5651 hosting-provider (yer sağlayıcı) or access-provider log-retention obligations, and how they would apply to a Turkish VPN operator, were not researched in primary text. See Section 5.

---

## 2. Top-ups and gift cards in Turkey: Law 6493 licensing, limited-network exemption, Turkish operator rules, MASAK

### Takeaway
Payment services and e-money are licensed by **TCMB** under Law 6493; the payment-services mandate moved from BDDK to TCMB in 2019–2020. Unlicensed payment services carry **1–3 years' imprisonment and up to 5,000 days' judicial fine**. Prepaid instruments usable only within a limited network, or for a limited range of goods and services, are reportedly outside scope. Above a volume threshold, however, notification or licensing may be triggered. Reselling third-party airtime or gift cards as an ordinary merchant (buying codes wholesale and selling them as goods) differs from issuing stored value or transferring funds. No source settled where a top-up/gift-card reseller falls, so this needs a formal opinion.

### Cited Findings
- TCMB is the competent authority for licensing and supervising payment and e-money institutions under Law 6493 — [TCMB – Ödeme Hizmetleri Genel Bakış](https://www.tcmb.gov.tr/wps/wcm/connect/tr/tcmb+tr/main+menu/temel+faaliyetler/odeme+hizmetleri/genel+bakis); [TCMB – Ödeme Kuruluşları list](https://tcmb.gov.tr/wps/wcm/connect/tr/tcmb+tr/main+menu/temel+faaliyetler/odeme+hizmetleri/odeme+kuruluslari); [TCMB – E-Para Kuruluşları list](https://www.tcmb.gov.tr/wps/wcm/connect/tr/tcmb%2Btr/main%2Bmenu/temel%2Bfaaliyetler/odeme%2Bhizmetleri/elektronik%2Bpara%2Bkuruluslari)
- A law-firm guide says prepaid instruments usable only in the issuer's own store network or for a defined group of goods and services, and "limited network" applications, are **outside the scope** of the law. The same guide says exceeding a transaction-volume threshold can trigger a **notification duty**, and the activity may become subject to licensing — [Hukukçular Evi – 6493 TCMB lisans](https://hukukcularevi.com/danismanlik/odeme-elektronik-para-kuruluslari-tcmb-lisans/)
- Activities such as bill payment, money transfer, mobile payment, e-money and prepaid cards are described as requiring a licence — [PwC Türkiye](https://www.pwc.com.tr/tr/risk-surec-teknoloji-hizmetleri/bilgi-teknolojileri-risk-hizmetleri-yayinlari/odeme-hizmetleri-ve-elektronik-para-ihtiyaci-nedir-pwc-turkiye.pdf)
- 2024 secondary-legislation amendments defined **"dijital cüzdan" (digital wallet)** as a licensed service requiring at least an "ödeme aracı ihracı" licence. This matters if the platform holds customer balances or wallet credits — [Çakmak Avukatlık – Ödeme Hizmetleri İkincil Mevzuatında Önemli Değişiklikler (Jul 2024)](https://cakmak.av.tr/wp-content/uploads/2024/07/Odeme-Hizmetleri-Ikincil-Mevzuatinda-Onemli-Degisiklikler.pdf)
- TCMB published guidance on which business models map to which payment-service types. A licence analysis should start from the exemption list — [Erdem & Erdem – TCMB guideline on business models](https://www.erdem-erdem.av.tr/en/insights/guideline-introduced-by-the-central-bank-on-business-models-used-in-payments-associated-with-payment-service-types)
- Penalty for unlicensed payment services: **1–3 years' imprisonment and up to 5,000 days' judicial fine**. TCMB has a mechanism for reporting unauthorized providers — [Moroğlu Arseven – guide on notifying TCMB of unauthorized payment services](https://www.morogluarseven.com/insights/ma-gazette-en/magazette-edition-40-8-march-2017/the-guide-for-applications-on-notifying-the-central-bank-of-the-republic-of-turkey-regarding-persons-and-institutions-providing-unauthorized-payment-services/); [Alomaliye – TCMB press release on unlicensed providers](https://www.alomaliye.com/2021/09/10/izinsiz-odeme-hizmeti-sunan-kisi-ve-kuruluslar-hakkinda-basin-duyurusu/)
- TÖDEB has a professional regulation (mesleki tanzim kararı) on measures for mobile payment services by payment and e-money institutions — [TÖDEB](https://todeb.org.tr/source/Mevzuat/Birlik-Duzenlemeleri/odeme_kuruluslari_ve_elektronik_para_kuruluslarinca_mobil_odeme_hizmeti_sunumunda_alinacak_tedbirlere_iliskin_mesleki_tanzim_karari-pdf.pdf)
- **Wholesale suppliers:** Reloadly's API covers airtime top-ups worldwide and a gift-card catalogue of 14,000+ products, and markets explicitly to "pure resellers." Clients reselling to end users must also accept Reloadly's Platform Client Terms, which were not retrieved — [Reloadly corporate terms](https://reloadly.com/corporate-terms); [Reloadly presentation](https://www.reloadly.com/reloadly_presentation.pdf); [Reloadly platform client terms](https://reloadly.com/platform-client-terms)
- In typical reseller agreements, the **reseller is the Merchant of Record** to end customers. This example is from Reach, not Ding or Reloadly — [Reach reseller terms](https://www.withreach.com/merchant-terms-of-service)
- Payment-industry onboarding lists classify "store of digital value (vouchers, e-wallets, mobile money and e-money)" as **high risk** — [Peach Payments high-risk list](https://support.peachpayments.com/support/solutions/articles/47001276655-capitec-pay-high-risk-industry)

### Inferences
- **Lower-risk model:** sell fixed-denomination third-party codes or airtime one transaction at a time, delivered immediately, with no customer wallet or balance and no peer-to-peer transfers. This looks like ordinary sale of digital goods or services. **Higher-risk model:** adding a stored balance, wallet, cash-out, or "send top-up to someone else, funded by the sender's balance" could look like e-money issuance, a digital wallet, or money remittance under 6493. [NEEDS PROFESSIONAL ADVICE — ödeme hukuku avukatı]
- International airtime top-ups are commonly used as a remittance substitute, so payment partners and AML teams treat them as high risk.
- If the Turkish entity sells *Turkish* operator top-ups (Turkcell, Vodafone TR, Türk Telekom), it would normally need a dealer or distributor agreement with the operator or an authorized distributor. Selling only foreign-operator top-ups through Reloadly or Ding avoids that.
- Selling eSIMs to people in Turkey is a separate risk: BTK has blocked foreign eSIM sellers since July 2025 (see Section 1).

### Gaps
- No primary text of 6493 Art. 12 (scope exemptions, including limited network and electronic communications operator payments) was retrieved. The exact exemption wording and any volume threshold are unverified.
- No TCMB opinion was found on whether reselling gift cards, game codes or airtime requires a licence.
- Nothing specific was found on Turkish operators' rules for third-party top-up resellers.
- **MASAK:** no source was retrieved. Law 5549 and its regulation list obliged parties ("yükümlüler"). Banks, payment and e-money institutions are obliged; a plain e-commerce merchant generally is not, but its PSP will apply KYC and monitoring to it. This is unverified and should be confirmed with counsel.
- Ding's and Reloadly's onboarding requirements for a Turkish-resident reseller, and their wholesale margins and pricing, were not found.

---

## 3. Payments through the founder's existing US LLC: Stripe rules for VPN and for gift cards / stored value / top-ups; reserves, Radar and 3DS; alternatives if Stripe refuses (high-risk acquirers, Paddle, Lemon Squeezy, crypto); brief note on Turkish PSPs

*(Updated after the user clarified that the founder already has a US LLC and will collect payments through Stripe via that LLC.)*

### Takeaway
- **VPN subscription via a US LLC on Stripe: plausible.** VPN, proxy and "anonymity" services do **not** appear anywhere on Stripe's prohibited or restricted list; the only telecom item is jamming equipment. A standard SaaS-style VPN subscription should therefore go through normal onboarding. Stripe still reviews every account and can apply reserves at its discretion.
- **Gift cards / third-party stored value: "Restricted" on Stripe.** This means extra due diligence, possible requests for licences or business-model detail, possible refusal, and approval that is per-offering and revocable. Stripe also lists money transmitters, remittance and other MSBs among the categories on its list, and international airtime top-ups are commonly treated as remittance-adjacent.
- **Consequence for the business plan:** build the top-up and gift-card line expecting that it may need (a) explicit Stripe approval in writing, or (b) a separate high-risk acquirer and/or crypto rail. It should not share a Stripe account with the VPN, so that a termination does not take down both lines.

### Cited Findings
**Stripe policy text** (all from [Stripe – Prohibited and Restricted Businesses](https://stripe.com/legal/restricted-businesses))
- Checked the full page for "VPN", "proxy", "anonym", "phone" and "prepaid": **none appear**. The only telecom-related prohibited item is "Telecommunications manipulation equipment, including jamming devices."
- Restricted under "Nonfiat currency and stored value":
  - "Preloaded payment cards, gift cards, virtual credits, or other products and services"
  - "Sale of stored value or credits maintained, accepted, and issued by anyone other than the seller"
  - "Seller-maintained stored value or credits may be subject to limits."
- The list also names "Money transmitters, remittances, currency exchange services, and other money service businesses" and "Peer-to-peer money transmission." The fetched text did not show which tier (prohibited or restricted) each item is in; see Gaps.
- What "restricted" means:
  - These businesses require additional due diligence before Stripe confirms it can support them.
  - Applicants may be asked for proof of relevant licences or more detail on the business model.
  - Stripe may not approve them.
  - Approval is specific to each service offering and can be modified or revoked at any time under the Stripe Services Agreement.

**Reserves**
- Stripe uses **fixed and rolling reserves**, sized by the business's risk level (industry conditions, payment activity, financial stability), and notifies the account by email when it applies one — [Stripe Support – Reserves FAQ](https://support.stripe.com/questions/reserves-frequently-asked-questions?locale=en-GB); [Stripe – Rolling reserves 101](https://stripe.com/en-ca/resources/more/rolling-reserves-101-what-they-are-why-they-matter)
- Stripe's help content shows a worked example of a **25% rolling reserve with a 30-day release window** for a US business. This is an illustration, not a quoted rate — [Stripe Support – Reserves FAQ](https://support.stripe.com/questions/reserves-faq)
- Third-party sources claim rolling reserves of **90–180 days**; Stripe itself publishes no percentage range. Unverified — [terms.law – Stripe holds FAQ](https://terms.law/FAQ/payment-processors/stripe-holds-faq.html)

**Fraud tooling (Radar and 3DS)**
- Stripe's default approach is to let **Radar dynamically request 3D Secure** based on risk level. Manual 3DS triggering is for advanced users with their own fraud engine — [Stripe Docs – Authenticate with 3D Secure](https://docs.stripe.com/payments/3d-secure/authentication-flow)
- **Custom 3DS rules need Radar for Fraud Teams** (Radar Plus). Example rules request 3DS above a risk score or amount — [Stripe Docs – Radar rules](https://docs.stripe.com/radar/rules)
- Gift cards are a classic fraud vector. Stolen cards buy codes that are redeemed instantly, and the merchant absorbs the chargeback. This is why the vertical is treated as high risk — [Marix – gift card merchant high risk](https://marix.app/library/faq/gift-card-merchant-high-risk)

**Alternatives if Stripe refuses or is too risky for top-ups and gift cards**
- **Paddle:**
  - "VPN and Proxies (Restricted Category)", with enhanced due diligence.
  - Stored value, including **gift cards and vouchers, prohibited**.
  - Approval at Paddle's "absolute discretion."
  - Fee 5% + $0.50 (third-party figure).
  - Sources: [Paddle Help – AUP](https://www.paddle.com/help/start/intro-to-paddle/what-am-i-not-allowed-to-sell-on-paddle); [Paddle MSA](https://www.paddle.com/legal/terms); [Unibee review](https://unibee.dev/blog/paddle-review-features-pricing-pros-cons/)
- **Lemon Squeezy:**
  - Prohibits anything restricted by its processing partners (Stripe) and "regulated services such as… cellular/communication… banking/financing… currency exchange."
  - Fee 5% + $0.50 plus surcharges.
  - Owned by Stripe since 2024. Stripe's own MoR product, **Stripe Managed Payments**, is in preview, and sources conflict on its pricing.
  - Sources: [Lemon Squeezy – Prohibited products](https://docs.lemonsqueezy.com/help/getting-started/prohibited-products); [Freemius](https://freemius.com/blog/payment-processing-fees/); [MEAN CEO](https://blog.mean.ceo/stripe-vs-lemon-squeezy/)
- **High-risk merchant accounts:**
  - Gift cards sit "squarely in the high-risk tier." High-risk is not a ban, but it needs a processor experienced in the vertical with a real acquiring-bank relationship.
  - Ask a provider "Who is your acquiring bank for merchants in my vertical?"
  - Sources: [Marix](https://marix.app/library/faq/gift-card-merchant-high-risk); [NerdWallet – best high-risk processors 2026](https://www.nerdwallet.com/business/software/best/high-risk-payment-processors); [Chargebacks911](https://chargebacks911.com/high-risk-merchant-accounts/)
- **Crypto rails:**
  - Crypto settlement does not remove the need for a card account, because customers still want to pay by card.
  - Some fiat-to-crypto gateways market "no merchant KYC, no rolling reserves, no MATCH list." These are unverified marketing claims, and they are a compliance red flag for a gift-card business.
  - Sources: [Inqud blog 2026](https://inquid.blogspot.com/2026/06/high-risk-payment-processing-in-2026.html); [TechBullion](https://techbullion.com/high-risk-merchant-account-in-2026-the-complete-guide-including-crypto-settlement-alternatives/); [NOWPayments blog](https://nowpayments.io/blog/risk-merchant-providers-gateways)
- **Wholesale supply:** Reloadly offers top-up and gift-card APIs aimed at resellers, under separate API Terms and Platform Client Terms. In typical reseller contracts the reseller is the Merchant of Record — [Reloadly corporate terms](https://reloadly.com/corporate-terms); [Reloadly platform client terms](https://reloadly.com/platform-client-terms); [Reach reseller terms (example)](https://www.withreach.com/merchant-terms-of-service)

**Brief note: Turkish PSPs (de-emphasized)**
- iyzico and PayTR need a Turkish merchant entity.
- TCMB 2026 caps: foreign-issued cards 1.90%, single-payment TL credit card 3.56%.
- PayTR from about 2.19%. iyzico has no public price; Paynet was folded into iyzico from 1 Jan 2026.
- These are relevant only if a Turkish company invoices, for example under the service-export regime in Section 4. Using them for VPN sales to Turkish users would increase BTK exposure (Section 1).
- Sources: [Karekod.org](https://www.karekod.org/blog/sanal-pos-komisyon-oranlari/); [KobiTime](https://kobitime.com/sanal-pos-ucretleri-ve-sanal-pos-firmalari-2026/)

### Inferences
- **VPN on Stripe:** the main risks are not policy text but (a) chargeback and fraud ratios, since VPN buyers include card-testers and fraudsters hiding their IP; (b) sanctions screening, because Stripe must block users in comprehensively sanctioned jurisdictions; and (c) marketing that frames the product as evading law enforcement or national blocks. Keep messaging privacy and security focused. Use Radar plus 3DS on first payment, and consider blocking prepaid and anonymous cards via Radar rules.
- **Top-ups and gift cards on Stripe:**
  - Disclose the business model honestly at onboarding. Do not label it as "VPN/SaaS"; misclassification is a common cause of termination with funds held.
  - Expect questions on supplier (Reloadly or Ding), KYC, velocity limits and refund policy, and possibly a request for an MSB or legal opinion (see Section 4, FinCEN).
  - Mitigations: low per-order and per-day caps, 3DS on every order, delayed code delivery for new customers, and no customer stored balance.
- **Separation:** run each line under a separate Stripe account, or ideally a separate LLC. Stripe can link accounts, so this reduces but does not eliminate contagion risk.
- **Fallback order for top-ups and gift cards:** Stripe (approved restricted) → specialist high-risk acquirer → crypto (supplementary). Paddle and Lemon Squeezy are effectively unavailable for this line. For the VPN, Paddle remains a fallback MoR that also removes EU VAT and US sales-tax work.

### Gaps
- The fetched Stripe page did not reveal which tier "money transmitters / remittances / MSBs" falls in. That matters for airtime top-ups and should be verified directly on the page or with Stripe sales.
- No published Stripe reserve percentages for gift cards or VPNs exist; reserves are set case by case.
- No named high-risk acquirers with verified pricing for gift cards or top-ups were found. Typical high-risk pricing and reserves (often cited as about 3.5–6% plus a 5–10% rolling reserve) are unverified.
- Coinbase Commerce and NOWPayments policies on gift-card merchants were not verified.
- PayPal was not researched for a US LLC with a Turkish-resident owner.

---

## 4. Company structure and tax: US-side obligations of the foreign-owned single-member LLC; US sales tax; FinCEN MSB / prepaid access for top-ups and gift cards; Turkish taxation of a Turkish resident owning a US LLC; the Turkish-company service-export alternative

### Takeaway
- **US federal tax filing:** a foreign-owned single-member LLC is a disregarded entity. Every year it must file **Form 5472 with a pro forma Form 1120**, even with zero revenue. The penalty is **$25,000 per form**. With no US trade or business (no ECI), there is generally no US federal income tax.
- **State costs:** Delaware annual tax of $300 (one source says $400 from 2026), plus a registered agent of about $100/yr.
- **US sales tax:** SaaS and digital subscriptions are taxable in a growing set of states, and economic nexus thresholds count *all* sales. A VPN sold to US consumers via direct Stripe may create state sales-tax obligations. An MoR such as Paddle avoids this.
- **FinCEN:** sellers of closed-loop gift cards are generally not MSBs and are not required to register. Exceptions apply above $10,000 per person per day, or where products are open-loop or usable without later ID. Airtime top-ups have no clear FinCEN ruling. [NEEDS US COUNSEL]
- **Turkey:** a Turkish-resident individual is taxed on worldwide income. The LLC's profit is reportedly taxable in Turkey as ticari kazanç or menkul sermaye iradı. Under the Turkey–US treaty, business profits without a US permanent establishment are taxable in Turkey. KVK Art. 7 CFC rules tax only *corporate* shareholders and need ≥25% passive income, so they likely do **not** apply to an individual owning an active VPN or top-up LLC. The bigger risks are Turkish taxation of the LLC's income directly and an "iş merkezi in Turkey" argument. [NEEDS PROFESSIONAL ADVICE — YMM]

### Cited Findings
**US federal obligations (foreign-owned single-member LLC)**
- Since tax years beginning 1 Jan 2017, a foreign-owned disregarded entity must file **Form 5472 with a pro forma Form 1120** (Treas. Reg. §1.6038A-1). This applies even with no revenue or activity. The 1120 is a cover sheet and creates no corporate tax liability — [SDO CPA – Form 5472 guide](https://www.sdocpa.com/form-5472-foreign-owned-business-guide/); [Zenind – filing guide](https://www.zenind.com/help/post/foreign-owned-single-member-llc-filing-guide-form-5472-pro-forma-1120-deadlines-and-penalties); [VJM Global – pro forma 1120](https://www.vjmglobal.com/feeds/blog/pro-forma-1120-foreign-owned-llc)
- **Penalty:** $25,000 per form per year (secondary sources; IRS primary not fetched) — [Taxes for Expats – Form 5472 penalty](https://cdn.taxesforexpats.com/articles/foreign-business/form-5472-penalty.html); [Dimov Tax](https://dimovtax.com/irs-form-5472/)
- **Deadline and filing method:** due 15 April (calendar year), extendable to 15 October. One source says the form must be mailed or faxed rather than e-filed — [Zenind](https://www.zenind.com/help/post/foreign-owned-single-member-llc-filing-guide-form-5472-pro-forma-1120-deadlines-and-penalties)
- If the LLC's income is effectively connected with a US trade or business, the foreign owner may need to file **Form 1040-NR**, typically with Schedule C — [Vergi Merkezi – 2025 ABD vergi beyanı LLC rehberi](https://vergimerkezi.com.tr/2025-abd-vergi-beyani-llc-rehberi/)
- **Delaware costs:**
  - Atlas: $500 one-time; $100/yr registered agent.
  - Delaware LLC annual tax: $300, or $400 from 1 Jan 2026 per one source (conflicting).
  - Sources: [Rho](https://www.rho.co/blog/stripe-atlas-review); [Stripe – Delaware LLC costs](https://stripe.com/resources/more/how-much-does-it-cost-to-form-an-llc-in-delaware-fees-and-other-costs); [AgentDeals 2026](https://agentdeals.dev/company-formation-pricing-2026)

**US state sales tax on VPN / digital subscriptions**
- Each state decides whether software, SaaS or digital services are taxable. Recent expansions:
  - Vermont: remotely accessed software, from 1 Jul 2024
  - Louisiana: HB 8, from 1 Jan 2025
  - Utah: SB 162, digital subscriptions, from 1 Jul 2026
  - Texas: SaaS taxed as data processing, 80% taxable
  - Sources: [Numeral – SaaS sales tax by state 2026](https://numeral.com/blog/sales-tax-on-saas); [Sales Tax Institute](https://www.salestaxinstitute.com/resources/saas-sales-tax-expansion-by-state); [TaxJar – SaaS sales tax](https://www.taxjar.com/sales-tax/saas-sales-tax-)
- Economic-nexus thresholds count all sales, not only taxable ones — [sales.tax – digital goods 2026](https://sales.tax/expert-articles/sales-tax-on-digital-goods-whats-taxable-in-2026-and-what-changed/)
- No source addressed VPN subscriptions specifically.

**FinCEN: MSB / prepaid access (gift cards, top-ups)**
- The 2011 FinCEN Prepaid Access Final Rule includes these points:
  - **Closed-loop prepaid access** below **$2,000** maximum value per device per day is outside "prepaid program."
  - Limited **open-loop** access up to **$1,000/day** is also outside, subject to conditions: no international use, no person-to-person transfers, no non-bank reloads.
  - **Providers** of prepaid access must register as MSBs.
  - **Sellers** are not required to register, but must keep an AML program if they sell products usable without later customer ID, or sell more than $10,000 to one person in a day without preventive policies.
  - Sources: [FinCEN – Prepaid Access Final Rule press release](https://www.fincen.gov/news/news-releases/fincen-issues-prepaid-access-final-rule); [Federal Register 76 FR 45403 (29 Jul 2011)](https://www.federalregister.gov/documents/2011/07/29/2011-19116/bank-secrecy-act-regulations-definitions-and-other-regulations-relating-to-prepaid-access); [Safeheld summary](https://safeheld.com/resources/provider-of-prepaid-access); [Lexology – FinCEN prepaid FAQs](https://www.lexology.com/library/detail.aspx?g=e550ea9a-4727-4104-963d-d80fefabd4ef)
- FinCEN administrative rulings on prepaid and stored value are fact-specific. FIN-2014-R006 concerns open-loop; FIN-2009-R001 found a stored-value reload processor was *not* a money transmitter in that arrangement. No airtime-specific ruling was found — [FIN-2014-R006](https://www.fincen.gov/system/files/administrative_ruling/FIN-2014-R006.pdf); [FIN-2009-R001](https://www.fincen.gov/system/files/shared/fin-2009-r001.pdf)
- Gaming and digital-goods companies can become "inadvertent MSBs" through stored value or transfer features — [Wilson Sonsini](https://www.wsgr.com/en/insights/how-gaming-companies-can-become-inadvertent-money-services-businesses.html)

**Turkish taxation of a Turkish resident owning a US LLC**
- A single-member LLC is a US "disregarded entity." Commentators say a Turkish full taxpayer must include the LLC income in Turkey as **ticari kazanç or menkul sermaye iradı** — [Manay CPA – ABD şirketinden kâr payı](https://www.manaycpa.com/tr/abddeki-sirketinizden-turkiyeye-kar-payi-cekimi-nasil-vergilendirilir/); [Lemon Academy – LLC ve çifte vergi](https://lemonacademy.co.uk/?p=40737)
- Under the **Turkey–US DTA (1996)**, absent a US permanent establishment, business profits are taxable in Turkey, the residence state. US tax paid may be credited subject to the treaty — [Lemon Academy](https://lemonacademy.co.uk/?p=40737)
- **KVK Art. 7 (kontrol edilen yabancı kurum / CFC)** has four cumulative conditions:
  - ≥50% control by Turkish full taxpayers, individuals included in the count
  - ≥**25% passive income** (interest, dividends, rent, royalties, securities gains)
  - Foreign tax burden **<10%**
  - Gross revenue >TRY 100,000
  - Source: [Hukukçular Evi – KVK 7 (2026)](https://hukukcularevi.com/kontrol-edilen-yabanci-kurum-kazanci-kvk-7-yuzde-50-kontrol-yuzde-25-pasif-gelir-yuzde-10-vergi-yuku-dagitilmayan-kar-kvk-33-2-mahsup-sonraki-kar-payi-gercek-kisi-cvoa-2026/); [Alomaliye – KEYK kazancının vergilendirilmesi (Apr 2025)](https://www.alomaliye.com/2025/04/14/kontrol-edilen-yabanci-kurum-kazancinin-vergilendirilmesi/)
- **Only corporate shareholders are taxed** under Art. 7, pro rata, whether or not profits are distributed. Individuals count toward control but are not taxed under the article; their dividends follow general rules. Treaties do not prevent Art. 7 application to residents, per the administration's view, which is disputed — [Hukukçular Evi](https://hukukcularevi.com/kontrol-edilen-yabanci-kurum-kazanci-kvk-7-yuzde-50-kontrol-yuzde-25-pasif-gelir-yuzde-10-vergi-yuku-dagitilmayan-kar-kvk-33-2-mahsup-sonraki-kar-payi-gercek-kisi-cvoa-2026/)
- Sources differ on the passive-income threshold quoted in older literature (25% vs. other figures). The 2026 summary and the statute as commonly cited use 25% — [Alomaliye 2023](https://www.alomaliye.com/2023/09/25/yurtdisi-istirak-kazanclari-istisnasi-ve-kontrol-edilen-yabanci-kurum-kazanci/); [Vergi Raporu 2012](https://vergiraporu.com.tr/upImage/org/2012-151-Kontrol_Edilen_Yabanci_Kurum_Kazanclarinin_Vergilendirilmesi-Nur_Pehlivan_Karakoc%20.pdf)

**Alternative or complement: Turkish company exporting services** (kept from the earlier research)
- **KDV exemption** (KDVK 11/1-a, 12/2) applies when the customer is abroad **and** benefits abroad. GİB özelgeler accepted software, design and video streaming to foreign users — [Alomaliye 2024](https://www.alomaliye.com/2024/07/30/yurt-disinda-mukim-firmaya-verilen-tasarim-yazilim-ve-danismanlik-hizmetinin-kdv-ve-kvk-karsisindaki-durumu/); [Alomaliye – faydalanma kriteri](https://www.alomaliye.com/2014/09/22/hizmet-ifasinda-turkiyede-faydalanmafaydalanmama-kriteri/)
- **Service-export income deduction** (KVK 10/1-ğ, GVK 89/1-13):
  - Raised to **100%** by Presidential Decision 11257 (RG 30.04.2026), from 80% under Law 7524, for periods from **1 Jan 2026**.
  - Software and data processing/storage are listed.
  - Conditions: used **exclusively abroad**, and **all** earnings brought to Turkey by the return deadline.
  - Companies still face the **10% domestic minimum CIT**; individuals (GVK 89) can reach zero.
  - Sources: [KPMG Vergi](https://kpmgvergi.com/blog/munhasir-hizmetlere-saglanan-indirim-orani-100-e-cikarildi/1391); [PwC TR bulletin 2026](https://www.pwc.com.tr/tr/Hizmetlerimiz/vergi/vergi-bultenleri/2026/yurt-disi-istirak-kazanci-istisnasi-ve-hizmet-ihracinda-indirim-uygulamasi-hakkinda-cumhurbaskani-karari.pdf); [Alomaliye May 2026](https://www.alomaliye.com/2026/05/17/hizmet-ihracati-kazanc-ve-kurumlar-vergisi-indirimi-asgari-kurumlar-vergisi-ve-kdv-istisnasi/); [Ekonomi Gazetesi – münhasıran çıkmazı](https://www.ekonomigazetesi.com/kose-yazisi/hizmet-ihracatinda-100-indirim-sira-munhasiran-cikmazinda-78578)

### Inferences
- **US cost floor for the existing LLC:**
  - Delaware tax $300–400/yr
  - Registered agent about $100/yr
  - Form 5472 + pro forma 1120 preparation, typically a few hundred USD at specialist firms (not sourced)
  - Total roughly **USD 500–1,000/yr** before sales-tax compliance, about TRY 21,000–42,000 at an assumed ~42 TRY/USD (rate not sourced; check current).
- **ECI:** a Turkey-resident founder operating remotely, with no US office, employees or dependent agent, is the classic "no ECI" fact pattern. US-located VPN servers or US staff could change that analysis. [US tax advice]
- **US sales tax:** selling the VPN directly via Stripe to US consumers means monitoring state nexus (Stripe Tax can calculate). Using Paddle as MoR transfers this, at a 5% + $0.50 cost.
- **FinCEN:**
  - *Lowest-risk:* reselling closed-loop third-party gift cards (e.g., a retailer's own card) in small denominations, with per-customer daily caps well below $10,000 and identity captured. This fits the "seller of prepaid access, no registration" pattern.
  - *Higher-risk:* open-loop prepaid cards (Visa/Mastercard gift cards) and any customer wallet or balance.
  - *Unclear:* international airtime top-ups. Whether an airtime reseller is a "money transmitter" turns on whether it is seen as transmitting value to a third party abroad. Many US airtime sellers rely on the telecom-product characterization, but no FinCEN source was found.
  - State money-transmitter laws may also apply independently.
  - [NEEDS US FINTECH COUNSEL]
- **Turkish CFC:** with an individual owner and active income (VPN subscriptions, top-up margins), KVK Art. 7 likely does not bite, since the owner is not a corporation and the income is not passive. The more relevant Turkish points are:
  1. The founder's worldwide-income declaration of LLC profits, as ticari kazanç at progressive rates up to 40% (rates not sourced here), or as dividend/menkul sermaye iradı depending on characterization.
  2. The risk that a US LLC managed entirely from Turkey is treated as having its **iş merkezi (place of effective management) in Turkey**, making it a Turkish full taxpayer under KVK Art. 3. This is unverified, and the search found no source.
  3. If the founder's *Turkish company* owns the LLC rather than the founder personally, Art. 7 analysis becomes relevant, and the 10% tax-burden test is easily failed because a disregarded LLC pays no US entity-level tax.
- **Possible hybrid:** the US LLC collects through Stripe, and the founder's Turkish company invoices the LLC for software development and operations. That invoice could qualify for the KDV export exemption plus the 100% service-export deduction, subject to the 10% minimum CIT. It needs transfer-pricing support and a YMM opinion.

### Gaps
- IRS primary text (Form 5472 instructions; the IRC §6038A penalty) was not fetched.
- The official Delaware 2026 LLC tax amount was not confirmed ($300 vs. $400).
- No state-by-state taxability of VPN services specifically was found.
- The eCFR text of 31 CFR 1010.100(ff) and (ww) could not be fetched (redirect); thresholds come from the Federal Register, the FinCEN press release and secondary summaries.
- No FinCEN ruling on international airtime top-up resellers was found. State money-transmitter law and the CSBS model act were not researched.
- No official GİB özelge was found on how a Turkish resident individual should declare income from a single-member US LLC (pass-through vs. corporate characterization). The Turkish place-of-effective-management risk is not sourced.
- Turkish individual income tax brackets (2026) and the dividend withholding treatment of US LLC distributions were not sourced.
- The UK Ltd and Estonia options were dropped from scope per the user update.

---

## 5. KVKK and GDPR obligations, including VPN no-log claims and data retention

### Takeaway
No sources were retrieved specifically on KVKK or GDPR for VPN no-log policies in this research pass. The relevant framework is: KVKK (Law 6698) for a Turkish controller, including VERBİS registration subject to thresholds and the amended Art. 9 cross-border transfer rules (2024); GDPR Art. 3(2) if offering services to EU residents; and Law 5651 traffic-log obligations if the operator falls within Turkish access-, hosting- or VPN-provider definitions. A Turkish VPN operator that is authorized under the draft 5809 regime would likely face BTK logging and lawful-intercept duties incompatible with a "no-log" marketing claim.

### Cited Findings
- The April 2026 draft would require VPN providers to operate under **BTK authorization through a Turkish company with fully authorized representatives** — [Webtekno](https://www.webtekno.com/vpn-duzenlemeye-dair-yeni-detaylar-h215785.html). BTK-authorized operators are subject to BTK's network and information-security regulations; a 2026 board decision on authorization and security rules exists — [BTK board decision 71/2026 (PDF)](https://www.btk.gov.tr/uploads/boarddecisions/yetkilendirme-mevzuati-ve-sebeke-ve-bilgi-guvenligine-iliskin-duzenlemeler/71-2026-web.pdf). Its content was not read.
- İFÖD reports that BTK-linked DPI traffic manipulation targeting Proton connections has no legal basis and may breach Constitution Arts. 13 and 20 (privacy) — [İFÖD](https://ifade.org.tr/en/reports/engelliweb-2025/11-vpn-blockings/)
- Turkish data-localization and cross-border transfer analysis — [M.B. Kaya – Türkiye kişisel veri lokalizasyon (PDF)](https://mbkaya.com/hukuk/turkiye-kisisel-veri-lokalizasyon.pdf) (not read in detail)

### Inferences
- If the VPN is operated from a Turkish entity and becomes BTK-authorized, a strict "no-logs" claim is likely untenable. Turkish electronic-communications operators are generally subject to traffic-data retention and interception duties. This is unverified for VPNs specifically. Marketing a no-log claim that cannot be honoured would also be a consumer-protection and KVKK/GDPR transparency risk.
- For EU customers, GDPR applies via Art. 3(2). The operator would need an EU representative (Art. 27) unless exempt, a privacy policy, a DPA with server hosts, and lawful-basis analysis for account and payment data. If an MoR such as Paddle is used, the MoR is the controller for payment data.
- Hosting VPN servers and account databases outside Turkey reduces, but does not eliminate, Turkish compelled-disclosure exposure, because the founder and company are in Turkey.

### Gaps
- No primary KVKK sources were retrieved: the VERBİS threshold, the 2024 Art. 9 amendment (standard contracts and notification within 5 days), and KVKK fines for 2026 (revalued annually).
- No source was found on Law 5651 log-retention periods for access providers or "toplu kullanım sağlayıcı", or on whether a VPN would be classed as one under current law. Background knowledge says the 5651 regulation requires access providers to retain traffic data for 1–2 years; this is unverified here.
- The content of BTK board decision 71/2026 was not reviewed.
- No source was found on GDPR enforcement against VPN no-log claims.
