# Projet 8 : Veille Technique et POC sur le Few-Shot Learning (SetFit)

### Objectif & Résultat Principal

Réalisation d’une veille sur l’efficacité du **Few-Shot Learning**, centrée sur le modèle **SetFit**. Un Proof of Concept (POC) a été mené pour comparer SetFit (F1-Score: 0.87) à une baseline (Régression Logistique, F1-Score: 0.93) sur une tâche de classification de texte.

L'analyse a démontré que **SetFit atteint 93% de la performance de la baseline en n'utilisant que 13% des données d'entraînement** (112 échantillons contre 840), validant son efficacité pour réduire les coûts d'annotation.

---

Ce projet, le huitième du parcours Data Scientist d'OpenClassrooms, est axé sur la veille technologique et la capacité à évaluer l'apport de nouvelles méthodes de modélisation.

*(Note : La mission initiale P8 comprenait un dashboard, qui a été intégré au Projet 7 (Scoring de Crédit) pour créer un projet MLOps complet. Ce repository se concentre donc exclusivement sur la partie Veille Technique et Proof of Concept.)*

### Contexte

La mission consiste à répondre à une demande de la direction : réaliser un état de l’art sur une technique récente de modélisation (moins de 5 ans) pour les données textuelles ou images. L'objectif est d'évaluer si ces nouvelles approches peuvent surpasser ou compléter les modèles "classiques" déjà en place, notamment en termes d'efficacité (coût de calcul, besoin en données).

Cette veille se concentre sur le **Few-Shot Learning**, une approche visant à obtenir de hautes performances avec très peu de données annotées, un enjeu majeur en entreprise pour réduire les coûts d'annotation.

### Missions

* **Réaliser une veille technologique** sur les méthodes récentes en NLP, en se concentrant sur le Few-Shot Learning.
* **Sélectionner une technique** pertinente : **SetFit (Sentence Transformer Fine-tuning)**, pour sa promesse d'efficacité avec peu de données.
* **Établir une baseline performante** : Entraînement d'une Régression Logistique sur des embeddings `all-MiniLM-L6-v2`, en utilisant 100% des données d'entraînement (840 échantillons).
* **Mener un Proof of Concept (POC)** : Entraînement du modèle SetFit sur un sous-ensemble "few-shot" de seulement 112 échantillons (16 par catégorie, soit 13% des données).
* **Comparer les performances** : Évaluation rigoureuse des deux modèles sur le même jeu de test (210 échantillons) en utilisant le **F1-Score pondéré**.
* **Rédiger une note méthodologique** pour synthétiser l'approche, expliquer les concepts de SetFit (apprentissage contrastif + tête de classification) et présenter les conclusions.

### Compétences Développées

* **Veille Technologique et Scientifique :** Capacité à rechercher, analyser et synthétiser des articles de recherche (NLP, Few-Shot Learning).
* **Conception de Proof of Concept (POC) :** Définition d'un protocole expérimental rigoureux pour comparer deux approches de modélisation.
* **Few-Shot Learning (NLP) :** Implémentation de modèles modernes et économes en données avec `setfit`.
* **Maîtrise de l'écosystème Hugging Face :** Utilisation des librairies `sentence-transformers`, `datasets` et `setfit`.
* **Communication Technique :** Rédaction d'une note méthodologique claire pour vulgariser un concept technique complexe et justifier une décision.
* **Analyse Coût/Bénéfice :** Évaluation d'un modèle non seulement sur sa performance brute, mais aussi sur son rapport performance/coût d'annotation.

### Outils et Librairies

* **Langage :** Python
* **Veille / POC :** `setfit`, `datasets` (Hugging Face), `sentence-transformers`
* **Modèle Baseline :** `Scikit-learn` (LogisticRegression, classification_report)
* **Manipulation de Données :** `Pandas`, `NumPy`
* **Outil :** Jupyter Notebook
