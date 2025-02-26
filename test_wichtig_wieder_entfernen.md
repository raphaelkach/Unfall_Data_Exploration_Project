Hier ein möglicher Fahrplan, wie du die Uni‐Vorgaben (Report, Jupyter Notebook, Vortragsunterlagen und Vortrag) am besten umsetzen könntest. Der Leitgedanke ist dabei, den CRISP-DM-Prozess (oder einen ähnlichen Data-Science-Prozess) strukturiert durchzugehen, um einen roten Faden zu haben und gleichzeitig die formalen Anforderungen (z.B. maximal 2500 Wörter im Report, bestimmte Anzahl an Visualisierungen, Reproduzierbarkeit im Notebook etc.) einzuhalten.

1. Allgemeine Vorgehensweise (CRISP-DM)
Business Understanding

Ziel definieren: Welche Fragestellung möchtest du beantworten? Z.B. „Welche Faktoren tragen besonders stark zu schweren (fatalen) Unfällen bei?“ oder „Kann man die Wahrscheinlichkeit eines Unfalls mit Todesfolge vorhersagen?“
Zielmetrik: Leg fest, ob du z.B. eine Klassifikation (Unfall mit/ohne Todesfolge) oder eine Regression (Anzahl der Todesopfer) machen willst.
Nutzen: Weshalb ist das interessant? (z.B. für Verkehrssicherheitsbehörden, Politik, Versicherungen, …)
Data Understanding

Überblick über alle vorhandenen Datenquellen (siehe deine Tabelle).
Zentrale Identifikatoren: Fast alle Tabellen haben ST_CASE als Schlüssel, zusätzlich manchmal VEH_NO oder PER_NO. Überlege, welche Datensätze du wirklich brauchst und wie du sie verknüpfst.
Erste Exploration:
Wie groß sind die Tabellen?
Welche Spalten sind besonders relevant für deine Fragestellung?
Wie hoch ist der Anteil fehlender Werte?
Da die Datensätze sehr umfangreich sind, macht es Sinn, einen zeitlichen oder thematischen Ausschnitt zu wählen (z.B. nur Unfälle ab 2020) oder sich auf bestimmte Fälle zu konzentrieren (z.B. nur PKW, keine LKW).
Data Preparation

Joins: Verbinde die relevanten Tabellen über ST_CASE (und ggf. VEH_NO, PER_NO).
Feature Engineering:
Kategorische Variablen (z.B. WEATHERNAME, MAN_COLLNAME, DRDISTRACTNAME) in numerische Features umwandeln (One-Hot-Encoding oder Label-Encoding).
Zeitliche Features (z.B. Uhrzeit in „Rush Hour vs. Nicht-Rush Hour“).
Evtl. Aggregation (z.B. Anzahl der beteiligten Fahrzeuge, Anzahl Verletzte/Tote, …).
Datenbereinigung:
Fehlende Werte sinnvoll behandeln (Dropping vs. Imputation).
Duplikate entfernen.
Ausreißer erkennen und ggf. bereinigen.
Modelling

Abhängig von deiner Zielsetzung:
Klassifikation: z.B. Vorhersage „Unfall mit Todesfolge = 1“ vs. „ohne Todesfolge = 0“. Modelle könnten sein Logistic Regression, Random Forest, XGBoost etc.
Regression: z.B. Vorhersage der Anzahl an Todesopfern.
Hyperparameter-Tuning: Cross-Validation, GridSearch oder RandomizedSearch.
Performance-Metriken:
Klassifikation: Accuracy, Precision, Recall, F1-Score, ggf. AUC.
Regression: MSE, MAE, R² etc.
Evaluation

Modellgüte: Wie gut sagt das Modell das Ziel vorher?
Interpretierbarkeit: Feature-Importance-Plot oder SHAP-Werte.
Limitationen: Datenerhebungsprobleme, Bias, fehlende Daten, eingeschränkte Zeiträume, etc.
Deployment bzw. „Reflektion & Ausblick“

