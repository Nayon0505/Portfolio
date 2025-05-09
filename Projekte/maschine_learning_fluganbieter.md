---
title: Machine Learning Model - Fluganbieterrezensionen
nav_order: 3
---

<details open markdown="block">
{: .text-delta }
<summary>Table of contents</summary>
+ ToC
{: toc }
</details>

---

# Machine Learning: Predicting Customer Satisfaction

In diesem Projekt führten mein Projektpartner und ich eine umfassende Analyse von Fluggastreviews durch, um Faktoren zu identifizieren, die die Zufriedenheit von Passagier:innen im Luftverkehr maßgeblich beeinflussen.

Ziel war die Entwicklung eines Prognosemodells zur Vorhersage künftiger Kundenzufriedenheit – auf Basis realer Umfragedaten. Vor dem Modelltraining führten wir eine detaillierte **Korrelationsanalyse** durch, um herauszufinden, welche Merkmale besonders stark mit dem Zufriedenheitswert zusammenhängen. Diese Variablen wurden anschließend gezielt als **Prädiktoren** im Modell verwendet.

👉 Das vollständige Projekt ist auf Kaggle verfügbar:

[![Kaggle](https://img.shields.io/badge/-Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/code/nayon0505/airline-passenger-satisfaction1/notebook)
{: .attention }

---

## Einblicke in das Projekt

Ein Blick auf den zugrunde liegenden Datensatz zeigt die Struktur und die enthaltenen Features:

![Datensatzübersicht]({{ site.baseurl }}/assets/images/ml_fp_overview.png)

Zur Modellierung testeten wir insgesamt **drei unterschiedliche Machine-Learning-Modelle**. Die folgende Grafik zeigt den direkten Vergleich der Modellgüte:

![Modellvergleich]({{ site.baseurl }}/assets/images/ml_fp_modellvergleich.png)

Zur Bewertung der Vorhersagegenauigkeit kommt abschließend die **Konfusionsmatrix** zum Einsatz – ein bewährtes Tool zur Analyse der Klassifikationsleistung:

![Konfusionsmatrix]({{ site.baseurl }}/assets/images/ml_fp_matrix.png)

---

## Technologien und Methoden

- **Python / Pandas / NumPy** – für Datenverarbeitung und Feature Engineering
- **Scikit-learn** – für Modelltraining, Evaluation und Hyperparameter-Tuning
- **Matplotlib / Seaborn** – zur visuellen Darstellung der Zusammenhänge
- **Kaggle Notebooks** – zur Veröffentlichung und interaktiven Nachvollziehbarkeit

---

## Kontakt

Bei Fragen oder Interesse an einer Zusammenarbeit:

[![Email](https://img.shields.io/badge/-lenz.nayon@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:lenz.nayon@gmail.com)
[![LinkedIn](https://img.shields.io/badge/-Nayon%20Lenz%20-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nayon-lenz-92792530b/)
[![GitHub](https://img.shields.io/badge/-@Nayon0505-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Nayon0505)

---

**Vielen Dank für Ihr Interesse!**
