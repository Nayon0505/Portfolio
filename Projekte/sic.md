---
title: SIC! - Sustainable Innovation Checker – Fullstack Flask App
nav_order: 2
---

<details open markdown="block">
{: .text-delta }
<summary>Inhaltsverzeichnis</summary>
+ ToC
{: toc }
</details>

---

# SIC! – Sustainable Innovation Checker

Im Rahmen dieses Projekts entwickelten mein Projektpartner und ich eine Webanwendung namens **SIC! – Sustainable Innovation Checker** für das EMF-Institut der HWR Berlin.

Als thematischen Schwerpunkt wählten wir das Konzept der **Steuertransparenz**, mit besonderem Fokus auf kleine und mittelständische Unternehmen (KMU) aus der **Gastronomiebranche**.

Die zentrale Zielsetzung bestand in der Entwicklung einer intuitiven, voll funktionsfähigen Anwendung, die es Betrieben ermöglicht:

- ihre Steuertransparenz systematisch zu erfassen,
- effizient zu überprüfen, ob grundlegende steuerrelevante Anforderungen erfüllt sind,
- und bestehende Lücken oder vergessene Pflichtelemente im Steuermanagement zu identifizieren.

Das Tool unterstützt Unternehmen dabei, kritische **Compliance-Risiken sichtbar zu machen** und gezielt zu adressieren.

> 👉 Das vollständige Projekt ist auf unserer GitHub-Pages-Seite öffentlich einsehbar:
>
> [![GitHub Pages](https://img.shields.io/badge/-GitHub%20Pages-181717?style=for-the-badge&logo=github&logoColor=white)](https://nayon0505.github.io/SIC-Projekt/)
{: .attention }

---

## Einblick in die Anwendung

Die Startseite der Anwendung bietet zwei verschiedene Testvarianten:

- **Schnelltest:** sofort und ohne Anmeldung nutzbar  
- **Detaillierter Test:** erfordert Registrierung und Anmeldung

{: .info }

<video 
  src="{{'/assets/videos/startseitesic.mp4' | relative_url }}" 
  autoplay 
  loop 
  muted 
  playsinline 
  controls
  style="max-width: 100%; height: auto;">
  Ihr Browser unterstützt das Video-Tag nicht.
</video>



---

### Anmeldung und Registrierung

Nutzerinnen und Nutzer können sich registrieren und anschließend anmelden. Die Eingaben werden gegen die hinterlegte SQLAlchemy-Datenbank geprüft. Erfolgreiche Logins werden entsprechend bestätigt.

{: .info }

<video 
  src="{{ '/assets/videos/loginsic.mp4' | relative_url }}" 
  autoplay 
  loop 
  muted 
  playsinline 
  controls
  style="max-width: 100%; height: auto;">
  Ihr Browser unterstützt das Video-Tag nicht.
</video>

---


### Tests und Auswertung

Die Testmodule bestehen aus einfachen Frageblöcken zur steuerlichen Transparenz. Es stehen zwei Varianten zur Verfügung:

{: .info }

#### Schnelltest

<video 
  src="{{ '/assets/videos/schnelltestsic.mp4' | relative_url }}" 
  autoplay 
  loop 
  muted 
  playsinline 
  controls
  style="max-width: 100%; height: auto;">
  Ihr Browser unterstützt das Video-Tag nicht.
</video>

#### Ausführlicher Test

<video 
  src="{{ '/assets/videos/detailtestsic.mp4' | relative_url }}" 
  autoplay 
  loop 
  muted 
  playsinline 
  controls
  style="max-width: 100%; height: auto;">
  Ihr Browser unterstützt das Video-Tag nicht.
</video>

Nach Abschluss der Tests werden die Eingaben mithilfe eines **Ampelsystems** (Grün / Gelb / Rot) visuell bewertet. Diese Darstellung bietet eine schnelle Einschätzung zum aktuellen Stand der Steuertransparenz.

Zusätzlich lässt sich ein **individueller PDF-Bericht** generieren, der Folgendes enthält:

- Hinweise zu möglichen Schwachstellen
- Empfehlungen zur Optimierung der Steuercompliance

{: .info }

---


### Benutzerbereich

Nach dem Login erhalten Nutzerinnen und Nutzer Zugang zu ihrem persönlichen Bereich. Dort sind alle bisherigen Testergebnisse gespeichert und können jederzeit eingesehen oder erneut abgerufen werden.

{: .info }

<video 
  src="{{ '/assets/videos/meinbereichsic.mp4' | relative_url }}" 
  autoplay 
  loop 
  muted 
  playsinline 
  controls
  style="max-width: 100%; height: auto;">
  Ihr Browser unterstützt das Video-Tag nicht.
</video>

---

## Kontakt

Bei Rückfragen oder Interesse an weiteren Informationen stehe ich gerne zur Verfügung:

[![Email](https://img.shields.io/badge/-lenz.nayon@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:lenz.nayon@gmail.com)  
[![LinkedIn](https://img.shields.io/badge/-Nayon%20Lenz%20-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nayon-lenz-92792530b)  
[![GitHub](https://img.shields.io/badge/-@Nayon0505-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Nayon0505)

---

Vielen Dank für Ihr Interesse an unserem Projekt!
