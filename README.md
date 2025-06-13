# Projet de scraping Python avec Jenkins CI/CD

Ce projet extrait automatiquement une liste de langages de programmation depuis Wikipédia à l'aide de Python, et utilise Jenkins pour automatiser l'installation, l'exécution et l'archivage des résultats.

---

## Contenu du projet

```
.
├── scraper.py             # Script Python de scraping
├── requirements.txt       # Liste des dépendances à installer
├── Jenkinsfile            # Définition du pipeline CI/CD Jenkins
├── data.csv               # Fichier généré (archivé par Jenkins)
```

---

## Technologies utilisées

- Python 3.12
- requests
- beautifulsoup4
- lxml
- pandas
- Jenkins (pipeline déclaratif)

---

## Fonctionnement du pipeline Jenkins

Le pipeline CI/CD est défini dans le fichier `Jenkinsfile` et exécute automatiquement les étapes suivantes :

1. Installation des dépendances via `requirements.txt`
2. Exécution du script Python `scraper.py`
3. Génération du fichier `data.csv` contenant la liste des langages
4. Archivage de `data.csv` en tant qu’artefact dans Jenkins

---

## Tester localement

Avant de lancer sur Jenkins, vous pouvez tester en local :

```bash
pip install -r requirements.txt
python scraper.py
```

Vous obtiendrez un fichier `data.csv` dans le répertoire courant.

---

## Exemple de sortie

```
Fichier 'data.csv' généré avec 336 langages.
```

Le fichier `data.csv` est archivé et téléchargeable dans Jenkins à la fin du pipeline.

---

## Intégration GitHub + Jenkins

Un webhook GitHub est configuré pour déclencher le pipeline Jenkins à chaque `git push` sur la branche `main`.

---

## Objectif pédagogique

Ce projet démontre :
- L'utilisation de BeautifulSoup et Pandas pour le scraping web
- La mise en place d’un pipeline Jenkins déclaratif
- La gestion des artefacts dans Jenkins
- L’application des pratiques DevOps (CI/CD) avec Python

---

## Auteur

Hanane Chaouche – Étudiante en développement Big Data  
Collège Bois-de-Boulogne

