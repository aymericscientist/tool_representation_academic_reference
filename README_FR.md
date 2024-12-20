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


