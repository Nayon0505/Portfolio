---
title: LP Sensitivity Analysis Interface
parent: Projekte
nav_order: 3
---

<div style="display: flex; align-items: center; gap: 20px;">
  <h1>Passwort Manager</h1>
  <img src="{{ site.baseurl }}/assets/images/Icon_MountainKeys.png" alt="Icon" style="height: 80px; width: auto;">
</div>

---

# LP Sensitivity Analysis

Dieses Projekt befasst sich mit der Untersuchung der Sensitivität von Lösungen in einem linearen Optimierungsmodell. Anhand eines Jupyter-Notebooks wird demonstriert, wie sich kleine Veränderungen in den Parametern – etwa in den Koeffizienten der Ziel- und Nebenbedingungen – auf die optimale Lösung eines linearen Programms auswirken.

## Projektinhalte

- **Modellierung eines linearen Optimierungsproblems:**  
  Formulierung von Entscheidungsvariablen, Zielfunktionen und Nebenbedingungen, um ein praxisnahes Optimierungsproblem zu lösen.

- **Sensitivitätsanalyse:**  
  Untersuchung der Robustheit der optimalen Lösung gegenüber Änderungen der Eingabedaten.  
  - Berechnung von Schattenpreisen und Durchführung dualer Analysen.  
  - Identifikation kritischer Parameter, die maßgeblich den Ergebnisbereich beeinflussen.

- **Anwendung und Visualisierung:**  
  Einsatz von realen oder simulierten Datensätzen, um die praktische Relevanz der Sensitivitätsanalyse aufzuzeigen.  
  Anschauliche Darstellung der Ergebnisse mit Diagrammen und Grafiken, die unterschiedliche Szenarien illustrieren.

- **Praxisrelevanz:**  
  Ableitung von Erkenntnissen, die in Bereichen wie Ressourcenallokation, Produktionsplanung und strategischer Entscheidungsfindung von Bedeutung sind.  
  Demonstration, wie durch gezielte Analyse robuster und fundierter Entscheidungen getroffen werden können.

## Prototyp

Die Anwendung sieht wie folgt aus.
![Diagramm]({{ site.baseurl }}/assets/images/lp_case.png)

>Ein Beispiel.

>Nehmen wir an, wir haben die Varriablen *a* und *b*, die Objective coefficients sind *a = 3* und *b = 4*.
>Außerdem nehmen wir für das beispiel die folgenden Constraints: 
>1 * a <= 40;
>1 * b <= 60;
>2 * a + 1* b <= 100
{: .info }

![Diagramm]({{ site.baseurl }}/assets/images/lp_zero.png)

>Folgend bekommen wir diese Ergebnisse.
{: .info }

![Diagramm]({{ site.baseurl }}/assets/images/lp_one.png)
![Diagramm]({{ site.baseurl }}/assets/images/lp_ergänzen.png)

>Nun erhöhen wir beispielsweise den Wert von a über die zulässige Erhöhung von 5,01, um zu untersuchen, wie sich die optimale Lösung verändert. 
>Dabei bleiben alle anderen Parameter unverändert; lediglich der Wert von a wird von 3 auf 9 angepasst.
{: .info }

![Diagramm]({{ site.baseurl }}/assets/images/lp_three.png)

>Wenn wir alles vergleich, entstehen diese Abbildungen. 
>Die optimale Lösung verändert sich, da die zulässige Erhöhung überschritten wurde.
{: .info }

![Diagramm]({{ site.baseurl }}/assets/images/lp_diagramm.png)

>Zum Vergleich erhöhen wir den Startwert von a = 3 nun innerhalb der zulässigen Erhöhung von 5,01.
>Alle anderen Parameter bleiben unverändert; lediglich a wird von 3 auf 8 angepasst.
{: .info }

![Diagramm]({{ site.baseurl }}/assets/images/lp_vergleich_one.png)

>Das Diagramm zeigt, wie erwartet, dass sich die optimale Lösung nicht ändert:
>Zwar variiert der Profit, das Produktionsvolumen bleibt jedoch konstant.
{: .info }

![Diagramm]({{ site.baseurl }}/assets/images/lp_vergleich_two.png)

### Technologien

- **Jupyter Notebook:** Interaktive Ausführung und Visualisierung der Analysen.
- **Python:** Implementierung der Optimierungsmodelle und Sensitivitätsanalysen.
- **Optimierungsbibliotheken:** Einsatz moderner Bibliotheken (z.B. PuLP oder ähnliche), um das lineare Programm zu lösen.

---

## download 

>Gerne können sie sich das Projekt auch genauer anschauen.

><a href="Ablage\lpsensitivityanalysis.ipynb" download class="btn">📥 Download Notebook</a>
{: .download }

---

Diese Arbeit unterstreicht, wie mathematische Optimierung in Verbindung mit Sensitivitätsanalysen dazu beitragen kann, fundierte Entscheidungen in dynamischen und unsicheren Umfeldern zu treffen.

---

## 📧 Kontakt
Falls Sie Fragen haben oder mehr erfahren möchten, können Sie mich gerne kontaktieren:
 
> {: .info }
[![Email](https://img.shields.io/badge/-aniloeker@hotmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:aniloeker@hotmail.com)
[![LinkedIn](https://img.shields.io/badge/-Anil%20Emircan%20Öker-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/anil-emircan-öker-a2878430a)
[![GitHub](https://img.shields.io/badge/-@Emircan1122-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Emircan1122)

--- 

Vielen Dank für's anschauen meines Projektes!