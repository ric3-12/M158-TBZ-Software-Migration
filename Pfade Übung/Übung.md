# Übung Pfade

## Gegebene Verzeichnisstruktur

```
C:\Daten\
│
├── index.html
├── Bilder\
│   ├── Blume.jpg
│   └── test.html
└── CSS\
    └── main.css
```

---

## 1. Absoluter Pfad von main.css

Ein absoluter Pfad beginnt immer beim Laufwerk.

```
C:\Daten\CSS\main.css
```

---

## 2. Relativer Pfad von index.html zu Blume.jpg

index.html liegt in:
```
C:\Daten
```

Blume.jpg liegt in:
```
C:\Daten\Bilder
```

Relativer Pfad:

```
Bilder/Blume.jpg
```

Beispiel in HTML:

```html
<img src="Bilder/Blume.jpg" alt="Blume">
```

---

## 3. Absoluter Pfad von main.css zu Blume.jpg

Der absolute Pfad lautet:

```
C:\Daten\Bilder\Blume.jpg
```

---

## 4. Relativer Pfad von main.css zu Blume.jpg

main.css liegt in:
```
C:\Daten\CSS
```

Blume.jpg liegt in:
```
C:\Daten\Bilder
```

Man geht eine Ebene nach oben (`..`) und dann in den Ordner Bilder.

```
../Bilder/Blume.jpg
```

Beispiel in CSS:

```css
background-image: url("../Bilder/Blume.jpg");
```

---

## 5. Relativer Pfad von test.html zu Blume.jpg

test.html liegt in:
```
C:\Daten\Bilder
```

Blume.jpg liegt im gleichen Ordner.

Relativer Pfad:

```
Blume.jpg
```

Beispiel in HTML:

```html
<img src="Blume.jpg" alt="Blume">
```

---

## Kurz-Erklärung

- `../` bedeutet: eine Ebene nach oben gehen
- `./` bedeutet: aktueller Ordner
- Kein `../` nötig, wenn sich Dateien im gleichen Ordner befinden
- Absolute Pfade beginnen immer mit Laufwerk (z.B. C:\)
- Relative Pfade starten vom aktuellen Speicherort der Datei
