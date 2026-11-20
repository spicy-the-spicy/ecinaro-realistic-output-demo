# ecinaro-realistic-output-demo

Gerçekten çekilmiş bir an hissi veren görsel prompt'ları üreten, sade bir Claude Code becerisi (skill). Sahne metninden ya da yüklenen bir görselden tek bir İngilizce prompt çıkarır. Sadece görsel içindir.

## Ne yapar

- iPhone varsayılanlı, elde çekilmiş kadraj kurar.
- Kaynağı belli, yönlü ve tutarlı ışıkla, hikayeye hizmet eden detaylarla prompt yazar.
- "8k", "ultra realistic", bokeh gibi boş sözcükleri yasaklar.

## Kurulum

`ecinaro-realistic-output-demo` klasörünü becerilerin bulunduğu dizine kopyala.

Claude Code için:

```
~/.claude/skills/ecinaro-realistic-output-demo/SKILL.md
```

## Kullanım

Şöyle istekler becerinin devreye girmesini sağlar:

- "gerçekçi çıktı, gece vardiyasındaki eczacı arka kapıda çay içiyor"
- "iPhone ile çekilmiş gibi bir mutfak sahnesi"
- "bu görseli candid bir prompt'a çevir" (görsel ekle)

## Dosyalar

| Dosya | Ne için |
|---|---|
| `SKILL.md` | Becerinin kendisi |
| `README.md` | Bu açıklama |