Reflektiere: Was lief gut, was könnte man besser machen?
Ausblick: Welche Daten wären zusätzlich hilfreich? Welche weiteren Analysen könnte man anstellen?
2. Report (Artefakt „Report“)
Format & Inhalt
LaTeX/ArXiv-Style mit 2 Spalten (oder das Template, das in Moodle bereitgestellt wurde).
Maximal 2500 Wörter (Tipp: In LaTeX kann man mit einem externen Tool oder später in Word/OpenOffice per Copy/Paste zählen).
Struktur (am besten angelehnt an CRISP-DM, damit du automatisch alle geforderten Punkte abdeckst):
Einleitung (Business Understanding)
Data Understanding
Data Preparation
Modelling
Evaluation
Ergebnisse & Diskussion (Reflektion, Ausblick)
Wichtige Vorgaben:
2–4 aussagekräftige Plots/Diagramme (z.B. Korrelationen, Verteilung von Unfalltagen über die Woche, Modellgüte, Feature Importance etc.).
Du musst nicht zwingend CRISP-DM im Report als Überschriften aufführen, aber es hilft, nichts zu vergessen.
Tipps zum Inhalt
Business Understanding: Hier stellst du kurz den „Auftrag“ oder das „Warum?“ dar.
Data Understanding & Preparation:
Fasse kurz zusammen, welche Daten du tatsächlich genutzt hast (nicht jede Tabelle muss drankommen, nur was relevant ist).
Zeige ggf. eine kleine Beispiel-Tabelle (5 Zeilen).
Zeige in 1–2 Plots die wichtigsten Erkenntnisse (z.B. wie häufig kommt Wettertyp XY vor?).
Modelling & Evaluation:
Zeige, welches Modell du genommen hast, welche Hyperparameter du probiert hast und wie du die Modelle bewertet hast.
1 Plot mit ROC-Kurve oder Confusion Matrix (falls Klassifikation). Oder ein Residuen-Plot (falls Regression).
Fazit: kurze Zusammenfassung, Ausblick.
3. Jupyter Notebook (Artefakt „Jupyter Notebook“)
Anforderungen
Format: .pdf (also Notebook als PDF exportieren) oder du reichst das Notebook selbst plus PDF ein (je nach Vorgabe).
Alle Schritte sollten reproduzierbar sein (d.h. alle Zellen sind ausführbar, Daten können heruntergeladen oder lokal bereitgestellt werden).
Alle Plots und Ergebnisse aus dem Report sollten im Notebook nachvollziehbar sein.
Aufbau
Am besten deckt das Notebook dieselben CRISP-DM-Schritte ab, allerdings kannst du hier mehr Code zeigen und auch Zwischenergebnisse ausgeben.
Achte auf Lesbarkeit:
Überschriften für jeden Abschnitt,
Kommentare im Code,
kurze Erklärtexte in Markdown-Zellen.
Praktische Tipps
Lade die Daten (z.B. aus einem Ordner data/) ein.
Mache alle Preprocessing-Schritte in klar gekennzeichneten Code-Zellen.
Erstelle erste Explorationsplots (Histogramme, Boxplots, Heatmaps).
Baue dein Modell auf, zeige Hyperparameter-Tuning etc.
Speichere ggf. Zwischenergebnisse in .csv oder pickle, damit man nicht alles jedes Mal neu berechnen muss. (Aber Vorsicht mit Speicherplatz und Reproduzierbarkeit.)
4. Vortragsunterlagen (Artefakt „Vortragsunterlagen“)
Format & Inhalt
Format: .pdf (typisch wäre eine PowerPoint/Keynote/LaTeX-Beamer-Präsentation, die dann als PDF exportiert wird).
„Beamer-tauglich“ heißt: große Schrift, nicht zu viel Text, Farbschema einheitlich.
Wesentlich weniger Details als im Report – das soll eher die wichtigsten Ergebnisse und Grafiken enthalten, damit du sie im Vortrag erklären kannst.
Gliederungsvorschlag (ca. 6–10 Folien für 10 Min. Vortrag)
Motivation & Ziel
Datengrundlage (kurzer Überblick)
Methodik (CRISP-DM in 1 Folie oder 2 Folien)
Zentrale Ergebnisse (ggf. 1–2 Grafiken, Modellgüte)
Fazit & Ausblick
5. Vortrag (ca. 10 Min. + 5 Min. Q&A)
Ablauf
Zeitmanagement: 10 Minuten sind schnell vorbei – pro Folie ca. 1–2 Minuten.
Inhaltlich: Das Gleiche wie in den Vortragsunterlagen beschrieben.
Tipps:
Übe den Vortrag vorher, um die Zeit einzuhalten.
Sprich verständlich, nicht zu schnell.
Nenne Fachbegriffe, erkläre sie aber kurz, damit das Publikum folgen kann.
Nutze Blicke zum Publikum, mache kurze Pausen, um wichtige Punkte zu betonen.
Q&A
Häufige Fragen könnten sein:
„Wie bist du mit fehlenden Daten umgegangen?“
„Warum hast du genau dieses Modell gewählt?“
„Wie generalisierbar sind deine Ergebnisse?“
„Welche Daten würdest du noch gerne haben, um das Modell zu verbessern?“
6. Praktische Hinweise
Datenumfang reduzieren

