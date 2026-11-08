# Racoony

Ein endloser Plattformer für den Browser. Du steuerst Racoony, einen diebischen Waschbären, nachts über die Dächer einer schlafenden Vorstadt. Lauf über Giebeldächer, spring über die Gärten zwischen den Häusern, stopf deinen Beutel voll und lass dich von keinem Nachbarn erwischen.

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
- **Beute:** Münze 5, Grillwurst 20, Gartenzwerg 100 Punkte. Mit jedem Stück wird Racoonys Beutel dicker.
- **Dächer:** Racoony läuft die Dachschrägen hinauf und hinunter. Schornsteine und Gauben sind feste Blöcke, gegen die man stößt oder auf die man springt.
- **Garagen und Gartenhäuschen** stehen in manchen breiten Gärten und dienen als Zwischenstufe.
- **Trampoline** in den Gärten schleudern dich zurück aufs Dach.
- **Ratten und Tauben** sind die Gegner auf den Dächern. Ratten laufen auf dem Dach hin und her, auch die Schrägen hinauf. Tauben sitzen pickend auf dem Dach oder einem Schornstein und flattern auf, wenn du näher kommst; dann schweben sie auf Kopfhöhe. Spring ihnen auf den Kopf: Das gibt Punkte (Ratte 15, Taube 25) und Schwung nach oben, mit gehaltener Sprungtaste noch mehr. Wer sie anders berührt, fliegt vom Dach.
- **Nachbarn mit Taschenlampe:** Ab etwa 300 m steht hin und wieder ein Nachbar im Bademantel im Garten und leuchtet die Dächer ab. Solange du im Licht stehst, füllt sich die Anzeige „Entdeckt“. Ist sie voll, bist du erwischt.
- **Verlieren** kannst du auf drei Arten: durch einen Sturz in einen Garten (je nachdem, wo du landest, im Gartenteich, in der Regentonne oder beim Nachbarshund), durch eine Ratte oder Taube, die dich vom Dach schubst, oder wenn dich ein Nachbar erwischt. Danach gibt es einen Steckbrief mit deiner Beute und den erledigten Gegnern.
- Je weiter du kommst, desto breiter werden die Gärten und desto mehr Schornsteine, Gauben, Ratten, Tauben und Nachbarn gibt es. Tauben tauchen ab etwa 120 m auf.
- Deine Bestleistung speichert der Browser lokal (`localStorage`).

## Technik

- Eine einzige HTML-Datei: Canvas 2D für die Grafik, Web Audio für Geräusche und Musik.
- Figuren, Häuser, Gärten und Sound erzeugt das Spiel komplett im Code. Es gibt keine Bild- oder Audiodateien.
- Die Vorstadt entsteht beim Laufen zufällig. Die Abstände zwischen den Häusern werden aus der Sprungphysik berechnet, sodass jeder Garten im normalen Lauftempo zu schaffen ist, manche nur mit Doppelsprung, Trampolin oder über eine Garage.
- Die wichtigsten Stellschrauben stehen am Anfang des Skripts im Abschnitt `Tuning`: Schwerkraft, Sprungkraft, Lauf- und Renntempo, Trampolin-Schwung und die Größe der Kollisionsbox.
