# Tijdseenheden Converter - README

Dit zijn de bronbestanden voor de Flutter-app.

## Hoe gebruik ik deze bestanden?

1. Maak in Android Studio een nieuw Flutter-project aan (bijvoorbeeld via
   New > New Flutter Project). Noem het project bij voorkeur `tijd_converter`.
2. Vervang de inhoud van de map `lib/` door de `lib/` uit deze map.
3. Kopieer ook de map `test/` naar je project.
4. Run de app met de groene play-knop (of `flutter run`).
5. Run de tests met `flutter test`.

## Heet jouw project niet 'tijd_converter'?

Open dan `test/converter_test.dart` en pas in deze regel de naam aan naar de
naam die bovenaan in `pubspec.yaml` staat (achter `name:`):

    import 'package:tijd_converter/converter.dart';

## Bestanden

- `lib/main.dart`              - start van de app, thema en navigatie onderaan
- `lib/converter.dart`         - de reken-logica (apart, zodat het testbaar is)
- `lib/schermen/invoer_scherm.dart`        - scherm 1: waarde invoeren
- `lib/schermen/overzicht_scherm.dart`     - scherm 2: overzicht + live klok
- `lib/schermen/instellingen_scherm.dart`  - scherm 3: donkere modus
- `test/converter_test.dart`   - tests voor de reken-logica

Er zijn geen extra packages nodig; alles werkt met de standaard Flutter-installatie.