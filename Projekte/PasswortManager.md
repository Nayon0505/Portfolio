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

## **1. App-Architektur** 📱

**Technische Grundlagen**  
- **Backend**  
  besteht aus insgesammt 7 Java-Klassen 
- **Frontend**  
  12 XML-Layouts für responsive UI-Komponenten
- **Integration**  
  Firebase-Anbindung für Echtzeit-Datensynchronisation

**Nutzerflow**  
Starten der App erfordert zunächst:
1. **Authentifizierung**  
   Registrierung oder Login mit bestehenden Credentials
2. **Hauptnavigation**  
   Zugriff auf drei Kernmodule:
   - Dashboard  (Passwort-Verwaltung)
   - Einstellungen  
   - Passwort-Generator 

![Diagramm]({{ site.baseurl }}/assets/images/PasswortManager_Diagramm.jpg)

---
## **2. Login/Registrierung** 🔐

**Authentifizierungsprozess**  
Sicheres Anmeldesystem mit folgenden Kernfunktionen:

- **Anmeldung**  
  Validierung von E-Mail und Passwort mit Dashboard-Weiterleitung bei Erfolg
- **Fehlerbehandlung**  
  Klare Fehlermeldungen bei ungültigen Credentials
- **Passwort-Reset**  
  Passwortneusetzung via E-Mail-Link möglich

**Registrierungsablauf**  
Erstellung eines neuen Benutzerkontos erfordert:

1. **Pflichtangaben**  
   Nutzername, E-Mail-Adresse und Passwort (mit Bestätigungsfeld)
2. **Validierung**  
   Einhaltung aller Sicherheitskriterien wird geprüft
3. **Automatisierte Prozesse**  
   - Kontoanlage in Firebase-Datenbank
   - Direkte Weiterleitung zum Dashboard
   - Versand der Verifizierungs-E-Mail

<div style="display: flex; justify-content: space-between; gap: 10px; margin: 20px 0;">
  <img src="{{ site.baseurl }}/assets/images/login.png" alt="Login" style="width: 48%;">
  <img src="{{ site.baseurl }}/assets/images/register.png" alt="Register" style="width: 48%;">
</div>

---

## **3. Dashboard** 🖥️

**Zentrale Verwaltungsoberfläche**  
Das Dashboard ermöglicht folgende Kernfunktionen für das Passwortmanagement:

- 🗃️ **Wallet-Übersicht**  
  Zentrale Anzeige aller gespeicherten Zugangsdaten
- ➕ **Neueintrag erstellen**  
  Hinzufügen von Benutzername/E-Mail, Website und Passwort
- 🔍 **Suchfunktion**  
  Schnelle Filterung durch vorhandene Einträge
- ✏️ **Bearbeitungsoptionen**  
  Direktes Editieren, Kopieren oder Löschen von Einträgen

  **Sicherheitsfeatures**  
- **Verschlüsselter Speicher**  
  Passwörter werden in Firebase unter spezifischen Security Rules gespeichert
- **Selektive Sichtbarkeit**  
  Maskierte Passwörter werden per Klick temporär im Klartext angezeigt

<div style="display: flex; justify-content: space-between; gap: 10px; margin: 20px 0;">
  <img src="{{ site.baseurl }}/assets/images/dashboard_one.png" alt="Login" style="width: 48%;">
  <img src="{{ site.baseurl }}/assets/images/dashboard_add_pw.png" alt="Register" style="width: 48%;">
</div>

> 🔒 **Datenisolierung**  
> Zugriff auf gespeicherte Passwörter haben ausschließlich:  
> - Der jeweilige Kontoinhaber  
> - Authorisierte Administratoren  
{: .tip }

---

## **4. Settings** ⚙️

**Benutzerkonto-Verwaltung**  
In diesem Bereich können folgende Aktionen durchgeführt werden:

- **E-Mail & Profildaten**  
  Anzeige der registrierten E-Mail-Adresse und des Benutzernamens
- **E-Mail-Verifizierung**  
  Statusüberprüfung mit Möglichkeit zur erneuten Zusendung des Verifizierungslinks
- **Passwort ändern**  
  Sichere Passwortaktualisierung über Bestätigungsdialog
- **Logout**  
  Sitzungsbeendigung 

<div style="display: flex; justify-content: center; margin: 20px 0;">
  <img src="{{ site.baseurl }}/assets/images/settings_verify.png" alt="Einstellungsübersicht" style="width: 48%;" class="shadow">
</div>

> 📬 **Verifizierungsprozess**  
> Bei Anforderung einer neuen Verifizierungs-E-Mail erhält der Nutzer diese in folgendem Format:
{: .info }

![Beispiel Verifizierungs-E-Mail]({{ site.baseurl }}/assets/images/settings_verify_email.png){: .border }

---

## **5. Passwort Generator** 🔐

**Individuelle Passworterstellung**  
Erzeugen Sie sichere Passwörter nach Maß mit folgenden Konfigurationsoptionen:

- **Zeichentyp-Auswahl**  
  Kombination aus Groß-/Kleinbuchstaben, Zahlen und Sonderzeichen
- **Optionale Komponenten**  
  Einzelne Charaktergruppen per Toggle aktivierbar
- **Längenvorgabe**  
  Flexible Einstellung der Passwortlänge (8-16 Zeichen)

**Workflow-Optimierungen**  
- **Echtzeit-Generierung**  
  Sofortige Anzeige des erstellten Passworts
- **Ein-Klick-Kopierfunktion**  
  Direkte Übernahme in die Zwischenablage

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