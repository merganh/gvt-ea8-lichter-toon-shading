# EA 8: Lichter auf einer Kreisbahn mit Toon Shading

Einsendeaufgabe 8, Modul Graphical Visualisation Technologies, TH Lübeck, Wintersemester 2026/27.

Eine einseitige WebGL-Anwendung auf Basis der Übung BEL-03: ein roter Torus, eine
grüne und eine blaue Kugel auf einer hellgrauen Ebene, beleuchtet von zwei weißen
Punktlichtern mit dem Phong-Beleuchtungsmodell pro Fragment. Mit der Taste `l`
bzw. `L` bewegen sich beide Lichter schrittweise auf einer Kreisbahn um die
Modelle, unabhängig von der Kamera. Mit `t` bzw. `T` wird ein Toon-Shader
(Cel-Shading) im Fragment-Shader ein- und ausgeschaltet.

## Live-Demo

Öffentlich erreichbar unter:
<https://merganh.github.io/gvt-ea8-lichter-toon-shading/>

## Lokal ausführen

Kein Build-Schritt. Die Seite lässt sich über einen lokalen Server öffnen:

```bash
python3 -m http.server 8000
# dann im Browser: http://localhost:8000
```

## Deployment via GitHub Pages

Im Repo liegt ein Workflow unter `.github/workflows/pages.yml`, der die Seite bei
jedem Push auf `main` automatisch nach GitHub Pages deployt. Einmalig im Repo
unter **Settings → Pages → Build and deployment → Source** `GitHub Actions`
wählen.

## Aufbau

- `index.html`: gesamte Anwendung in einer Datei (HTML, CSS, Shader und JS inline)

Es werden keine externen Bibliotheken, Bilder oder Schriften verwendet. WebGL 1,
GLSL ES 1.00, Geometrie und Matrizen sind selbst implementiert.

## Bedienung

- **l / L**: beide Lichter einen Schritt (15°) weiter auf der Kreisbahn bewegen
- **t / T**: Toon-Shader ein- und ausschalten (Erweiterung)
- **← / →**: Kamera um die Szene drehen
- **↑ / ↓**: Kamera anheben bzw. absenken

Jede Taste hat einen Button auf der Seite. Bei `l` und `t` löst Gedrückthalten
keinen Dauerlauf aus.

## Quelltext-Markierung

Die für die Aufgabe geschriebenen Stellen sind mit
`// START EA8_LICHTER_TOON` und
`// END EA8_LICHTER_TOON` markiert.
