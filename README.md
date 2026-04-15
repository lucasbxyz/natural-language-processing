# Natural Language Processing – Yelp Reviews

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/lucasbxyz/natural-language-processing/HEAD)

Klassifikation von Yelp-Reviews als 1-Stern oder 5-Sterne anhand des Textinhalts. Zum Einsatz kommen NLP-Techniken wie Bag of Words und TF-IDF in Kombination mit einem Naive Bayes Classifier sowie einem Pipeline-Ansatz.

## Ausführung

1. Auf den **Binder Badge** oben klicken — die Umgebung startet automatisch.
2. Im Jupyter-Interface das Notebook `3-Nlp_Projekt.ipynb` öffnen.
3. **Cell → Run All** ausführen (oder Zellen einzeln mit Shift+Enter durchlaufen).
4. Die Ausführung dauert ca. 1–2 Minuten.

## Erwartete Ergebnisse

- **Explorative Analyse:** Histogramme der Bewertungsverteilung, Textlängen-Analyse, Heatmap der Feature-Korrelationen.
- **Modell 1 — CountVectorizer + Naive Bayes:**

| Metrik    | Klasse 1 (1-Stern) | Klasse 5 (5-Sterne) |
|-----------|--------------------|---------------------|
| Precision | 0.88               | 0.93                |
| Recall    | 0.70               | 0.98                |
| F1-Score  | 0.78               | 0.96                |

- **Gesamtgenauigkeit:** ca. **93 %**

- **Modell 2 — TF-IDF Pipeline:** Zum Vergleich wird ein Modell mit TF-IDF-Transformation trainiert. Die TF-IDF-Pipeline zeigt hier etwas niedrigere Werte (ca. 81 % Accuracy), da der einfache Bag-of-Words-Ansatz für diese binäre Klassifikation bereits sehr effektiv ist.

## Dateien

| Datei | Beschreibung |
|-------|-------------|
| `3-Nlp_Projekt.ipynb` | Jupyter Notebook mit der Analyse |
| `Yelp.csv` | Yelp-Review-Datensatz |
| `requirements.txt` | Python-Abhängigkeiten für Binder |
