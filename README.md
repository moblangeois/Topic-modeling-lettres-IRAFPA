Analyse de Textes avec NLP et Clustering
Ce projet vise à analyser une collection de lettres académiques, extraire des insights pertinents grâce à des techniques de traitement du langage naturel (NLP) et de clustering, et identifier des thèmes récurrents au fil du temps.

## Dépendances
Le projet utilise plusieurs bibliothèques Python importantes pour le traitement des données, le NLP, le clustering, et la visualisation, dont :

- Pandas pour la manipulation des données
- re (RegEx) pour les expressions régulières
- Collections pour les structures de données avancées
- dotenv pour la gestion des variables d'environnement
- BERTopic pour le topic modeling avancé
- spaCy et nltk pour le NLP
- HDBSCAN et UMAP pour le clustering et la réduction de dimension
- Matplotlib et Seaborn pour la visualisation
- OpenAI pour l'intégration de modèles de langage avancés

## Configuration Initiale
Variables d'environnement : Le code utilise une clé API OpenAI, qui doit être configurée comme une variable d'environnement (OPENAI_API_KEY).
Modèles spaCy : Un modèle spaCy en français (fr_core_news_md) est chargé pour le traitement du langage naturel.
Détection de la langue : Un détecteur de langue est ajouté au pipeline spaCy pour filtrer les phrases non françaises.

## Analyse des Lettres de l'IRAFPA
Le script exécute les étapes suivantes pour analyser le texte des lettres de l'IRAFPA :

- Extraction des Lettres : Les lettres sont extraites d'un fichier texte en utilisant des expressions régulières.
- Nettoyage et Préparation des Données : Les données sont nettoyées et préparées pour l'analyse, y compris le tri par date et la tokenisation des phrases.
- Analyse NLP : Les phrases sont analysées pour retirer celles en langue étrangère, en double, ou ne respectant pas certains critères de longueur ou de contenu.

## Clustering et Topic Modeling
Le projet utilise BERTopic pour le topic modeling, en appliquant différentes techniques pour la représentation des topics, y compris :

- KeyBERT pour l'extraction de mots-clés
- Maximal Marginal Relevance (MMR) pour la diversité des mots-clés
- PartOfSpeech et OpenAI GPT-3.5 Turbo pour des représentations améliorées

Les topics identifiés sont ensuite visualisés et analysés pour comprendre les thèmes principaux et leur évolution dans le temps.
Deux fichiers HTML sont générés pour visualiser les topics et les clusters.
- visualize_documents_all.html : Visualisation de tous les documents et clusters
- visualize_topics_over_time.html : Visualisation des topics et clusters au fil du temps