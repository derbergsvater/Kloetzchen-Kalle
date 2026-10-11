# Klötzchen-Kalle

Steine-Stapelspiel (Tetris-Prinzip) für kleine Kinder, getestet von Ella auf dem iPad.
Idee + Machbarkeit: `../Ideen/ideen.md` („Kinder-Tetris mit Dreh-Männchen“).

- Alles in `index.html` (Vanilla JS + Canvas, keine Abhängigkeiten), live über GitHub Pages.
- Kern: Kalle läuft bei „Drehen“ hin und dreht den Stein um 90°, solange ruht das Fallen. Kein Game Over. Vorschau „Nächster“ rechts neben dem Feld (`nextShape`, `drawNext`).
- Tempo-Stellschrauben oben im Skript: `WALK`, `CLIMB`, Drehphasen `T_WIND`/`T_PUSH`/`T_REL`, Fallzeit über Regler `#speed` (Stufe 1–10 = 3 s … 0,45 s je Reihe).
- Musik: `makeSong()` erfindet jedes Lied neu (Stil aus `STYLES`, Tonart, Tempo, Swing, Akkordfolge, Motive; Intro–A–B–A–Schluss). Klang selbst synthetisiert: Karplus-Strong-Zupfsaite, Marimba, Glockenspiel, Flöte, Pad, Bass, Drums, Hall + Echo.
- Anreiz: Sterne (Bonus bei Mehrfach-Reihen) füllen den Balken bis zum nächsten Geschenk (`GIFTS`: Hüte, Hund, Vogel, Regenbogen; bewusst nichts mit Zaubern/Spiritismus). Sammlung in `localStorage['kalle']`, Schatzkiste 🧰 zum Auswählen.
- Hilfe 🔨 / H: Kalle seilt sich ab und zertrümmert oben Reihen (`smashRow`), bis höchstens die Hälfte belegt ist; keine Sterne dafür.
- Tastatur: ← → schieben, ↑ drehen bzw. Fallen abbrechen, ↓ (oder Leertaste) fallen; Schieben geht immer, P/Esc Pause (Legende im Pause-Fenster und auf den Knöpfen).
- Ton: Web Audio, auf dem iPad erst nach Berührung (`unlock`); `navigator.audioSession.type = "playback"` damit es auch bei Stummschaltung klingt.
- Name/Optik bewusst nicht „Tetris“ (geschützte Marke).
