---
title: Passwort manager
parent: Projekte
nav_order: 0
---

# Passwort Manager 

---

![Icon]({{ site.baseurl }}/assets/images/Icon_MountainKeys.png)

---

Der Name des Passwort Managers lautet MountanKey (natürlich wird Berg im Englischen anders geschrieben), 
im Rahmen des Modules App Entwicklung mit Android, habe ich dieses Projekt bearbeitet.
In den Folgenden abschnitten bekommen Sie einen kleinen Einblick.

---

## Grundstruktur der App

Im Rahmen eines Projekts habe ich eine Android-App entwickelt, deren Backend aus insgesamt 7 Java-Klassen besteht. Für das Frontend wurden 12 XML-Dateien erstellt, die die Benutzeroberfläche gestalten.

Beim ersten Start muss sich der Nutzer registrieren oder anmelden. Nach erfolgreichem Login erhält er Zugriff auf drei Hauptbereiche:

- Dashboard 
- Einstellungen 
- Passwort-Generator 

![Diagramm]({{ site.baseur1 }}/assets/images/PasswortManager_Diagramm.jpg)

---

## Login/Registrierung

Das Anmeldesystem umfasst alle erforderlichen Funktionen: Es überprüft die E-Mail-Adresse und das Passwort des Benutzers. Bei gültigen Anmeldedaten wird der Benutzer authentifiziert und in das Dashboard weitergeleitet. Sind die Daten ungültig, erscheint eine Fehlermeldung. Zusätzlich besteht die Möglichkeit, das Passwort bei Bedarf über einen E-Mail-Link zurückzusetzen. Falls kein Benutzerkonto existiert, kann dieses direkt im System neu angelegt werden.

Um ein Benutzerkonto zu erstellen, muss der Benutzer einen Nutzernamen, seine E-Mail-Adresse sowie ein gewünschtes Passwort angeben und dieses bestätigen. Erfüllen alle Angaben die festgelegten Kriterien, wird das Benutzerkonto in der Firebase-Datenbank angelegt, und der Benutzer wird automatisch zum Dashboard weitergeleitet.

![Diagramm]({{ site.baseur1 }}/assets/images/login.jpg)
![Diagramm]({{ site.baseur1 }}/assets/images/register.jpg)

---
