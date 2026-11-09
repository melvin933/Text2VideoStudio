# Text2Video Studio – Android-Projekt (Version 3.1)

Dieses Paket enthält ein Android-Studio-Projekt, das die bestehende Text2Video-Studio-Web-App in einer Android-WebView startet. Es ist ein installierbarer-App-Projektstand, aber **noch keine fertig gebaute APK**.

## Öffnen und APK bauen
1. ZIP entpacken.
2. Android Studio öffnen und den entpackten Ordner `Text2VideoStudioAndroid` als Projekt öffnen.
3. Gradle-Synchronisierung abwarten (Android Studio benötigt Internet für die Android-Gradle-Plugins und das SDK).
4. Menü **Build > Build Bundle(s) / APK(s) > Build APK(s)** wählen.
5. Die erzeugte APK liegt normalerweise unter `app/build/outputs/apk/debug/app-debug.apk`.

## Was enthalten ist
- Native Android-Hülle mit App-Symbol-Eintrag/Launcher-Aktivität.
- Lokale HTML-App im App-Paket; kein Webhosting nötig.
- Datei-Auswahl zum Hinzufügen eigener Szenenbilder und Audiodateien.
- Szenenaufteilung, feste Figurenbeschreibung, Bild-Prompt-Erstellung, Geräte-Sprachausgabe, Zoom-Bewegung und WebM-Export aus Version 3.1.

## Ehrliche Grenzen
- Dieses Projekt wurde hier nicht mit Android SDK/Gradle zu einer APK kompiliert oder auf einem echten Gerät getestet.
- Die automatische Bilderzeugung ist integriert, nutzt aber AI Horde mit freiwilligen Rechnern. Anonyme Aufträge haben niedrige Priorität; Wartezeiten, Fehlversuche und Änderungen an der kostenlosen Verfügbarkeit sind möglich. Für die erste Probe nur 1–2 Szenen erzeugen.
- Die Bildgröße ist auf 512 × 512 begrenzt. Das Videoformat kann Hochkant sein, aber die KI-Bilder werden quadratisch erzeugt und beim Filmexport zugeschnitten.
- Die wiederholte Figurenbeschreibung kann helfen, garantiert aber keine identische Figur über mehrere Bilder hinweg.
- Eine echte KI-Bilderzeugung braucht einen Bilddienst. Viele Dienste verlangen ein Konto, einen API-Schlüssel oder Guthaben. Einen geheimen API-Schlüssel sollte man nicht fest in eine APK einbauen.
- Echte KI-Videoanimation und garantierte Figurenidentität sind nicht enthalten.
- Der Videoexport ist WebM. MP4-Export ist noch nicht implementiert.
- Die Browser-Sprachausgabe liest Text vor, wird aber nicht automatisch als Tonspur in den Film gemischt. Für Ton im Export kann man Audiodateien pro Szene hochladen.

## Technischer Hinweis
Die App lädt `file:///android_asset/index.html` lokal. Die WebView erlaubt die Auswahl von Bild- und Audiodateien über den Android-Dateiauswahldialog.


## Automatische KI-Bilder
In der Szenenansicht auf **„Alle fehlenden Szenenbilder erzeugen“** tippen. Die App erstellt die Bilder nacheinander über AI Horde. Die anonyme Nutzung ist kostenlos möglich, aber nicht priorisiert; bei hoher Auslastung kann es lange dauern. Die App bricht einen einzelnen Auftrag nach 10 Minuten ab. Bereits erzeugte Bilder bleiben erhalten. Für größere Projekte empfiehlt sich ein eigener AI-Horde-Account mit persönlichem Schlüssel; ein Schlüssel ist in dieser App-Version bewusst nicht fest eingebaut.

Datenschutz: Die Szenentexte und Figurenbeschreibung werden an AI Horde übermittelt, damit die Bilder erzeugt werden können. Keine sensiblen oder privaten Geschichteninhalte senden, wenn du sie nicht an diesen externen Dienst weitergeben möchtest.
