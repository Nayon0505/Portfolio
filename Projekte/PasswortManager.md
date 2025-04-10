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

Um ein Benutzerkonto zu erstellen, muss der Benutzer einen Nutzernamen, seine E-Mail-Adresse sowie ein gewünschtes Passwort angeben und dieses bestätigen. Erfüllen alle Angaben die festgelegten Kriterien, wird das Benutzerkonto in der Firebase-Datenbank angelegt, und der Benutzer wird automatisch zum Dashboard weitergeleitet, außerderm erhält er eine Verifizierungsmail.

<div style="display: flex; justify-content: space-between; gap: 10px; margin: 20px 0;">
  <img src="{{ site.baseurl }}/assets/images/login.png" alt="Login" style="width: 48%;">
  <img src="{{ site.baseurl }}/assets/images/register.png" alt="Register" style="width: 48%;">
</div>

---

## **3. Dashboard**

Das Dashboard bildet das Herzstück dieser Applikation. Hier kann der Nutzer seinem persönlichen "Wallet" neue Passwörter hinzufügen. Dazu gibt er den Benutzernamen oder die zugehörige E-Mail-Adresse, die Website sowie das entsprechende Passwort ein. Anschließend kann er die Eingaben speichern.
Das Passwort wird in der Firebase-Datenbank unter einem nutzerspezifischen Verzeichnis abgelegt. Durch definierte Sicherheitsregeln ist der Zugriff darauf aktuell ausschließlich dem jeweiligen Nutzer sowie Administratoren vorbehalten.
Zusätzlich kann der Nutzer Passwörter einfach bearbeiten, kopieren, durchsuchen oder bei Bedarf löschen.
Ein kleines Feature: Maskierte Passwörter werden im Klartext angezeigt, sobald man sie anklickt – dies soll in bestimmten Situationen zur Wahrung der Privatsphäre beitragen.

<div style="display: flex; justify-content: space-between; gap: 10px; margin: 20px 0;">
  <img src="{{ site.baseurl }}/assets/images/dashboard_one.png" alt="Login" style="width: 48%;">
  <img src="{{ site.baseurl }}/assets/images/dashboard_add_pw.png" alt="Register" style="width: 48%;">
</div>

---

## **4. Settings**

In den Einstellungen kann der Nutzer seine E-Mail-Adresse und seinen Benutzernamen einsehen. Außerdem erhält er Informationen darüber, ob seine E-Mail bereits verifiziert wurde. Falls nicht, kann er erneut eine Verifizierungs-E-Mail anfordern. Darüber hinaus hat er die Möglichkeit, sein Passwort zu ändern und sich bei Bedarf auszuloggen.

![Diagramm]({{ site.baseurl }}/assets/images/settings_verify.png)

> {: .info }
Sobald der User eine Verifizierungs-E-Mail anfordert, wird ihm diese zugeschickt und sieht wie folgt aus.

![Diagramm]({{ site.baseurl }}/assets/images/settings_verify_email.png)

---

## **5. Passwort Generator**

Der Passwort-Generator ermöglicht es dem Nutzer, schnell und einfach Passwörter nach seinen persönlichen Vorlieben zu erstellen. Dabei kann er auswählen, ob das Passwort Groß- und/oder Kleinbuchstaben, Zahlen und/oder Sonderzeichen enthalten soll. Außerdem lässt sich die gewünschte Passwortlänge individuell festlegen.
Nach der Generierung kann das Passwort mit einem einfachen Klick in die Zwischenablage kopiert werden.

<div style="display: flex; justify-content: space-between; gap: 10px; margin: 20px 0;">
  <img src="{{ site.baseurl }}/assets/images/pw_generator_one.png" alt="Login" style="width: 48%;">
  <img src="{{ site.baseurl }}/assets/images/pw_generator_two.png" alt="Register" style="width: 48%;">
</div>

---

## 📧 Kontakt
Falls Sie Fragen haben oder mehr erfahren möchten, können Sie mich gerne kontaktieren:
 
> {: .info }
[![Email](https://img.shields.io/badge/-aniloeker@hotmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:aniloeker@hotmail.com)
[![LinkedIn](https://img.shields.io/badge/-Anil%20Emircan%20Öker-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/anil-emircan-öker-a2878430a)
[![GitHub](https://img.shields.io/badge/-@Emircan1122-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Emircan1122)

--- 

Vielen Dank für's anschauen meines Projektes!