Da du extrem viele CSV-Dateien hast, picke dir das Wichtigste: Meist reicht die Kombination aus accidents.csv (Unfallmerkmale) und vehicle.csv (Fahrzeuginfos) und person.csv (Personeninfos), plus ggf. weather.csv.
Achte darauf, dass du mit ST_CASE die Datensätze verbindest und nicht versehentlich Datensätze vervielfachst.
Klare Fragestellung

Das macht es leichter zu entscheiden, welche Spalten du wirklich brauchst.
Einheitliches Projektverzeichnis

Ordnerstruktur:
sql
Kopieren
/project
  |-- data/ (alle CSVs oder Symlinks zu den Daten)
  |-- notebook/ (Jupyter Notebook)
  |-- report/ (LaTeX-Dateien oder Word)
  |-- slides/ (Vortragsfolien)
So stellst du sicher, dass du nichts durcheinanderbringst.
Wortlimit einhalten

Bei 2500 Wörtern kommst du mit ca. 5–6 Seiten in 2‐Spalten-Layout hin (je nach Formatierung).
Schreib prägnant, nutze ggf. Abbildungen/Tabelle statt Fließtext.
Diagramme

Wähle 2–4 wirklich aussagekräftige Plots:
z.B. Unfallanzahl pro Wochentag oder Tageszeit,
Korrelationsmatrix oder Heatmap,
Feature Importance,
Confusion Matrix (bei Klassifikation).
Vorlage/Template

Wenn deine Uni ein eigenes LaTeX-Template vorgibt, verwende es.
Ansonsten kannst du das arXiv-Template nehmen. Achte darauf, dass das PDF nachher sauber aussieht (Seitenränder, 2 Spalten, Lesbarkeit).
Zusammenfassung
Report: wissenschaftlich-formaler Text mit max. 2500 Wörtern, enthält alle wichtigen Projektschritte (Business Understanding bis Evaluation), inkl. 2–4 Plots.
Jupyter Notebook: ausführbarer Code, der alle Analyseschritte transparent und reproduzierbar zeigt.
Vortragsunterlagen: komprimierte Darstellung (ca. 6–10 Folien) für einen 10-minütigen Vortrag.
Vortrag: klare und prägnante Präsentation, Fokus auf Kernaussagen und Ergebnisse, plus 5 Minuten Q&A.
Mit dieser Vorgehensweise erfüllst du die Uni-Vorgaben und hast zugleich einen „roten Faden“, um dein Data-Science-Projekt effizient umzusetzen. Viel Erfolg!