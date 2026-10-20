# Stationary-String Çerçevesi (P1) — Yayın Paketi

> **English:** [README.md](./README.md)

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](LICENSE)

**P1: Stationary-String Çerçevesi — Galaktik, Hadronik ve Laboratuvar Fenomenolojisi için Birleşik FENE-P Modeli (Derece-Defteri, Kırılganlık Haritası ve Kendi Hatalarımızın Adli Denetimi)**

Yazar: Fahri Meral · Tarih: 20 Ekim 2026 · Sürüm: v1 (P1)

> **Durum:** Yayımlanmamış ön-baskı (v1). Hakem denetiminden geçmemiştir. *Zenodo DOI'si yüklemeyi bekliyor.*

## Bu makale ne (ve ne değil)
Bu bir **yöntem makalesidir**: çerçevenin kendi iddialarını kendi
puanlamasına sunar. **Yang–Mills kütle aralığının çözüldüğü** ya da
**karanlık maddenin ikame edildiği** iddiaları kapsam dışıdır ve
makalenin 1. bölümünde açıkça belirtilmiştir.

## İçerik

| Dosya | Açıklama |
|---|---|
| `paper/stationary_strings_framework_p1.tex` | Ana makale, Türkçe (Tablo 1, 7 bölüm) |
| `paper/stationary_strings_framework_p1_EN.tex` | İngilizce sürüm |
| `paper/ledger.json` | Makine-okunur derece-defteri (17 satır) |
| `CITATION.cff` | Atıf kaydı |
| `LICENSE` | CC BY 4.0 |

## Ana bulgular

- **Derece-defteri (Tablo 1):** 17 yayımlanmış karşılaştırmanın her biri için
  gözlenebilir, literatür değeri, model değeri, girişen serbest parametreler,
  bu parametrelerin o veriye fit edilip edilmediği ve kırılganlık ölçümü.
  Sınıf dağılımı: **2 fit, 2 fit-benzeri, 10 transfer, 2 gerçek, 1 yapısal**.
  Korelasyonlu satırlar gruplandığında **8 bağımsız gözlem grubu / 9 serbest
  derece → kanıt oranı 0.889**.
- **Kırılganlık haritası:** glueball ortalaması (T33), $\mathcal{C}_{\mathrm{univ}}$
  kilidinin yalnızca %1'lik kaymasıyla **%27.8** oynuyor; %1.56'lık uyum
  dolayısıyla **kararlı değildir**. Charmonium (%0.05) ve Vela (%0.17) pratikte kararlıdır.
- **Yalnızca iki gerçek öngörü** var (T22 Ps bant bütçesi, T37 Na-22 bant oranı),
  ikisi de laboratuvar tarafında; kalan on beş satır fit ya da transferdir.
  Tablo serinin en güçlü ve en zayıf yanlarını aynı anda gösterir.
- **Adli denetim:** bu çalışma içinde bulunup düzeltilen sekiz hata sınıfı
  (hatalı öz-eşlenir uzantı, totolojik Temple–Kato alt sınırı, ters etiketlenmiş
  kaynak formülleri, *hayalet parametre* niteliğindeki literatür bandı,
  $H_0$ bağımlılığı, sapma sonrası eklenen çarpanlar, kendi kaynağıyla
  çelişen model, sabit kopyalanan "bağımsız" denetimler).

## Sayısal yeniden-üretim

Defter bir tablo değil bir programdır: her satırı yeniden hesaplar,
çözücüyle çapraz kontrol eder ve makaledeki tabloyu doğrular.

```bash
git clone https://github.com/fahrim/stationary-strings-v
pip install numpy scipy matplotlib
python duran_sicimler_sim/solver_engine.py   # T1–T37 (38/38 PASS)
python duran_sicimler_sim/ledger.py          # defter + capraz kontrol (1e-9) + tablo kontrolu
python duran_sicimler_sim/mini_check_audit.py # bagimsiz seri denetimi (9/9 PASS)
```

Makaledeki tablo yeniden hesaplanan değerlerden saptığında \texttt{ledger.py}
uyuşmayan satırları listeler.

## Atıf

```bibtex
@misc{meral2026stationarystringsP1,
  author = {Fahri Meral},
  title  = {Stationary-String Çerçevesi: Galaktik, Hadronik ve Laboratuvar Fenomenolojisi için Birleşik FENE-P Modeli},
  year   = {2026},
  url    = {https://github.com/fahrim/grand-proof-p1}
}
```

Ayrıca bkz. `CITATION.cff`.

## İlgili çalışmalar

- `stationary-strings-i` … `stationary-strings-x` — Teoremler I–X (ana seri).
- `grand-proof-i` / `grand-proof-ii` / `grand-proof-iii` — üç uygulama makalesi;
  her biri bu çalışmanın derece-defteri tarafından denetlenir.

## Lisans

CC BY 4.0 — bkz. `LICENSE`. İçerik hakem denetiminden geçmemiştir.
