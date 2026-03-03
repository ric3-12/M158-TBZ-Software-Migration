# Übung – Migration von zwei 5er Switch-Stacks auf ein produktives Chassis – Vorname Nachname

---

# 1. Ausgangslage

- Zwei bestehende Switch-Stacks (jeweils 5 Geräte pro Stack)
- Ziel: Migration auf ein neues produktives Core-Chassis
- Downtime sollte vermieden werden
- Übergang erfolgte über 3 Chassis-Systeme

Architektur:

Stack A (5x) → Übergangs-Chassis 1  
Stack B (5x) → Übergangs-Chassis 2  
Beide → Produktives Core-Chassis  

---

# 2. Gewählter Migrationsansatz

## Inkrementelle Migration (Chicken-Little-Prinzip)

Begründung:

- Schrittweise Übernahme der Infrastruktur
- Keine vollständige Abschaltung notwendig
- Parallelbetrieb möglich
- Risiko-Minimierung
- Test nach jeder Phase

Ein Big-Bang-Ansatz wäre zu riskant gewesen, da beide Stacks gleichzeitig ersetzt worden wären.

---

# 3. Zielarchitektur

Phase 1:
Stack A → Chassis 1  
Stack B → Chassis 2  

Phase 2:
Chassis 1 + Chassis 2 → Produktives Core-Chassis  

Phase 3:
Produktives Core-Chassis übernimmt vollständig

---

# 4. Grober Durchführungsplan (18 Schritte)

## Phase 1 – Vorbereitung

1. Dokumentation beider Stacks (VLANs, Routing, STP, ACLs)
2. Backup der Konfigurationen
3. Design der Ziel-Core-Architektur
4. Definition der VLAN- und Routing-Strategie
5. Aufbau der drei Chassis im Rack
6. Grundkonfiguration der Chassis (Hostname, Management-IP)

---

## Phase 2 – Migration Stack A

7. Verbindung Stack A mit Übergangs-Chassis 1
8. Konfiguration der Trunks / VLANs
9. Routing-Anpassungen
10. Funktionstest (Clients, Server, Uplinks)
11. Monitoring & Stabilitätsprüfung

---

## Phase 3 – Migration Stack B

12. Verbindung Stack B mit Übergangs-Chassis 2
13. VLAN- und Routing-Synchronisierung
14. Funktionstest
15. Monitoring & Validierung

---

## Phase 4 – Migration zum produktiven Core-Chassis

16. Aufbau redundanter Uplinks zu produktivem Chassis
17. Schrittweise Umschaltung des Routings
18. Test der Konnektivität
19. Entfernen der alten Stacks
20. Finaler Stabilitätstest

---

# 5. Technische Herausforderungen

- Spanning Tree Stabilität
- VLAN-Konsistenz
- Routing-Redundanz (z.B. HSRP/VRRP)
- Loop-Vermeidung
- Latenz während Übergangsphase

---

# 6. Risikominimierung

- Schrittweise Migration
- Redundante Verbindungen
- Rollback-Plan
- Wartungsfenster für kritische Umschaltungen
- Permanentes Monitoring

---

# 7. Fazit

Durch die Verwendung von zwei Übergangs-Chassis konnte eine vollständige Downtime vermieden werden.  

Die Migration erfolgte kontrolliert und inkrementell, wodurch das Risiko eines kompletten Netzwerkausfalls minimiert wurde.

Das gewählte Vorgehen entspricht dem Prinzip einer schrittweisen Migration (Chicken-Little-Ansatz) auf Infrastruktur-Ebene.