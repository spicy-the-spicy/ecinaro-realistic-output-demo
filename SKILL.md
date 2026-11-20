---
name: ecinaro-realistic-output-demo
description: Gerçekten çekilmiş bir an hissi veren, basit ve hızlı görsel prompt'ları üretir (iPhone varsayılan). Sahne metninden ya da yüklenen görselden tek bir İngilizce prompt çıkarır. Sadece görsel, video ve ses yok. Tetikle gerçekçi çıktı, iPhone ile çekilmiş gibi, candid, AI gibi durmasın, UGC tarzı, günlük hayat fotoğrafı. Sinematik kadraj isteniyorsa kullanma.
---

# Ecinaro Realistic Output (demo)

Kurulu bir sinema karesi değil, gerçekten çekilmiş bir an üretir: biri cebinden telefonunu çıkarmış, o ışıkta, o mesafeden, o haliyle yakalamış. Fark estetikte değil, inandırıcılıkta.

Prompt'lar İngilizce, brief ve sorular Türkçe yazılır.

## Mod 1: metinden prompt'a

Dört kararı sırayla ver, sonra tek prompt yaz.

1. **An ve çeken kişi.** Sahnede ne oluyor, kim çekiyor (arkadaş, aile, yabancı, selfie, gözlemci)? Çeken kişi kadrajı belirler: özne hafif kayık, omuz ya da kol kadrajı kesebilir. Kadrajda bir "yanlış" bırak: kenarda yabancı biri, yarım kalmış bir obje.
2. **Kamera.** Kullanıcı belirtmediyse varsayılan iPhone ana kamera, 24mm eşdeğeri, elde, göğüs hizası. Çekim yüksekliğini ve mesafeyi yaz (portre 1-2 m, yemek 40 cm, sokak 3-5 m). Alan derinliği derindir: özne ve arka plan birlikte okunur.
3. **Işık.** Işık "güzel" olmasın, bir yerden gelsin. Ana kaynağı seç, adını, yönünü ve kalitesini (sert ya da yumuşak) yaz: pencere, lamba, ekran, far, buzdolabı ışığı. Gerçek sahnede ikinci bir kaynak ya da duvardan sıçrayan ışık olabilir, bu serbest. Kural şu: gölgeler ve karakterin üstündeki ışık, kadrajdaki kaynaklarla tutarlı olsun. Işığın rengini de yaz (sıcak ampulün yanında soğuk floresan gibi). Her yerden gelen gölgesiz stüdyo ışığı ve neon yok.
4. **Detay.** İnsanda en az 3, nesnede en az 2, ortamda en az 3 detay düşün. Her detay hikayeye hizmet etsin (gece vardiyasındaki kişinin kıyafeti buruşuk, elinde soğumuş çay vardır). Rastgele "ilginç" detay ekleme.

## Mod 2: görselden prompt'a

Kullanıcı görsel yüklerse sadece okunabilen katmanları çöz: kamera ve lens tahmini, ana ışık kaynağı ve yönü, insan ve nesne detayları, görüntüde zaten olan kusurlar (odak kaçması, kırpık özne). Sonra Mod 1'deki formüle göre yeniden kur. Okunmayan kategoriyi zorlama.

## Prompt formülü

Tek blok, 60-90 kelime, en fazla 110:

```
[device + lens + grip + height], [moment: who is doing what], [human details], [object details], [environment], [light: main source + direction + quality + colour, secondary or bounce light], [phone processing], [aspect ratio]
```

## Çıktı formatı

1. **SHOT BRIEF** (Türkçe, 2-3 satır): an, kamera ve nedeni, ana ışık, kilit detaylar.
2. **PROMPT** (İngilizce, tek blok).

Birden fazla kare istenirse her kare için ayrı prompt yaz, aynı cihaz ve aynı ışık ailesinde kal.

## Yasaklar

- "8k", "ultra realistic", "masterpiece", "hyper detailed", "photorealistic" gibi boş sözcükler yok. Gerçeklik somut detaydan, somut ışıktan ve somut cihazdan gelir.
- "flawless skin", "perfect face", "airbrushed", "glossy" yok. Ten gözenekli ve düzensiz tonlu olsun.
- "shallow depth of field", "bokeh", "blurred background" yok. Arka plan bulanıksa nedeni mesafe ya da tele lens olmalı.
- Sinema kamerası, anamorphic ve film stock dili yok.
- Kullanıcı istemedikçe okunur yazı, logo ve filigran yok.
- Em dash kullanma.

## Çıkıştan önce kontrol (sessizce uygula)

- Işığın bir kaynağı ve yönü var mı, gölgeler ve karakterin üstündeki ışık buna uyuyor mu?
- Kadrajda bir "yanlış" bırakıldı mı, arka plan fazla temiz mi?
- Cihaz, lens ve tutuş yazıldı mı?
- Prompt 110 kelimeyi geçti mi?
- Yasaklı sözcük kaldı mı?

## Örnek

Sahne: gece vardiyasındaki eczacı arka kapıda çay içiyor.

**SHOT BRIEF:** Arka sokakta bir iş arası. Çeken, kapıdan çıkan bir iş arkadaşı. iPhone ana kamera, göğüs hizası, çünkü selam verir gibi çekmiş. Ana ışık kapının üstündeki sıcak ampul, ikinci ışık açık kapıdan sızan soğuk floresan.

**PROMPT:**

```
Candid handheld iPhone photo, main camera 24mm equivalent, chest height. A tired night-shift pharmacist in her thirties steps out the back door to drink cold tea, creased white coat, hair clip slipping, faint sleep crease on her cheek, chipped nail polish. Paper cup with a torn tea bag string. Wet alley, stacked flattened boxes, a mop bucket, a half-open fire door. Warm bare bulb above the door as the main light, hard from the upper left, cool fluorescent spill from the open door bouncing on her coat. Slight HDR shadow lift, 4:5.
```
