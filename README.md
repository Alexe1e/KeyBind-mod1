# Keybind Map (Fabric, Minecraft Java 26.3)

Zeigt eine Tastatur (Layout wie die Logitech G512) und färbt jede Taste ein:

- grau = frei
- blau = genau ein Keybind
- orange = mehrere Keybinds auf derselben Taste (Konflikt)

Klick auf eine Taste (oder die Taste auf der echten Tastatur drücken) zeigt unten alle Keybinds, die sie benutzen. Maustasten sind in der unteren Reihe.

## Öffnen
- Im Spiel: **F8** (änderbar unter Steuerung > Tastenbelegung)
- Im Menü Steuerung > Tastenbelegung: Button **Keybind-Karte** oben links

## Bauen
Voraussetzung: **JDK 25** (Minecraft 26.x braucht Java 25).

    gradle wrapper --gradle-version 9.5.1    # einmalig, falls kein gradlew vorhanden
    ./gradlew build                          # Windows: gradlew.bat build

Die fertige Mod liegt danach in `build/libs/keybind-map-1.0.0.jar` (nicht die `-sources.jar`).
Zusammen mit Fabric API 0.163.0+26.3 in den `mods`-Ordner legen.
Zum Testen: `./gradlew runClient`.

## Hinweise
- Versionen: Fabric Loader 0.19.5, Loom 1.18-SNAPSHOT, Fabric API 0.163.0+26.3 (aus der offiziellen Fabric-26.3-Vorlage).
- Falls ein Compile-Fehler bei einem Methodennamen kommt: 26.x ändert Namen häufig (z. B. `extractRenderState`, `KeyMappingHelper`). Die Stellen sind klein und stehen in `KeybindMapScreen.java` und `KeybindMapClient.java`.
