# CMS und Datenbank Ablauf

## 1. CMS-Aufruf (User öffnet https://supercms.ch)

### 9 Schritte Ablauf

1. Der User gibt https://supercms.ch in seinen Browser ein.  
2. Der Browser baut über **HTTPS (TLS)** eine sichere Verbindung zum Webserver auf.  
3. Die Anfrage wird an den **Webserver** (z.B. Apache oder Nginx) gesendet.  
4. Der Webserver erkennt, dass die Seite von einem **PHP-CMS** verarbeitet werden muss.  
5. Der Webserver übergibt die Anfrage an den **PHP Interpreter**.  
6. Das **CMS** benötigt Inhalte und verbindet sich mit der **MySQL/MariaDB Datenbank** über **mysqli**.  
7. Die **Datenbank** liest die Daten von der Festplatte (**ext4 Dateisystem**).  
8. Die Daten werden zurück an das **CMS / PHP Script** geschickt.  
9. Das CMS generiert eine **HTML-Seite**, welche über **HTTPS** zurück an den Browser gesendet wird.

### Ablaufdiagramm

```text
User
 ↓
Browser
 ↓ HTTPS
Webserver (Apache / Nginx)
 ↓
PHP Interpreter
 ↓
CMS
 ↓ mysqli
MySQL / MariaDB
 ↓
ext4 Dateisystem