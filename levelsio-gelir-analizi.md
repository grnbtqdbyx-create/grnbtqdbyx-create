# Pieter Levels (@levelsio) Gelir Analizi — iOS mu, SaaS mı?

> Derinlemesine araştırma raporu · Tarih: 2026-06-14
> Yöntem: 5 paralel web araştırma kolu + çapraz doğrulama. Levels'in resmi
> sayfaları (x.com, levels.io, open-startup panoları) otomatik erişime kapalı
> olduğundan rakamlar arama sonucu snippet'leri ve ikincil kaynaklardan derlendi.

## Kısa cevap

Parasının ezici çoğunluğu **web tabanlı SaaS** ürünlerinden geliyor — iOS native
uygulamalardan değil. Levels bilinçli olarak "web-first" çalışır: tüm ürünleri tek
bir sunucuda **PHP + jQuery + SQLite** ile yazılmış, modern framework (React/Next/Swift)
kullanmaz. Baskın iş modeli **abonelik SaaS**'tır (özellikle Photo AI).

## Ürün bazında gelir ve iş modeli

| Ürün | İş Modeli | Aylık Gelir (MRR) | Platform |
|------|-----------|-------------------|----------|
| **PhotoAI.com** | SaaS abonelik ($39/$99/$299) | ~$150K (Eyl 2025, Levels'in kendi açıklaması) | Web SaaS (+ kapatılmış iOS app) |
| **NomadList / Nomads.com** | Abonelik + ömür boyu üyelik | ~$60K (2024, belirsiz) | Web (2017'de iOS app vardı) |
| **RemoteOK.com** | İş ilanı marketplace (işveren öder) + reklam | ~$35–40K (~$3.4M/yıl 2024) | Sadece web |
| **InteriorAI.com** | SaaS abonelik (~$29–299) | ~$35–45K (düşüşte) | Web SaaS |
| **fly.pieter.com** | Oyun içi reklam/sponsorluk | ~$87K zirve (Mart 2025, geçici) | Web (tarayıcı oyunu) |
| **MAKE kitabı** | Tek seferlik dijital satış (~$29) | ~$2K/ay (kümülatif ~$880K) | Web (PDF/ePub) |
| **LEVELS II** | Ücretsiz + uygulama içi satın alma (reklam kaldırma) | Açıklanmamış (hobi) | Native iOS |
| **Hoodmaps / küçük projeler** | Monetize edilmemiş | ~$0 | Web |

## Hangi model baskın?

1. **SaaS abonelik = ana motor.** Photo AI tek başına gelirinin ~%70'ini oluşturuyor.
2. **Marketplace/reklam = ikincil ama önemli.** RemoteOK (işveren ilan ücreti) ve
   fly.pieter.com (oyun içi sponsorluk).
3. **Tek seferlik satış = küçük.** MAKE kitabı 7 yılda ~$880K kümülatif.
4. **Native iOS = ihmal edilebilir.** Photo AI iOS (Oca 2024, ~$1.330/ay, kapatıldı)
   ve LEVELS II (2048 tarzı hobi oyun, geliri açıklanmamış). Para web'de.

## İş geliri vs. yatırım geliri

Levels'in ~$120K/ay ek geliri **pasif yatırım getirisi** (çoğunlukla ETF'ler) —
operasyonel iş geliri değil; ürün MRR'larına eklenmemeli. Toplam aktif iş geliri
~$3M/yıl civarında (Lex Fridman Podcast #440, Ağu 2024), sıfır çalışanla.

## Sonuç

| Soru | Cevap |
|------|-------|
| iOS app mı, SaaS mı? | **SaaS / web app** (ezici çoğunluk) |
| Baskın iş modeli | **Abonelik SaaS** (özellikle Photo AI) |
| Native iOS rolü | Marjinal/hobi; denendi ve büyük ölçüde terk edildi |
| Teknik felsefe | Tek sunucu, PHP+jQuery+SQLite, framework yok, "hızlı ship et" |
| En büyük ürün | Photo AI (~$150K/ay, gelirinin ~%70'i) |

## Güvenilirlik notları

- **Güçlü (Levels'in kendi tweetleri):** Photo AI $150K MRR/%87 marj (Eyl 2025),
  Photo AI iOS ilk ay $1.330 (Oca 2024), InteriorAI $45K (Mar 2024), teknik yığın,
  ETF $120K/ay, fly.pieter.com kademeli rakamlar.
- **Zayıf/belirsiz:** NomadList güncel MRR, InteriorAI güncel rakamı,
  fly.pieter.com $87K'sının kalıcılığı (viral anlık zirve), $202K/ay ETF iddiası.
- Resmi "open startup" panoları (nomads.com/open, remoteok.com/open) en güncel
  rakamlar için elle kontrol edilmeli (botlara kapalı).

## Kaynaklar

- Photo AI $150K MRR (Eyl 2025): https://x.com/levelsio/status/1970858876212756506
- Photo AI iOS ilk ay $1.330 (Oca 2024): https://x.com/levelsio/status/1748018428466647298
- Photo AI FAQ — iOS app kapatıldı: https://photoai.com/faq
- InteriorAI $45K MRR (Mar 2024): https://x.com/levelsio/status/1773443837320380759
- ETF portföyü $120K/ay (Oca 2024): https://x.com/levelsio/status/1748713482692759647
- fly.pieter.com $87K MRR / $1M ARR (Mar 2025): https://x.com/levelsio/status/1899596115210891751
- fly.pieter.com $67K (13 gün): https://x.com/levelsio/status/1897784027186446820
- fly.pieter.com $38K (10 gün): https://x.com/levelsio/status/1896690611257844116
- 2018 gelir dökümü (MAKE $1.960, Hoodmaps $0): https://x.com/levelsio/status/968027544103473152
- RemoteOK gelir verisi (Latka): https://getlatka.com/companies/remote-ok
- NomadList gelir verisi (Latka): https://getlatka.com/companies/nomad-list
- Lex Fridman Podcast #440: https://lexfridman.com/pieter-levels/
- PPC.land — Photo AI $132K analizi: https://ppc.land/how-one-photo-ai-app-generates-132k-monthly-after-70-failed-startups/
- LEVELS II (native iOS): https://apps.apple.com/us/app/levels-ii/id6458190333
- Geliştirici sayfası: https://apps.apple.com/us/developer/levelsio/id1713575398
