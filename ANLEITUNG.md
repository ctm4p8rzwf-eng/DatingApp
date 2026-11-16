# Todate auf deinem iPhone

Dies ist eine installierbare Webversion, keine App-Store-App. Sie benötigt für den ersten Aufruf und erneutes Laden Internet; Offline-Start ist nicht zugesichert. Es gibt kein E-Mail-Konto, keine Cloud-Synchronisierung und keine echte Folgen-Funktion.

## GitHub Pages – vom Computer aus
1. Entpacke Todate-Web.zip.
2. Melde dich auf github.com an. Öffne dein Repository DatingApp oder erstelle ein neues öffentliches Repository, z. B. todate. GitHub Pages für öffentliche Repositories ist im kostenlosen GitHub-Angebot verfügbar; private Repositories können einen passenden Tarif erfordern.
3. Wähle „Add file → Upload files“. Bei einem leeren Repository nutze den Link „uploading an existing file“. Lade die Dateien AUS dem entpackten Ordner hoch: index.html, manifest.webmanifest, icon.svg, icon-180.png und icon-512.png. index.html muss ganz oben liegen, nicht in einem Unterordner. Die ZIP-Datei selbst nicht hochladen.
4. Klicke „Commit changes“. Dadurch entsteht bei einem leeren Repository der erste Branch (üblicherweise main).
5. Öffne „Settings → Pages“. Unter „Build and deployment“: Source „Deploy from a branch“, Branch „main“, Ordner „/(root)“, dann „Save“.
6. Warte auf die fertige Bereitstellung. Unter Settings → Pages findest du den Link. Er lautet normalerweise https://DEIN-GITHUB-NAME.github.io/REPOSITORY-NAME/ . Verwende den dort tatsächlich angezeigten Link.

## iPhone
1. Öffne diesen Link in Safari.
2. Tippe auf Teilen → „Zum Home-Bildschirm“. Je nach iOS-Version gegebenenfalls „Als Web-App öffnen“ einschalten. Name: Todate; dann Hinzufügen.
3. Öffne Todate über das neue Symbol. Richte erst hier dein lokales Passwort ein (mindestens 12 Zeichen). Safari und die installierte Web-App können getrennte Speicher haben.
4. Bestätigte Einträge werden automatisch lokal gespeichert. Zusätzlich gibt es „Speichern“. Warte vor dem Schließen auf „Auf diesem Gerät gespeichert“. Unbestätigte Formulare sind keine gespeicherten Einträge.
5. „Sperren“ speichert zunächst und sperrt dann. Nach Neuladen ist das Passwort erneut erforderlich. Im Hintergrund wird nicht automatisch gesperrt: auf gemeinsam genutzten Geräten ausdrücklich sperren.

## Deine Daten
Die Website und ihr Code sind öffentlich, deine Tagebucheinträge werden vom Anwendungscode nicht an GitHub gesendet. GitHub erhält technisch notwendige Aufrufdaten wie bei anderen gehosteten Websites. Keine Werbung, Analyse- oder Drittanbieter-Schriften eingebunden.

Texte und Bilder werden zusammen in einem AES-GCM-verschlüsselten Datensatz in IndexedDB gespeichert. Der Schlüssel wird über Web Crypto PBKDF2/SHA-256 mit zufälligem Salt und 600.000 Iterationen aus dem Passwort abgeleitet. Der Schlüssel wird nicht dauerhaft gespeichert. Kein unabhängiger Sicherheitsaudit; kein Versprechen, gegen kompromittierte Geräte, schädliche Website-Updates oder alle Browserangriffe geschützt zu sein. Verwende zunächst Testdaten.

Speicherung ist an Gerät, Browser und Webadresse gebunden. Das ist KEIN Online-Konto. Passwort vergessen: keine Wiederherstellung durch uns. Browserdaten löschen, App entfernen, Speicherbereinigung oder Geräteverlust können Daten löschen. Ein neuer Domainname verschiebt die Daten nicht automatisch. Unter „Backup“ kannst du eine verschlüsselte Datei sichern. Zum Wiederherstellen: Sperrbildschirm → „Verschlüsseltes Todate-Backup wiederherstellen“, Datei und damaliges Passwort wählen. Wiederherstellen ersetzt den vorhandenen lokalen Datensatz erst nach Bestätigung. Sichere vor Updates ein Backup. Behalte die URL bei.

Mehrere gleichzeitig bearbeitete Tabs werden durch eine Revisionsprüfung vor gegenseitigem Überschreiben geschützt. Bei Konflikt nicht weiterarbeiten oder neu laden, bevor Änderungen notiert sind. Nur einen Tab verwenden.

## Aktualisieren
Neue Webdateien an derselben Stelle im Repository hochladen und committen; GitHub Pages veröffentlicht sie neu. Änderungen am HTML sollten keine eingegebenen Journaldaten enthalten. Nur dieses Webpaket hochladen, keine privaten Backups oder Screenshots aus deinem Tagebuch.

## Verifiziert
Chromium: Einrichtung, falsches Passwort, Sperren/Entsperren, dauerhafte Personen/Bilder/Stimmung nach Neuladen und verschlüsselter Datensatz ohne Klartextnamen. Backup-Wiederherstellung in separatem Browserkontext getestet. Safari/iPhone wurde hier nicht auf einem echten Gerät getestet.
