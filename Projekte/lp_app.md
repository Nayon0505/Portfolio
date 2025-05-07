---
title: LP Sensitivity Analysis Interface – Python
nav_order: 4
---

<details open markdown="block">
{: .text-delta }
<summary>Inhaltsverzeichnis</summary>
+ ToC
{: toc }
</details>

---

# LP Sensitivity Analysis

Dieses Projekt beschäftigt sich mit der Sensitivitätsanalyse von linearen Optimierungsmodellen. In einem interaktiven Jupyter-Notebook wird veranschaulicht, wie sich kleine Änderungen an Parametern – insbesondere an den Koeffizienten der Zielfunktion und Nebenbedingungen – auf die optimale Lösung eines linearen Programms auswirken.

---

## Projektinhalte

- **Modellierung eines linearen Optimierungsproblems**  
  Formulierung von Entscheidungsvariablen, Zielgrößen und Restriktionen zur Lösung eines praxisnahen Optimierungsproblems.

- **Sensitivitätsanalyse**  
  Analyse der Stabilität und Robustheit der optimalen Lösung bei Änderungen der Eingabedaten.  
  - Berechnung von Schattenpreisen und Durchführung dualer Auswertungen  
  - Identifikation kritischer Parameter, die die Lösung maßgeblich beeinflussen

- **Anwendung & Visualisierung**  
  Veranschaulichung der Auswirkungen mit Hilfe von realen oder simulierten Datensätzen  
  - Darstellung der Ergebnisse mittels anschaulicher Diagramme und Visualisierungen

- **Praxisrelevanz**  
  Übertragung der Ergebnisse auf konkrete Anwendungsbereiche wie Ressourcenallokation, Produktionsplanung oder strategische Entscheidungsprozesse

---

## Prototyp

**Einblick in die interaktive Anwendung:**

![LP Case]({{ site.baseurl }}/assets/images/lp_case.png)

Nehmen wir als Beispiel zwei Variablen *a* und *b* mit den Zielkoeffizienten *a = 3* und *b = 4*. Die Nebenbedingungen sind wie folgt definiert:

- \(1 \cdot a \leq 40\)  
- \(1 \cdot b \leq 60\)  
- \(2 \cdot a + 1 \cdot b \leq 100\)

---

![LP Zero]({{ site.baseurl }}/assets/images/lp_zero.png)

Basierend auf diesen Parametern ergibt sich eine erste optimale Lösung:

---

![LP One]({{ site.baseurl }}/assets/images/lp_one.png)
![LP Ergänzen]({{ site.baseurl }}/assets/images/lp_ergänzen.png)

Nun erhöhen wir den Wert von *a* deutlich – von 3 auf 9 – also über die zulässige Toleranz von 5,01 hinaus. Alle übrigen Parameter bleiben unverändert. Ziel ist es, zu analysieren, wie sich diese Änderung auf das Ergebnis auswirkt.

---

![LP Drei]({{ site.baseurl }}/assets/images/lp_three.png)

Die Abbildungen zeigen: Durch die Überschreitung der zulässigen Erhöhung verändert sich die optimale Lösung sichtbar.

---

![Diagramm Vergleich]({{ site.baseurl }}/assets/images/lp_diagramm.png)

Zum Vergleich wird *a* nun lediglich von 3 auf 8 erhöht – innerhalb der zulässigen Schwankungsbreite. Die restlichen Parameter bleiben gleich.

---

![Vergleich Eins]({{ site.baseurl }}/assets/images/lp_vergleich_one.png)

Hier zeigt sich: Die Struktur der optimalen Lösung bleibt stabil. Zwar steigt der Profit, das Produktionsvolumen bleibt jedoch konstant.

---

![Vergleich Zwei]({{ site.baseurl }}/assets/images/lp_vergleich_two.png)


---

## Technologien

- **Jupyter Notebook** – interaktive Analyseumgebung
- **Python** – Implementierung der Modelle und Analysen
- **Optimierungsbibliotheken** – u.a. *PuLP* zur Lösung linearer Programme

---

Diese Arbeit zeigt, wie mithilfe mathematischer Optimierung und gezielter Sensitivitätsanalysen robuste Entscheidungen auch unter Unsicherheit fundiert getroffen werden können.

---

## Kontakt

Falls Sie Fragen haben oder mehr erfahren möchten, können Sie mich gerne kontaktieren:

[![Email](https://img.shields.io/badge/-lenz.nayon@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white "E-Mail senden")](mailto:lenz.nayon@gmail.com)  
[![LinkedIn](https://img.shields.io/badge/-Nayon%20Lenz%20-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nayon-lenz-92792530b/)  
[![GitHub](https://img.shields.io/badge/-@Nayon0505-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Nayon0505)

---

**Vielen Dank für Ihr Interesse!**
