# Python Script: DOI Resolution and Metadata Processing

## Overview
This Python script automates the process of resolving DOIs (Digital Object Identifiers) and retrieving metadata for academic references from a `.txt` file. It supports:

- Resolving DOIs via the CrossRef API.
- Fetching metadata such as title, journal, authors, pISSN, and eISSN.
- Matching journals with the FNEGE 2022 ranking.
- Calculating similarity indices between the source reference and retrieved metadata (Title, Journal).
- Exporting results to an Excel file with conditional formatting.

The script is designed to handle large datasets efficiently with multithreading and progress indicators.

---

## Features

1. **DOI Resolution**:
   - Uses the CrossRef API to resolve DOIs for references provided in a `.txt` file.

2. **Metadata Retrieval**:
   - Fetches metadata for each resolved DOI, including Title, Journal, Authors, pISSN, and eISSN.

3. **FNEGE 2022 Ranking**:
   - Matches journal metadata against an external FNEGE 2022 ranking file and adds the corresponding ranking to the output.

4. **Similarity Indices**:
   - Calculates similarity between the source reference and the resolved metadata (Title and Journal).

5. **Excel Export with Conditional Formatting**:
   - Exports the results to an Excel file with:
     - Highlighted similarity scores based on thresholds.
     - Progress tracking during export.

6. **Progress Indicators**:
   - Uses `tqdm` to display progress bars for key operations.

7. **Multithreading**:
   - Processes multiple API requests simultaneously to improve performance.

---

## Requirements

### Dependencies
The script requires the following Python packages:

- `requests`
- `pandas`
- `openpyxl`
- `tqdm`
- `tkinter`
- `queue`

Install the dependencies with:
```bash
pip install requests pandas openpyxl tqdm
```

### External Files
1. **Input File**: A `.txt` file containing references (one reference per line).
2. **FNEGE File**: The Excel file containing journal rankings is automatically downloaded from GitHub.

---

## Usage

1. Clone this repository:
   ```bash
   git clone <repository_url>
   cd <repository_folder>
   ```

2. Run the script:
   ```bash
   python <script_name>.py
   ```

3. Follow the prompts to:
   - Select the `.txt` file containing the references.

4. The script will:
   - Resolve DOIs.
   - Fetch metadata.
   - Match the FNEGE ranking.
   - Calculate similarity indices.
   - Export the results to an Excel file (`_resolved_dois.xlsx`).

---

## Output

### Excel File
The output file contains the following columns:

- **Source Reference**: The original reference from the `.txt` file.
- **DOI**: Resolved DOI for the reference.
- **Title**: Title retrieved from the DOI.
- **Journal**: Journal name retrieved from the DOI.
- **Authors**: Authors retrieved from the DOI.
- **pISSN_PRINT**: Print ISSN.
- **eISSN**: Electronic ISSN.
- **Classement FNEGE 2022**: Journal ranking from the FNEGE 2022 file.
- **Similarity (Source vs Title)**: Similarity score between the source reference and the title.
- **Similarity (Source vs Journal)**: Similarity score between the source reference and the journal.

### Conditional Formatting
- **Green**: Strong similarity (80-100%).
- **Orange**: Moderate similarity (60-79%).
- **Red**: Low similarity (<60%).

---

## License
This project is licensed under the Apache License 2.0.

---

## Contributing
Feel free to open issues or submit pull requests for bug fixes, improvements, or additional features.

---

## Author
Developed by aymericscientist

---

# Script Python : Résolution des DOI et traitement des métadonnées

## Vue d'ensemble
Ce script Python automatise le processus de résolution des DOI (Digital Object Identifiers) et la récupération des métadonnées pour des références académiques à partir d'un fichier `.txt`. Il prend en charge :

