# APK direkt über GitHub Actions bauen (nur mit dem Handy)

1. Erstelle unter https://github.com/signup ein kostenloses GitHub-Konto und bestätige deine E-Mail-Adresse.
2. Öffne GitHub im Browser und melde dich an.
3. Erstelle ein neues Repository. Name: `Text2VideoStudio`. Sichtbarkeit: `Private`.
4. Lade den Inhalt dieses Projektordners in das Repository hoch. Wichtig: Lade die Dateien und Ordner IN `Text2VideoStudioAndroid` hoch, nicht den äußeren Ordner als zusätzliche Ebene. Die Datei `settings.gradle` muss direkt im Hauptverzeichnis des Repositorys liegen.
5. Öffne im Repository den Reiter **Actions**. Der Workflow **Build Android APK** sollte starten. Falls nicht: Workflow öffnen und **Run workflow** wählen.
6. Wenn der Lauf erfolgreich ist, öffne den abgeschlossenen Lauf und lade unter **Artifacts** die Datei `Text2VideoStudio-debug-apk` herunter.
7. ZIP-Datei entpacken und `app-debug.apk` auf dem Handy öffnen. Android kann nach Erlaubnis zum Installieren aus dieser Quelle fragen.

Hinweise:
- Der GitHub-Workflow ist vorbereitet, aber der Build wurde hier nicht auf GitHub ausgeführt. Ein erfolgreicher APK-Build ist daher noch nicht bestätigt.
- Repository privat lassen. Teile niemals dein GitHub-Passwort oder persönliche Zugriffstokens im Chat.
- Die APK ist eine Debug-Version zum Testen, keine veröffentlichungsfertige Play-Store-Version.
