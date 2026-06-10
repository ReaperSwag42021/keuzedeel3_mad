# ⏱️ Tijdseenheden Converter

Een eenvoudige mobiele app waarmee je tijd omrekent tussen **seconden, minuten, uren en dagen**.
Gebouwd met Flutter & Dart voor het keuzedeel **Mobile Application Development (MAD)**.

![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=flat&logo=dart&logoColor=white)
![Platform](https://img.shields.io/badge/platform-Android-3DDC84?style=flat&logo=android&logoColor=white)
![Tests](https://img.shields.io/badge/tests-11%20passed-success?style=flat)
![Status](https://img.shields.io/badge/status-afgerond-brightgreen?style=flat)

---

## ✨ Functionaliteiten

- Omrekenen tussen **seconden, minuten, uren en dagen**
- Drie schermen: **Invoer**, **Overzicht** en **Instellingen**
- **Lichte en donkere modus** (light/dark mode) — de kleuren passen bij de modus: warm/geel in de lichte modus, donkerblauw in de donkere modus
- Ontwerp geïnspireerd op tijd (klok-iconen en een live klok)
- Invoer is bestand tegen fouten: letters of lege invoer laten de app niet crashen

### Extra's (bonus)
- 🕒 Een **live meelopende klok** met de huidige tijd
- 🎵 Een leuk weetje: hoeveel **liedjes** komt de tijd ongeveer overeen
- 🌍 **Wereldklokken** voor enkele steden

> De wereldklokken gebruiken vaste tijdverschillen ten opzichte van UTC en passen zich niet automatisch aan zomer-/wintertijd aan.

---

## 🖥️ Schermen

| Scherm | Wat je ziet |
| --- | --- |
| **Invoer** | Een waarde invoeren, de eenheid kiezen, en direct het resultaat in alle eenheden |
| **Overzicht** | Live klok, een tabel met de waarde in alle eenheden, een leuk weetje en wereldklokken |
| **Instellingen** | Schakelaar voor de donkere modus en informatie over de app |

---

## 🛠️ Gebouwd met

- [Flutter](https://flutter.dev/) (Material 3)
- [Dart](https://dart.dev/)
- [Android Studio](https://developer.android.com/studio)
- Geen externe packages — alleen de standaard Flutter- en Dart-bibliotheken

---

## 📂 Projectstructuur

```text
keuzedeel3_mad/
├── lib/
│   ├── main.dart                     # Start, thema (licht/donker) en navigatie
│   ├── converter.dart                # Reken-logica, los van de schermen (testbaar)
│   └── schermen/
│       ├── invoer_scherm.dart        # Scherm 1: waarde invoeren
│       ├── overzicht_scherm.dart     # Scherm 2: klok, tabel en wereldklokken
│       └── instellingen_scherm.dart  # Scherm 3: donkere modus
└── test/
    ├── converter_test.dart           # Tests voor de reken-logica
    └── widget_test.dart              # Tests voor de schermen
```

---

## 🚀 Aan de slag

**Vereisten:** een geïnstalleerde [Flutter SDK](https://docs.flutter.dev/get-started/install) en een emulator of telefoon.

```bash
# 1. Project clonen
git clone https://github.com/reaperswag42021/keuzedeel3_mad.git
cd keuzedeel3_mad

# 2. Packages ophalen
flutter pub get

# 3. App starten
flutter run
```

---

## 🧪 Tests draaien

De app heeft automatische tests voor de reken-logica en de schermen. Draai ze met:

```bash
flutter test
```

> **Let op:** voer de tests altijd uit met `flutter test` (of een Flutter-test-configuratie in je IDE).
> Een testbestand rechtstreeks met `dart` draaien werkt niet voor Flutter-tests.

Verwachte uitvoer:

```text
00:02 +11: All tests passed!
```

---

## 🧮 Hoe de omrekening werkt

Alle eenheden worden vergeleken via **seconden** als basis:

| Eenheid | In seconden |
| --- | --- |
| 1 seconde | 1 |
| 1 minuut | 60 |
| 1 uur | 3600 |
| 1 dag | 86400 |

Het omrekenen gebeurt in twee stappen:

1. Reken de waarde om naar seconden: `waarde × seconden-per-eenheid`
2. Reken de seconden om naar de doel-eenheid: `seconden ÷ seconden-per-eenheid`

**Voorbeeld:** 2 uur naar minuten → `2 × 3600 = 7200` seconden → `7200 ÷ 60 = 120` minuten.

---

## 📖 Context

Dit project is gemaakt als examenopdracht voor het keuzedeel **Mobile Application Development (K0497)** —
kerntaak D1-K1: *Realiseert (onderdelen van) een mobiele applicatie*. Het is opgezet op een beginnersniveau
in Flutter/Dart, met de nadruk op leesbare, eenvoudige code.

---

## 👤 Auteur

**Rik** — [ReaperSwag](https://reaperswag42021.github.io)
