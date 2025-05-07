---
title: FeelSave
parent: Projekte
nav_order: 0
---
<details open markdown="block">
{: .text-delta }
<summary>Table of contents</summary>
+ ToC
{: toc }
</details>

---

<div style="display: flex; align-items: center; gap: 20px;">
  <h1>FeelSave</h1>
  <img src="{{ site.baseurl }}/assets/images/Icon_MountainKeys.png" alt="Icon" style="height: 80px; width: auto;">
</div>

FeelSave wurde von mir im Rahmen eines meiner Kurse entwickelt. Die Android App, porgrammiet mit Java und XML bietet eine Sicherheitslösung für Menschen, die beispielsweise oft in der Nacht oder in abgelegenen Orten unterwegs sind. Die ,,unfair advantage" also, das heraustechende an der App ist der Button, welcher gedrückt werden kann sobald man sich unsicher fühlt. Man hält diesen Button fest und sobald etwas passiert und der Button losgelassen wird treten Schutzmechanismen ein. (Standorttracking, Notrufe usw.) Im folgendem Teil erläuter ich die Software. 

Zudem entwickelten 3 meiner Komolitonen und ich eine Infoseite für FeelSave mithilfe von HTML, CSS, Bootstrap und JavaScript.

Link zur Seite hier: <a href="https://nayon0505.github.io/FeelSave-Infoseite/"> FeelSave/Info </a>


![Beschreibung des GIFs]()

<video 
  src="{{ site.baseurl }}/assets/images/safemode_feelsave.mp4" 
  autoplay 
  loop 
  muted 
  playsinline 
  style="max-width: 100%; height: auto;"
>
  Dein Browser unterstützt das Video-Tag nicht.
</video>

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
[![Email](https://img.shields.io/badge/-lenz.nayon@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:lenz.nayon@gmail.com)
[![LinkedIn](https://img.shields.io/badge/-Nayon%20Lenz%20-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](www.linkedin.com/in/nayon-lenz-92792530b)
[![GitHub](https://img.shields.io/badge/-@Nayon0505-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Nayon0505)

--- 

Vielen Dank für's Anschauen meines Projektes!