- La résolution des DOI via l'API CrossRef.
- La récupération des métadonnées telles que le titre, la revue, les auteurs, le pISSN et le eISSN.
- La correspondance des revues avec le classement FNEGE 2022.
- Le calcul d'indices de similarité entre la référence source et les métadonnées récupérées (Titre, Revue).
- L'exportation des résultats dans un fichier Excel avec mise en forme conditionnelle.

Le script est conçu pour gérer efficacement de grands ensembles de données grâce au multithreading et aux indicateurs de progression.

---

## Fonctionnalités

1. **Résolution de DOI** :
   - Utilise l'API CrossRef pour résoudre les DOI des références fournies dans un fichier `.txt`.

2. **Récupération des Métadonnées** :
   - Récupère les métadonnées pour chaque DOI résolu, y compris le Titre, la Revue, les Auteurs, le pISSN et le eISSN.

3. **Classement FNEGE 2022** :
   - Associe les métadonnées des revues à un fichier de classement FNEGE 2022 externe et ajoute le classement correspondant dans le résultat.

4. **Indices de Similarité** :
   - Calcule la similarité entre la référence source et les métadonnées résolues (Titre et Revue).

5. **Exportation Excel avec Mise en Forme Conditionnelle** :
   - Exporte les résultats dans un fichier Excel avec :
     - Mise en surbrillance des scores de similarité en fonction des seuils.
     - Suivi de progression pendant l'exportation.

6. **Indicateurs de Progression** :
   - Utilise `tqdm` pour afficher des barres de progression pour les opérations clés.

7. **Multithreading** :
   - Traite plusieurs requêtes API simultanément pour améliorer les performances.

---

## Prérequis

### Dépendances
Le script nécessite les packages Python suivants :

- `requests`
- `pandas`
- `openpyxl`
- `tqdm`
- `tkinter`
- `queue`

Installez les dépendances avec :
```bash
pip install requests pandas openpyxl tqdm
```

### Fichiers Externes
1. **Fichier d'Entrée** : Un fichier `.txt` contenant des références (une référence par ligne).
2. **Fichier FNEGE** : Le fichier Excel contenant les classements des revues est automatiquement téléchargé depuis GitHub.

---

## Utilisation

1. Clonez ce dépôt :
   ```bash
   git clone <repository_url>
   cd <repository_folder>
   ```

2. Lancez le script :
   ```bash
   python <script_name>.py
   ```

3. Suivez les invites pour :
   - Sélectionner le fichier `.txt` contenant les références.

4. Le script va :
   - Résoudre les DOI.
   - Récupérer les métadonnées.
   - Associer le classement FNEGE.
   - Calculer les indices de similarité.
   - Exporter les résultats dans un fichier Excel (`_resolved_dois.xlsx`).

---

## Résultats

### Fichier Excel
Le fichier de sortie contient les colonnes suivantes :

- **Source Reference** : La référence originale provenant du fichier `.txt`.
- **DOI** : DOI résolu pour la référence.
- **Title** : Titre récupéré à partir du DOI.
- **Journal** : Nom de la revue récupéré à partir du DOI.
- **Authors** : Auteurs récupérés à partir du DOI.
- **pISSN_PRINT** : ISSN imprimé.
- **eISSN** : ISSN électronique.
- **Classement FNEGE 2022** : Classement de la revue dans le fichier FNEGE 2022.
- **Similarity (Source vs Title)** : Score de similarité entre la référence source et le titre.
- **Similarity (Source vs Journal)** : Score de similarité entre la référence source et la revue.

### Mise en Forme Conditionnelle
- **Vert** : Similarité forte (80-100%).
- **Orange** : Similarité modérée (60-79%).
- **Rouge** : Faible similarité (<60%).

---

## Licence
Ce projet est sous licence Apache 2.0.

---

## Contribuer
N'hésitez pas à ouvrir des tickets ou à soumettre des pull requests pour corriger des bugs, apporter des améliorations ou ajouter des fonctionnalités supplémentaires.

---

## Auteur
Développé par aymericscientist

