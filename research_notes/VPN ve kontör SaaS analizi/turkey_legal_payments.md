# Turkey-based founder: legal, regulatory, payments and tax landscape for (a) a branded VPN subscription and (b) international mobile top-ups / digital gift cards (as of Nov 2026)

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

## 3. Payment processors: iyzico, PayTR, Param, Stripe (via a foreign entity), Paddle, Lemon Squeezy / Stripe Managed Payments, PayPal, and high-risk options

### Takeaway
For the **VPN**, Merchant-of-Record platforms are possible but not guaranteed. Paddle lists VPN/proxies as a "Restricted Category" requiring enhanced due diligence at Paddle's sole discretion. Stripe's restricted list does not name VPNs. For **gift cards and top-ups**, Paddle prohibits stored value and gift cards. Stripe classes gift cards, prepaid cards and third-party stored value as "Restricted", meaning extra due diligence and possible rejection. Lemon Squeezy bars anything Stripe restricts, plus "regulated services" including "cellular/communication". So the top-up and gift-card line realistically needs a Turkish PSP (iyzico or PayTR, with sector approval) or a high-risk acquirer, not a SaaS MoR.

### Cited Findings
**Paddle (MoR)**
- Paddle's AUP lists **"VPN and Proxies (Restricted Category)"**. Paddle runs enhanced due diligence on restricted offerings and will reach out for more information — [Paddle Help – What am I not allowed to sell](https://www.paddle.com/help/start/intro-to-paddle/what-am-i-not-allowed-to-sell-on-paddle)
- Virtual currency and stored value, **including gift cards and vouchers**, appear among Paddle's prohibited categories — [Paddle Help](https://paddle.com/help/start/intro-to-paddle/what-am-i-not-allowed-to-sell-on-paddle)
- Paddle's MSA lets it decide "in its absolute discretion" that a product falls outside the AUP or its risk tolerance — [Paddle Master Services Agreement](https://www.paddle.com/legal/terms)
- Fee: **5% + $0.50 per transaction** (third-party sources; not confirmed on Paddle's own page in this research) — [Unibee Paddle review 2026](https://unibee.dev/blog/paddle-review-features-pricing-pros-cons/); [MoR Finder](https://www.merchantofrecordfinder.com/providers/paddle)

**Lemon Squeezy / Stripe Managed Payments**
- Lemon Squeezy prohibits "any products restricted by our payment processing partners" (linking to Stripe's list). It also prohibits "regulated services such as" cellular/communication, banking/financing and currency exchange. VPN, gift cards and top-ups are not named explicitly; sellers are told to contact support if unsure — [Lemon Squeezy – Prohibited products](https://docs.lemonsqueezy.com/help/getting-started/prohibited-products)
- Lemon Squeezy fee: **5% + $0.50**, with surcharges for subscriptions, international payments and PayPal — [Freemius fees comparison](https://freemius.com/blog/payment-processing-fees/)
- Stripe acquired Lemon Squeezy in 2024 and launched **Stripe Managed Payments** (MoR, public preview). Sources conflict on price, from about 3.5% on top of Stripe processing to 5% + $0.50 — [MEAN CEO](https://blog.mean.ceo/stripe-vs-lemon-squeezy/); [Rework](https://resources.rework.com/tools/billing-revenue/paddle-vs-lemon-squeezy); [Stripe support – "Sold through Link, LLC"](https://support.stripe.com/questions/why-is-sold-through-link-llc-the-legal-entity-on-my-invoice-for-stripe-managed-payments-fees)

**Stripe (direct, via a foreign entity)**
- Stripe's Restricted Businesses list does **not mention VPN/proxy services**. Its only telecom item is the *prohibited* "telecommunications manipulation equipment, including jamming devices" — [Stripe Restricted Businesses](https://stripe.com/legal/restricted-businesses)
- Under "Nonfiat currency and stored value", Stripe lists **"Preloaded payment cards, gift cards, virtual credits"** and "sale of stored value or credits maintained, accepted, and issued by anyone other than the seller" as **Restricted**, meaning extra due diligence, may not be approved, and sometimes limited availability via sales. Mobile top-ups and airtime are not named — [Stripe Restricted Businesses](https://stripe.com/legal/restricted-businesses)
- Stripe does not onboard Turkish entities directly; this was not checked in this research (see Gaps). The usual route is a US LLC via Stripe Atlas.
- **Stripe Atlas costs:**
  - **$500 one-time**, covering Delaware filing and the first year of registered agent.
  - **$100/yr** registered agent after year 1.
  - Delaware LLC annual tax of **$300**, with one source claiming **$400 from 1 Jan 2026** (conflicting).
  - For a C-corp, franchise tax of at least **$175 + $50** annual report.
  - Sources: [Rho – Stripe Atlas review](https://www.rho.co/blog/stripe-atlas-review); [Stripe – Delaware LLC costs](https://stripe.com/resources/more/how-much-does-it-cost-to-form-an-llc-in-delaware-fees-and-other-costs); [AgentDeals – Forming a US company in 2026](https://agentdeals.dev/company-formation-pricing-2026)

**Turkish PSPs (iyzico, PayTR, Param)**
- **TCMB 2026 maximum merchant commission caps** reported in a secondary source:
  - domestic debit card **1.04%**
  - **foreign-issued cards 1.90%**
  - single-payment TL credit card **3.56%**
  - Source: [Karekod.org – Sanal POS komisyon oranları 2026](https://www.karekod.org/blog/sanal-pos-komisyon-oranlari/)
- **PayTR:** from **2.19%** for new merchants (7-day settlement). The final rate depends on volume, sector and card type. A figure of 3.49% + $0.30 for foreign cards appears on a low-reliability page — [Karekod.org](https://www.karekod.org/blog/sanal-pos-komisyon-oranlari/); [ikas – POS ücretleri](https://ikas.com/tr/blog/pos-ucretleri-ve-giderleri)
- **iyzico:** no public list price; rates appear in the merchant panel. Third-party estimates are about 2.99%+. Paynet merged into iyzico, and services run under the iyzico brand from 1 Jan 2026 — [Karekod.org](https://www.karekod.org/blog/sanal-pos-komisyon-oranlari/); [KobiTime](https://kobitime.com/sanal-pos-ucretleri-ve-sanal-pos-firmalari-2026/)

**High-risk merchant accounts**
- "Store of digital value (vouchers, e-wallets, mobile money and e-money)" is classed as high risk. High-risk accounts carry stricter terms, such as reserves and higher fees — [Peach Payments](https://support.peachpayments.com/support/solutions/articles/47001276655-capitec-pay-high-risk-industry); [Chargebacks911 – high-risk merchant accounts](https://chargebacks911.com/high-risk-merchant-accounts/); [PayPro Global – high-risk category](https://payproglobal.com/answers/what-is-high-risk-merchant-category/)

### Inferences
- **VPN, international customers:** apply to Paddle first. It is a full MoR that handles global VAT/GST, and VPN is restricted rather than banned, but approval is discretionary. As a fallback, use Stripe (via a US LLC) directly, which does not list VPN as restricted, plus a VAT/OSS registration or a tax engine. Stripe Managed Payments is a third option, with policy for VPNs to be confirmed.
- **VPN, Turkish customers:** a Turkish PSP such as iyzico or PayTR would require a Turkish company and would expose the business to the BTK risks in Section 1. PSPs may also refuse VPN merchants once the draft law passes. This was not verified.
- **Top-ups and gift cards:** Paddle is out because these are prohibited. Lemon Squeezy is likely out (Stripe-restricted, plus "cellular/communication"). Stripe is possible only after restricted-business review. The realistic options are a Turkish PSP with sector approval, a crypto or alternative-payment processor, or a specialist high-risk acquirer. Expect rolling reserves and fees well above the TCMB caps quoted for normal merchants.
- **Foreign-card economics in Turkey:** the TCMB cap of 1.90% for foreign-issued cards makes iyzico or PayTR cheaper than any MoR at 5% + $0.50, if the Turkish entity can handle foreign VAT itself.

### Gaps
- **Param:** no pricing or policy found.
- **PayPal:** not researched. Background knowledge (unverified here) is that PayPal stopped domestic operations in Turkey in 2016 after BDDK licence refusal, so a Turkish-resident account cannot receive payments. A foreign-entity PayPal account would be the only route. This needs confirmation.
- Whether Stripe currently supports Turkey-incorporated accounts was not checked; background knowledge says it does not.
- iyzico's and PayTR's prohibited-sector lists (VPN, gift cards, e-pin, top-ups) were not retrieved.
- Paddle's VPN approval criteria and Stripe Managed Payments' VPN policy were not found.
- No specific high-risk acquirer names or fees for gift cards and top-ups were found.

---

## 4. Company structure and Turkish tax: existing Turkish company vs. US LLC / UK Ltd / Estonia; KDV export exemption; corporate tax; the service-export deduction; e-fatura/e-arşiv

### Takeaway
A Turkish company exporting a service to foreign customers can generally apply the **KDV exemption (KDVK 11/1-a, 12/2)** when the customer is abroad and benefits from the service abroad. Since **1 Jan 2026** the **service-export income deduction is 100%** (Presidential Decision 11257, RG 30.04.2026, previously 80% under Law 7524), with **software** among the listed services. It applies only if earnings are **brought to Turkey** by the tax-return deadline. The **10% domestic minimum corporate tax** may still apply to a company. A foreign LLC owned by a Turkish resident does not escape Turkish taxation, and CFC/residence rules apply. Whether a VPN subscription or top-up resale counts as qualifying "software / data processing" export is uncertain. [NEEDS PROFESSIONAL ADVICE — YMM]

### Cited Findings
**Service-export income deduction (KVK 10/1-ğ; GVK 89/1-13)**
- Law 7524 raised the deduction from 50% to 80% — [TÜRMOB e-library](https://turmob.org.tr/ekutuphane/Read/31b9a8e3-c6b1-4f5f-9ff6-1d2149cf7e0f); [PwC – Recep Bıyık column](https://www.pwc.com.tr/tr/medya/kose-yazilari/recep-biyik/hizmet-ihracindan-elde-edilen-kazanclarda-indirim.html)
- **Presidential Decision No. 11257** (RG 30.04.2026, no. 33239) raised it to **100%** for tax periods starting on or after **1 Jan 2026** — [KPMG Vergi](https://kpmgvergi.com/blog/munhasir-hizmetlere-saglanan-indirim-orani-100-e-cikarildi/1391); [PwC Türkiye bulletin 2026](https://www.pwc.com.tr/tr/Hizmetlerimiz/vergi/vergi-bultenleri/2026/yurt-disi-istirak-kazanci-istisnasi-ve-hizmet-ihracinda-indirim-uygulamasi-hakkinda-cumhurbaskani-karari.pdf)
- **Qualifying services** include architecture, engineering, design, **software**, medical reporting, bookkeeping, call centres, product testing, certification, **data storage, processing and analysis**, and certain vocational training, education and health services — [KPMG Vergi](https://kpmgvergi.com/blog/munhasir-hizmetlere-saglanan-indirim-orani-100-e-cikarildi/1391)
- **Conditions** (all from [KPMG Vergi](https://kpmgvergi.com/blog/munhasir-hizmetlere-saglanan-indirim-orani-100-e-cikarildi/1391)):
  - The service is provided from Turkey to non-residents.
  - It is used **exclusively abroad** ("münhasıran yurt dışında yararlanılması").
  - **All** earnings are transferred to Turkey by the CIT return deadline; even a small untransferred portion can block the full deduction.
  - The deduction must be shown on the return, and unused amounts cannot be carried forward.
- **Domestic minimum CIT:** the deduction is not deductible from the 10% *yurt içi asgari kurumlar vergisi* base, so a company may still owe **10% minimum CIT**. Individuals (GVK 89) can reach zero — [KPMG Vergi](https://kpmgvergi.com/blog/munhasir-hizmetlere-saglanan-indirim-orani-100-e-cikarildi/1391); [Alomaliye, 17 May 2026 – hizmet ihracatı, asgari KV, KDV istisnası](https://www.alomaliye.com/2026/05/17/hizmet-ihracati-kazanc-ve-kurumlar-vergisi-indirimi-asgari-kurumlar-vergisi-ve-kdv-istisnasi/)
- Commentary notes interpretive problems, including the "münhasıran" (exclusively-abroad) test and procedural certification risk — [Ekonomi Gazetesi – "%100 indirim sıra münhasıran çıkmazında"](https://www.ekonomigazetesi.com/kose-yazisi/hizmet-ihracatinda-100-indirim-sira-munhasiran-cikmazinda-78578); [Ekonomi Gazetesi – "Hizmet ihracatında şirketleşmemeli mi?"](https://www.ekonomigazetesi.com/kose-yazisi/hizmet-ihracatinda-sirketlesmemeli-mi-82057)

**KDV (VAT) on exported services**
- Legal basis: **KDVK 11/1-a and 12/2**. The service must be performed for a customer abroad **and** benefited from abroad. A foreign customer alone is not enough. If the benefit occurs in Turkey, no exemption applies even if invoiced to a foreign firm and paid in FX — [Alomaliye – hizmet ifasında Türkiye'de faydalanma kriteri](https://www.alomaliye.com/2014/09/22/hizmet-ifasinda-turkiyede-faydalanmafaydalanmama-kriteri/); [Alomaliye – yurt dışında mukim firmaya verilen hizmet](https://alomaliye.com/2017/04/21/yurt-disinda-mukim-firmaya-verilen-hizmetin-kdv-karsisindaki-durumu/)
- A GİB özelge (private ruling) accepted design, software and consultancy services to a foreign customer used abroad as exempt under 11/1-a. Video streaming to foreign viewers was also treated as potentially exempt — [Alomaliye 2024 – tasarım/yazılım/danışmanlık hizmetinin KDV ve KVK karşısındaki durumu](https://www.alomaliye.com/2024/07/30/yurt-disinda-mukim-firmaya-verilen-tasarim-yazilim-ve-danismanlik-hizmetinin-kdv-ve-kvk-karsisindaki-durumu/); [Alomaliye – YouTube aracılığıyla hizmet ihracatı](https://www.alomaliye.com/2024/10/09/hizmet-ihracatindan-youtube-araciligi-ile-turkiyede-faydalanilma/amp/)
- Related GİB özelgeler: [Lexpera özelge 790034](https://www.lexpera.com.tr/mevzuat/ozelgeler/39044742-130-ozelge-790034-sayili-ozelge-1); [Lexpera özelge 222571](https://www.lexpera.com.tr/mevzuat/ozelgeler/39044742-130-ozelge-222571-sayili-ozelge-1)

**Foreign entity (US LLC via Atlas)**
- Atlas costs $500 one-time plus $100/yr registered agent, with a Delaware annual tax of $300–$400 (sources conflict; see Section 3) — [Rho](https://www.rho.co/blog/stripe-atlas-review); [Stripe](https://stripe.com/resources/more/how-much-does-it-cost-to-form-an-llc-in-delaware-fees-and-other-costs); [AgentDeals](https://agentdeals.dev/company-formation-pricing-2026)

### Inferences
- **VPN subscription to foreign consumers:** a strong argument exists for the KDV 11/1-a exemption, since the customer is abroad and the benefit is abroad. Whether a VPN counts as qualifying "software / data processing" for the 100% income deduction is untested in the sources found. The B2C, consumer-facing nature and the "münhasıran" test are risk points. [YMM opinion / özelge application recommended]
- **Top-up and gift-card resale:** this is trading in third-party digital goods or services, not a listed service type, so the 100% service-export deduction **likely does not apply**. Ordinary 25% CIT on margin would apply. The KDV treatment of airtime and vouchers sold to foreigners is complex (voucher vs. service, place of supply) and unresearched.
- **Foreign LLC route:** it simplifies Stripe, PayPal and MoR onboarding. But a Turkey-resident owner likely triggers Turkish tax on the LLC's income under KVK Art. 7 CFC rules, or the place-of-effective-management test (kanuni veya iş merkezi). The 100% deduction requires earnings to land *in Turkey* through a Turkish taxpayer anyway. A common hybrid is a foreign entity for payment collection plus the Turkish company invoicing the foreign entity for software or development services. That structure needs transfer-pricing review. [NEEDS PROFESSIONAL ADVICE]
- **Foreign consumer VAT** (EU OSS, UK VAT and others) applies if selling B2C directly rather than through an MoR. This is a key reason to prefer Paddle or Lemon Squeezy for the VPN.

### Gaps
- No primary text of Presidential Decision 11257 or of the Kurumlar Vergisi Genel Tebliği draft amendment (Alomaliye June 2026 draft) was read. The "bring earnings to Turkey" rule is from KPMG's summary.
- **e-fatura / e-arşiv:** no source was retrieved on 2026 thresholds or on the e-arşiv rules for B2C sales to foreign individuals; generally an e-arşiv fatura is issued with "yurt dışı" customer details. GİB guidance needs checking.
- **Kurumlar vergisi:** 25% general rate (background, not sourced in this research).
- **Turkish digital service tax (DST)** and "foreign digital service providers" (KDVK 9/2 reverse-charge, and foreign providers registering for KDV) were not researched.
- **UK Ltd and Estonia e-Residency costs:** not researched. Background, unverified: UK Companies House incorporation is about £50 (raised in 2024); Estonia e-Residency is about €100–150 plus a €265 state fee. Both are also subject to Turkish CFC and management concerns.
- **Turkish company running costs** (mali müşavir monthly fees, e-fatura integrator costs, Ltd/AŞ capital minimums after 2024) were not sourced.

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
