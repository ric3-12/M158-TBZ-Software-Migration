# Übung – Grundelemente der Migration – Vorname Nachname

## 1. Nennen Sie zwei Gründe, wann man eine Software-Migration machen muss

- Wenn das bestehende System neue Anforderungen an Hard- und Software nicht mehr ausreichend erfüllt.
- Aus Gründen der Kostenreduktion, da eine komplette Neuentwicklung oder Neuanschaffung häufig zu teuer ist.

(Quelle: Kapitel 1.1 Problemdarstellung :contentReference[oaicite:0]{index=0})

---

## 2. Wie ist die Definition für das Wort Migration im Skript?

Migration ist ein Verfahren, bei dem ein Teil eines Systems in ein anderes übertragen wird, indem möglichst alle Daten von einem Ursprungsort an einen neuen Zielort verschoben werden, ohne dass die Funktionalität verändert wird.

Wichtig:
- Keine funktionale Veränderung
- Keine Neuinstallation der Daten notwendig

(Quelle: Kapitel 2.1 Der Begriff Migration :contentReference[oaicite:1]{index=1})

---

## 3. Der Begriff Software-Migration gehört zu welchem Bereich des Software-Engineering?

Die Software-Migration gehört zur **Software-Erhaltung**.

Das Software-Engineering besteht aus:
- Software-Entwicklung (vor der ersten Freigabe)
- Software-Erhaltung (nach der ersten Freigabe)

Migration ist Teil der Software-Erhaltung.

(Quelle: Kapitel 2.1 :contentReference[oaicite:2]{index=2})

---

## 4. Wie ist die Beziehung zwischen Hard- und Software-Migration?

Hardware- und Software-Migration überschneiden sich häufig und gehen oft Hand in Hand.  

Nach einer Hardware-Migration muss in der Regel auch die Software angepasst oder aktualisiert werden.

(Quelle: Kapitel 2.1 :contentReference[oaicite:3]{index=3})

---

## 5. Was sollte niemals mit einer Software-Migration vermischt werden und warum?

Funktionale Änderungen dürfen niemals mit einer Migration vermischt werden.

Begründung:
Ein migriertes System muss funktional identisch mit dem ursprünglichen System sein, damit es korrekt gegentesten werden kann.  
Erforderliche Änderungen sollten erst nach vollständiger Migration durchgeführt werden.

(Quelle: Kapitel 2.2.1 Integration :contentReference[oaicite:4]{index=4})

---

## 6. Auf was zielt das Reengineering bei einer Migration ab?

Reengineering zielt auf die **Verbesserung der Software-Qualität** ab.

Unterschied zur Migration:

| Migration | Reengineering |
|------------|--------------|
| Übertragung in eine neue Umgebung | Verbesserung der Software-Qualität |
| Funktion bleibt gleich | Funktion bleibt gleich |
| Qualität bleibt unverändert | Qualität wird verbessert |

(Quelle: Kapitel 2.2.2 :contentReference[oaicite:5]{index=5})

---

## 7. Was versteht man unter Reverse Engineering?

Reverse Engineering bedeutet das Ableiten oder Nachdokumentieren von Informationen über ein bestehendes System.

Merkmale:
- Analyse des bestehenden Systems
- Erstellung von Grafiken, Diagrammen, Tabellen oder Texten
- System bleibt unverändert
- Kann Grundlage für eine Migration sein

Ziele:
- Systemanalyse
- Vorbereitung der Wiederverwendung
- Unterstützung einer Migration

(Quelle: Kapitel 2.2.3 :contentReference[oaicite:6]{index=6})

---

## Git Commit

```bash
git add Abgaben/Übung- Grundelemente der Migration - Vorname Nachname.md
git commit -m "Grundelemente der Migration"
git push