# Klötzchen-Kalle

Steine-Stapelspiel (Tetris-Prinzip) für kleine Kinder, getestet von Ella auf dem iPad.
Idee + Machbarkeit: `../Ideen/ideen.md` („Kinder-Tetris mit Dreh-Männchen“).

- Alles in `index.html` (Vanilla JS + Canvas, keine Abhängigkeiten), live über GitHub Pages.
- Kern: Kalle läuft bei „Drehen“ hin und dreht den Stein um 90°, solange ruht das Fallen. Kein Game Over.
- Tempo-Stellschrauben oben im Skript: `WALK`, `CLIMB`, Drehphasen `T_WIND`/`T_PUSH`/`T_REL`, Fallzeiten an den Tempo-Knöpfen (`data-ms`).
- Ton: Web Audio, auf dem iPad erst nach Berührung (`unlock`); `navigator.audioSession.type = "playback"` damit es auch bei Stummschaltung klingt.
- Name/Optik bewusst nicht „Tetris“ (geschützte Marke).
