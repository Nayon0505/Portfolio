---
title: Passwort manager
parent: Projekte
nav_order: 0
---

<div style="display: flex; align-items: center; gap: 20px;">
  <h1>Passwort Manager</h1>
  <img src="{{ site.baseurl }}/assets/images/Icon_MountainKeys.png" alt="Icon" style="height: 80px; width: auto;">
</div>

---

Der Name des Passwort Managers lautet MountanKey (natürlich wird Berg im Englischen anders geschrieben), 
im Rahmen des Modules App Entwicklung mit Android, habe ich dieses Projekt bearbeitet.
In den Folgenden abschnitten bekommen Sie einen kleinen Einblick.

---

<details open markdown="block">
{: .text-delta }
<summary>Table of contents</summary>
+ ToC
{: toc }
</details>

---

## **1. Grundstruktur der App**

Im Rahmen eines Projekts habe ich eine Android-App entwickelt, deren Backend aus insgesamt 7 Java-Klassen besteht. Für das Frontend wurden 12 XML-Dateien erstellt, die die Benutzeroberfläche gestalten.

Beim ersten Start muss sich der Nutzer registrieren oder anmelden. Nach erfolgreichem Login erhält er Zugriff auf drei Hauptbereiche:

- Dashboard 
- Einstellungen 
- Passwort-Generator 

![Diagramm]({{ site.baseurl }}/assets/images/PasswortManager_Diagramm.jpg)

---

## **2. Login/Registrierung**

Das Anmeldesystem umfasst alle erforderlichen Funktionen: Es überprüft die E-Mail-Adresse und das Passwort des Benutzers. Bei gültigen Anmeldedaten wird der Benutzer authentifiziert und in das Dashboard weitergeleitet. Sind die Daten ungültig, erscheint eine Fehlermeldung. Zusätzlich besteht die Möglichkeit, das Passwort bei Bedarf über einen E-Mail-Link zurückzusetzen. Falls kein Benutzerkonto existiert, kann dieses direkt im System neu angelegt werden.

Um ein Benutzerkonto zu erstellen, muss der Benutzer einen Nutzernamen, seine E-Mail-Adresse sowie ein gewünschtes Passwort angeben und dieses bestätigen. Erfüllen alle Angaben die festgelegten Kriterien, wird das Benutzerkonto in der Firebase-Datenbank angelegt, und der Benutzer wird automatisch zum Dashboard weitergeleitet.

<div style="display: flex; justify-content: space-between; gap: 10px; margin: 20px 0;">
  <img src="{{ site.baseurl }}/assets/images/login.png" alt="Login" style="width: 48%;">
  <img src="{{ site.baseurl }}/assets/images/register.png" alt="Register" style="width: 48%;">
</div>

---

## **3. Dashboard**

<div style="display: flex; justify-content: space-between; gap: 10px; margin: 20px 0;">
  <img src="{{ site.baseurl }}/assets/images/dashboard_one.png" alt="Login" style="width: 48%;">
  <img src="{{ site.baseurl }}/assets/images/dashboard_add_pw.png" alt="Register" style="width: 48%;">
</div>

---

## **4. Settings**

![Diagramm]({{ site.baseurl }}/assets/images/settings_verify.png)

> {: .info }
Sobald der User seine Email verifizieren möchte, wird ihm eine E-Mail gesschickt, die wie folgt aussieht.

![Diagramm]({{ site.baseurl }}/assets/images/settings_verify_email.png)

---

## **5. Passwort Generator**

![Diagramm]({{ site.baseurl }}/assets/images/pw_generator_one.png)
![Diagramm]({{ site.baseurl }}/assets/images/pw_generator_two.png)
