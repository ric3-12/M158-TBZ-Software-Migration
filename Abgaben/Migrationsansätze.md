# Übung – Migrationsansätze – Vorname Nachname

---

# 1. Beschreibung der Migrationsansätze

## Cold Turkey / Big Bang

- Vollständige Umstellung in einem einzigen Schritt
- Neues System wird parallel entwickelt
- Finaler, vollständiger Wechsel
- Downtime erforderlich
- Hohes Risiko

(Quelle: Skript Kapitel 3 :contentReference[oaicite:0]{index=0})

---

## Retire

- Alte Anwendung wird stillgelegt
- Ersatz durch neue Software oder Cloud-Lösung
- Keine Migration des alten Systems

(Quelle: Cloud Migration Checklist S.7 :contentReference[oaicite:1]{index=1})

---

## Refactor

- Bestehende Software wird angepasst
- Code wird optimiert oder modernisiert
- Funktionalität bleibt im Wesentlichen erhalten

(Quelle: :contentReference[oaicite:2]{index=2})

---

## Rebuild / Reengineering

- Komplette Neuentwicklung der Anwendung
- Moderne Architektur
- Hoher Aufwand, hohe Qualität

---

## Chicken-Little-Migrationsansatz

- System wird in einzelne Pakete zerlegt
- Schrittweise Migration
- Altsystem bleibt während Migration in Betrieb
- Geringeres Risiko
- Lange Migrationsdauer

(Quelle: Skript Kapitel 3 :contentReference[oaicite:4]{index=4})

---

## Butterfly-Migrationsansatz

- Nutzung von temporären Speichern
- Daten werden schrittweise übertragen
- Fallback möglich
- Sehr flexibel
- Hoher technischer Aufwand

(Quelle: Skript Kapitel 3 :contentReference[oaicite:5]{index=5})

---

## COREM-Migrationsansatz

- Kombination aus Top-Down und Bottom-Up Analyse
- Stark dokumentationsbasiert
- Für kleine Systeme geeignet
- In der Praxis selten verwendet

(Quelle: Skript Kapitel 3 :contentReference[oaicite:6]{index=6})

---

## Repurchase

- Wechsel auf anderes Produkt (z.B. SaaS)
- Keine technische Migration des bestehenden Systems

(Quelle: :contentReference[oaicite:7]{index=7})

---

## Retain

- Anwendung bleibt unverändert
- Migration wird verschoben

(Quelle: :contentReference[oaicite:8]{index=8})

---

# 2. Gewählter Migrationsansatz für meine imaginäre Migration

## Gewählt: Chicken-Little-Migrationsansatz

Begründung:

- Reduziertes Risiko durch schrittweise Migration
- System bleibt während der Umstellung verfügbar
- Geeignet für produktive Unternehmenssysteme
- Keine komplette Neuentwicklung erforderlich
- Gute Testbarkeit nach jedem Schritt

---

# 3. Grober Durchführungsplan (Ablaufdiagramm – 18 Schritte)

Dieser Ablauf dient als Grundlage für das visuelle Diagramm (z.B. draw.io).

1. Projektstart
2. Definition der Migrationsziele
3. Analyse des bestehenden Systems
4. Identifikation aller Module
5. Analyse der Abhängigkeiten
6. Definition der Zielumgebung
7. Aufbau der neuen Infrastruktur
8. Testumgebung einrichten
9. Migration der Datenbank
10. Datenintegrität testen
11. Migration des ersten Moduls
12. Funktionstest Modul 1
13. Anpassung der Schnittstellen
14. Migration weiterer Module
15. Gesamtsystem-Test
16. Vorbereitung Go-Live
17. Umschaltung auf neues System
18. Abschaltung des Altsystems
19. Post-Migration Review
20. Abschlussdokumentation

---

# 4. Präsentation

Das Ablaufdiagramm wurde mit draw.io erstellt und in eine Präsentation integriert.

---

# Git Commit

```bash
git add Abgaben/Übung - Migrationsansätze Vorname Nachname.md
git commit -m "Übung - Migrationsansätze"
git push