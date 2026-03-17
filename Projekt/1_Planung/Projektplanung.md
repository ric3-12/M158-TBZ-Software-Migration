# Projektziele
Das Ziel dieses Projekts ist die vollständige Migration der bestehenden vTiger CRM Installation von CentOS 6.6 auf Ubuntu 22.04 LTS. Im Scope enthalten sind die Datenbank, alle Konfigurationen sowie die Dateianhänge. Nicht im Scope ist eine Neuentwicklung oder Anpassung der CRM-Funktionalitäten.

---

# Verantwortlichkeiten
Die gesamte Planung, Durchführung und Dokumentation der Migration liegt beim Projektverantwortlichen. Der Berufsschullehrer übernimmt die Rolle des Stakeholders und ist für die Freigabe der einzelnen Milestones zuständig.

---

# Zeitplan
Das Projekt ist auf 6 Wochen ausgelegt und gliedert sich in die Phasen Planung, Architektur, Analyse, Installation, Migration und Deployment. Der Go-Live ist für Mitte Woche 6 geplant.

---

# Rollback-Plan
Die bestehende CentOS 6.6 VM bleibt bis zum offiziellen Go-Live vollständig erhalten und in Betrieb. Im Falle eines kritischen Fehlers während der Migration wird der DNS-Eintrag zurückgesetzt und der Betrieb auf der alten VM wiederhergestellt.

---

# Risiken
Die grössten identifizierten Risiken sind die Kompatibilität zwischen PHP 5.x (CentOS) und PHP 8.x (Ubuntu), potenzielle Datenverluste während des Datenbankimports sowie mögliche Zeitverzögerungen bei unvorhergesehenen technischen Problemen.
