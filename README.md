# Racoony

Ein endloser Plattformer für den Browser. Du steuerst Racoony, einen diebischen Waschbären, nachts über die Dächer der Stadt. Spring über die Lücken zwischen den Häusern, stopf deinen Beutel mit Beute voll und lass dich nicht vom Suchscheinwerfer erwischen.

## Spielen

Öffne `index.html` im Browser. Du brauchst keine Installation und keinen Build-Schritt, das ganze Spiel steckt in dieser einen Datei. Nur die Schriften lädt das Spiel von Google Fonts. Ohne Internet springen Ersatzschriften ein, spielbar bleibt es trotzdem.

Als Website: In den Repo-Einstellungen unter **Settings → Pages** den Branch `main` und den Ordner `/ (root)` wählen. Danach läuft das Spiel unter `https://judgeman.github.io/Racoony/`.

## Steuerung

| Aktion | Tastatur | Touchscreen |
| --- | --- | --- |
| Laufen | `←` `→` oder `A` `D` | Steuerkreuz unten links, Daumen nach links oder rechts schieben |
| Rennen | `Shift` oder `X` gedrückt halten | Schalter „Rennen“ |
| Springen | `Leertaste`, `↑` oder `W` | Sprungknopf unten rechts |
| Doppelsprung | in der Luft nochmal springen | in der Luft nochmal tippen |
| Pause | `Esc` oder `P` | Pause-Knopf oben rechts |
| Ton an/aus | `M` | Lautsprecher-Knopf oben rechts |

Länger gedrückt halten springt höher, und wer rennt, springt weiter.

## Regeln

- **Punkte** = zurückgelegte Strecke in Metern plus der Wert der Beute.
- **Beute:** Münze 5, Brezel 20, Ring 100 Punkte. Mit jedem Stück wird Racoonys Beutel dicker.
- **Hindernisse:** Schornsteine, Klimaanlagen und Wassertanks sind feste Blöcke. Du kannst dagegen laufen oder draufspringen.
- **Wäscheleinen** federn dich hoch, wenn du draufspringst. So schaffst du Lücken, die für einen normalen Sprung zu breit sind.
- **Suchscheinwerfer:** Ab etwa 360 m schwenken Lichtkegel von der Straße hoch. Solange du im Licht stehst, füllt sich die Anzeige „Entdeckt“. Ist sie voll, bist du erwischt.
- **Verlieren** kannst du auf zwei Arten: durch einen Sturz in eine Lücke oder wenn dich ein Suchscheinwerfer erwischt. Danach gibt es einen Steckbrief mit deiner Beute.
- Je weiter du kommst, desto breiter werden die Lücken und desto mehr Hindernisse und Scheinwerfer gibt es.
- Deine Bestleistung speichert der Browser lokal (`localStorage`).

## Technik

- Eine einzige HTML-Datei: Canvas 2D für die Grafik, Web Audio für Geräusche und Musik.
- Figuren, Stadt und Sound erzeugt das Spiel komplett im Code. Es gibt keine Bild- oder Audiodateien.
- Die wichtigsten Stellschrauben stehen am Anfang des Skripts im Abschnitt `Tuning`: Schwerkraft, Sprungkraft, Lauf- und Renntempo und die Größe der Kollisionsbox.
