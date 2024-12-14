# Python Script: DOI Resolution and Metadata Processing

## Overview (English)
This Python script automates the process of resolving DOIs (Digital Object Identifiers) and retrieving metadata for academic references from a `.txt` file. It supports:

- Resolving DOIs via the CrossRef API.
- Fetching metadata such as title, journal, authors, pISSN, and eISSN.
- Matching journals with the FNEGE 2022 ranking.
- Calculating similarity indices between the source reference and retrieved metadata (Title, Journal).
- Exporting results to an Excel file with conditional formatting.

The script is designed to handle large datasets efficiently with multithreading and progress indicators.

---

## Vue d'ensemble (Français)
Ce script Python automatise le processus de résolution des DOI (Digital Object Identifiers) et la récupération des métadonnées pour des références académiques à partir d'un fichier `.txt`. Il prend en charge :

- La résolution des DOI via l'API CrossRef.
- La récupération des métadonnées telles que le titre, la revue, les auteurs, le pISSN et le eISSN.
- La correspondance des revues avec le classement FNEGE 2022.
- Le calcul d'indices de similarité entre la référence source et les métadonnées récupérées (Titre, Revue).
- L'exportation des résultats dans un fichier Excel avec mise en forme conditionnelle.

Le script est conçu pour gérer efficacement de grands ensembles de données grâce au multithreading et aux indicateurs de progression.

---

## Features (English) / Fonctionnalités (Français)

1. **DOI Resolution** / **Résolution de DOI**:
   - Uses the CrossRef API to resolve DOIs for references provided in a `.txt` file.
   - Utilise l'API CrossRef pour résoudre les DOI des références fournies dans un fichier `.txt`.

2. **Metadata Retrieval** / **Récupération des Métadonnées**:
   - Fetches metadata for each resolved DOI, including Title, Journal, Authors, pISSN, and eISSN.
   - Récupère les métadonnées pour chaque DOI résolu, y compris le Titre, la Revue, les Auteurs, le pISSN et le eISSN.

3. **FNEGE 2022 Ranking** / **Classement FNEGE 2022**:
   - Matches journal metadata against an external FNEGE 2022 ranking file and adds the corresponding ranking to the output.
   - Associe les métadonnées des revues à un fichier de classement FNEGE 2022 externe et ajoute le classement correspondant dans le résultat.

4. **Similarity Indices** / **Indices de Similarité**:
   - Calculates similarity between the source reference and the resolved metadata (Title and Journal).
   - Calcule la similarité entre la référence source et les métadonnées résolues (Titre et Revue).

5. **Excel Export with Conditional Formatting** / **Exportation Excel avec Mise en Forme Conditionnelle**:
   - Exports the results to an Excel file with:
     - Highlighted similarity scores based on thresholds.
     - Progress tracking during export.
   - Exporte les résultats dans un fichier Excel avec :
     - Mise en surbrillance des scores de similarité en fonction des seuils.
     - Suivi de progression pendant l'exportation.

6. **Progress Indicators** / **Indicateurs de Progression**:
   - Uses `tqdm` to display progress bars for key operations.
   - Utilise `tqdm` pour afficher des barres de progression pour les opérations clés.

7. **Multithreading** / **Multithreading**:
   - Processes multiple API requests simultaneously to improve performance.
   - Traite plusieurs requêtes API simultanément pour améliorer les performances.

---

## Requirements (English) / Prérequis (Français)

### Dependencies / Dépendances
The script requires the following Python packages:
Le script nécessite les packages Python suivants :

- `requests`
- `pandas`
- `openpyxl`
- `tqdm`
- `tkinter`
- `queue`

Install the dependencies with / Installez les dépendances avec :
```bash
pip install requests pandas openpyxl tqdm
```

### External Files / Fichiers Externes
1. **Input File** / **Fichier d'Entrée**: A `.txt` file containing references (one reference per line).
   - Un fichier `.txt` contenant des références (une référence par ligne).
2. **FNEGE File** / **Fichier FNEGE**: An Excel file containing journal rankings (`TITLE`, `pISSN_PRINT`, `eISSN`, and `Classement_2022` columns).
   - Un fichier Excel contenant les classements des revues (`TITLE`, `pISSN_PRINT`, `eISSN`, et `Classement_2022`).

---

## Usage

1. Clone this repository / Clonez ce dépôt :
   ```bash
   git clone <repository_url>
   cd <repository_folder>
   ```

2. Run the script / Lancez le script :
   ```bash
   python <script_name>.py
   ```

3. Follow the prompts to / Suivez les invites pour :
   - Select the `.txt` file containing the references.
   - Sélectionner le fichier `.txt` contenant les références.
   - (Optional) Select the FNEGE 2022 ranking file.
   - (Optionnel) Sélectionner le fichier de classement FNEGE 2022.

4. The script will / Le script va :
   - Resolve DOIs.
   - Résoudre les DOI.
   - Fetch metadata.
   - Récupérer les métadonnées.
   - Match the FNEGE ranking.
   - Associer le classement FNEGE.
   - Calculate similarity indices.
   - Calculer les indices de similarité.
   - Export the results to an Excel file (`_resolved_dois.xlsx`).
   - Exporter les résultats dans un fichier Excel (`_resolved_dois.xlsx`).

---

## Output (English) / Résultats (Français)

### Excel File / Fichier Excel
The output file contains the following columns:
Le fichier de sortie contient les colonnes suivantes :

- **Source Reference**: The original reference from the `.txt` file.
  - La référence originale provenant du fichier `.txt`.
- **DOI**: Resolved DOI for the reference.
  - DOI résolu pour la référence.
- **Title**: Title retrieved from the DOI.
  - Titre récupéré à partir du DOI.
- **Journal**: Journal name retrieved from the DOI.
  - Nom de la revue récupéré à partir du DOI.
- **Authors**: Authors retrieved from the DOI.
  - Auteurs récupérés à partir du DOI.
- **pISSN_PRINT**: Print ISSN.
  - ISSN imprimé.
- **eISSN**: Electronic ISSN.
  - ISSN électronique.
- **Classement FNEGE 2022**: Journal ranking from the FNEGE 2022 file.
  - Classement de la revue dans le fichier FNEGE 2022.
- **Similarity (Source vs Title)**: Similarity score between the source reference and the title.
  - Score de similarité entre la référence source et le titre.
- **Similarity (Source vs Journal)**: Similarity score between the source reference and the journal.
  - Score de similarité entre la référence source et la revue.

---

## License (English) / Licence (Français)
This project is licensed under the Apache License 2.0.
Ce projet est sous licence Apache 2.0.

---

## Contributing (English) / Contribuer (Français)
Feel free to open issues or submit pull requests for bug fixes, improvements, or additional features.
N'hésitez pas à ouvrir des tickets ou à soumettre des pull requests pour corriger des bugs, apporter des améliorations ou ajouter des fonctionnalités supplémentaires.

---

## Author (English) / Auteur (Français)
Developed by aymericscientist
Développé par aymericscientist

