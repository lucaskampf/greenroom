# Greenroom

Ein ruhiger Fokus-Timer für die Menüleiste deines Macs. Du arbeitest in Fokus-Blöcken (Standard: 25 Minuten), danach schickt dich Greenroom mit einem grünen Vollbild in die Pause. Nach vier Blöcken gibt es eine lange Pause.

- Restzeit direkt in der Menüleiste
- Pausen-Bildschirm auf allen Monitoren, der nach der Pause von selbst wiederkommt
- Dashboard: Fokuszeit heute und diese Woche, Serie, Heatmap, beste Tageszeit, CSV-Export
- Freiwillige Online-Rangliste: vergleiche dich in privaten Gruppen oder global
- Kein Tracking, keine Werbung. Ohne Rangliste bleiben deine Daten auf deinem Mac

<!-- Screenshots (noch einzufügen):
  1. Menüleiste mit Restzeit und geöffnetem Menü
  2. Grüner Pausen-Bildschirm mit Countdown
  3. Hauptfenster mit Dashboard
  4. Einstellungen
-->

## Download

**[Greenroom herunterladen](https://github.com/lucaskampf/greenroom/releases/latest)**: Dort unter „Assets“ die Datei `Greenroom-<Version>.dmg` laden.

Greenroom ist kostenlos.

## Installieren

1. Die heruntergeladene `.dmg`-Datei öffnen.
2. **Greenroom** auf den Ordner **Programme** ziehen.
3. Das Fenster schließen und die DMG auswerfen.

### Erster Start: einmal freigeben

Greenroom ist nicht bei Apple notarisiert (dafür bräuchte es ein kostenpflichtiges Entwickler-Konto). macOS blockiert die App deshalb beim ersten Öffnen. Das musst du **nur einmal** erlauben.

**macOS 15 (Sequoia) und neuer:**

1. Greenroom im Programme-Ordner doppelklicken. macOS meldet, dass die App nicht geöffnet werden kann. Auf **Fertig** klicken (nicht „In den Papierkorb legen“).
2. **Systemeinstellungen** öffnen und zu **Datenschutz & Sicherheit** gehen.
3. Ganz nach unten zum Abschnitt **Sicherheit** scrollen. Dort steht ein Hinweis, dass „Greenroom“ blockiert wurde. Auf **Trotzdem öffnen** klicken.
4. Mit Passwort oder Touch ID bestätigen und im nächsten Dialog nochmals **Trotzdem öffnen** wählen.

Der Knopf „Trotzdem öffnen“ erscheint nur für kurze Zeit nach dem Startversuch. Fehlt er, Schritt 1 einfach wiederholen.

Unter macOS 14 (Sonoma) geht es schneller: Rechtsklick auf Greenroom → **Öffnen** → **Öffnen**.

**Für Terminal-Nutzer:** Statt der Schritte oben kannst du die Download-Markierung auch direkt entfernen:

```bash
xattr -dr com.apple.quarantine /Applications/Greenroom.app
```

Danach startet Greenroom normal per Doppelklick.

## Systemvoraussetzungen

- macOS 14 (Sonoma) oder neuer
- Apple-Silicon- oder Intel-Mac

## Updates

Greenroom schaut einmal am Tag hier auf GitHub nach, ob es eine neue Version gibt. Wenn ja, fragt die App dich vorher. Ohne deine Zustimmung wird nichts installiert. Du kannst auch selbst prüfen: im Menü **Nach Updates suchen …**

Jedes Update ist kryptografisch signiert. Greenroom installiert nur Updates, deren Signatur passt. Die automatische Prüfung kannst du unter **Einstellungen → Updates** abschalten.

Falls „Beim Anmelden starten“ nach einem Update nicht mehr greift: Den Schalter in den Einstellungen einmal aus- und wieder einschalten.

## Datenschutz

- Kein Tracking, keine Werbung, keine Analyse-Tools
- Standardmäßig bleiben deine Fokus-Daten und Einstellungen auf deinem Mac. Ein Konto brauchst du nicht.
- **Update-Prüfung:** Greenroom fragt einmal am Tag bei GitHub nach einer neuen Version (und lädt sie, wenn du zustimmst). Dabei werden keine persönlichen Daten gesendet. Wie bei jedem Abruf einer Webseite sieht GitHub deine IP-Adresse sowie die App- und macOS-Version. Die Prüfung lässt sich abschalten.
- **Online-Rangliste (nur wenn du beitrittst):** Greenroom sendet deinen Nickname und pro Tag deine Fokusminuten und die Zahl abgeschlossener Fokus-Blöcke an `greenroom.whiteroot.de`. Der Dienst läuft bei Cloudflare und wird von der WhiteRoot UG (haftungsbeschränkt) betrieben. Keine Uhrzeiten, keine einzelnen Einheiten, keine E-Mail-Adresse. In der globalen Rangliste erscheinst du nur, wenn du das zusätzlich einschaltest. Dein Zugangsschlüssel liegt nur auf deinem Mac in `~/Library/Application Support/Greenroom/account.json` (nur für deinen Benutzer lesbar). Unter **Rangliste → Konto & Online-Daten löschen** löschst du alles auf dem Server sofort.
- Details: [Datenschutzerklärung](https://greenroom.whiteroot.de/datenschutz) · [Impressum](https://greenroom.whiteroot.de/impressum)

## Deinstallieren

1. Greenroom beenden (Menüleiste → **Greenroom beenden**). Wenn „Beim Anmelden starten“ aktiv war, den Schalter vorher ausschalten.
2. `Greenroom.app` aus dem Programme-Ordner in den Papierkorb legen.
3. Optional die gespeicherten Daten löschen. Im Finder **Gehe zu → Gehe zum Ordner …** wählen und diese Orte entfernen:
   - `~/Library/Application Support/Greenroom` (deine Fokus-Statistik und ggf. der Ranglisten-Zugang `account.json`; ein Online-Konto vorher in der App unter **Rangliste → Konto & Online-Daten löschen** löschen, sonst wird es nach 12 Monaten Inaktivität automatisch entfernt)
   - `~/Library/Preferences/de.lucaskampf.greenroom.plist` (Einstellungen)
   - `~/Library/Caches/de.lucaskampf.greenroom`
   - `~/Library/HTTPStorages/de.lucaskampf.greenroom`

## Fehler oder Ideen?

Gern als [Issue](https://github.com/lucaskampf/greenroom/issues) melden oder per Mail an [greenroom@whiteroot.de](mailto:greenroom@whiteroot.de).

Greenroom wird herausgegeben von der WhiteRoot UG (haftungsbeschränkt). [Impressum](https://greenroom.whiteroot.de/impressum)

## Lizenz

Greenroom ist kostenlose Software (Freeware). Der Quellcode ist nicht öffentlich. Details stehen in [LICENSE](LICENSE). Greenroom nutzt [Sparkle](https://sparkle-project.org) für Updates ([Lizenz](THIRD_PARTY_LICENSES.txt)).
