# RAG Chatbot FAQ - Retrieval-Augmented Generation for Conversational AI

## Description

Ce projet implémente un chatbot de type **RAG (Retrieval-Augmented Generation)**, conçu pour répondre à des questions en utilisant une base de connaissances pré-existante sous forme de conversations. Le chatbot récupère des conversations pertinentes à partir d'une base de données, puis génère des réponses adaptées en utilisant un modèle de langage avancé.

Le système combine deux technologies puissantes :
1. **Récupération de connaissances (Retrieval)** : Le chatbot recherche dans les données existantes des éléments similaires à la question posée par l'utilisateur.
2. **Génération de réponses (Generation)** : Le modèle de langage génère des réponses adaptées à la question en se basant sur les informations récupérées.

Ce projet peut être utilisé pour construire des **FAQ dynamiques** où les réponses aux questions sont générées en fonction des conversations passées.

## Fonctionnalités

- **Récupération de données** : Le chatbot recherche des conversations pertinentes à partir d'un fichier JSONL contenant des dialogues.
- **Modèle de langage Ollama** : Utilisation du modèle **gemma** via `Langchain` pour générer des réponses intelligentes et contextuelles.
- **Embeddings de texte** : Conversion des messages en vecteurs (embeddings) pour une comparaison rapide de la similarité des textes.
- **Réponses dynamiques** : Le chatbot génère des réponses fluides et naturelles, adaptées aux questions spécifiques posées par l'utilisateur.

## Prérequis

Avant d'exécuter le projet, tu dois installer les dépendances suivantes :
1. **Ollama** : Logiciel permettant d'utiliser des modèles de langage puissants (comme `gemma`).
2. **Langchain** : Bibliothèque pour interagir avec le modèle Ollama.
3. **Sentence-Transformers** : Pour calculer les embeddings des messages.

### Installation des dépendances

Tu peux installer les dépendances nécessaires avec les commandes suivantes :

1. Installer Ollama
2. Installer les bibliothèques Python nécessaires (`langchain-ollama` et `sentence-transformers`)

## Structure du Code

### 1. **Chargement et Préparation des Données**
Le projet commence par charger un fichier JSONL contenant des conversations. Chaque ligne du fichier représente une conversation sous forme de texte brut.

### 2. **Conversion des Conversations**
Les conversations sont transformées en une structure de données où chaque message est étiqueté comme appartenant à l'utilisateur ou à l'assistant.

### 3. **Calcul des Embeddings**
Les textes des utilisateurs et des assistants sont convertis en embeddings vectoriels, permettant ainsi de comparer les messages en fonction de leur similarité.

### 4. **Recherche de Réponses Similaires**
Le système utilise la similarité cosinus pour comparer les embeddings des messages avec la requête de l'utilisateur.

### 5. **Génération de Réponses**
Une fois les conversations similaires récupérées, le modèle génère une réponse en se basant sur le contexte trouvé.

### 6. **Exemple d'Utilisation**
Le chatbot peut répondre à des questions posées par les utilisateurs en recherchant les conversations pertinentes et en générant des réponses dynamiques basées sur ces informations.

## Conclusion

Ce projet démontre l'utilisation d'un chatbot **RAG** pour des **FAQ dynamiques**. Grâce à la combinaison de la recherche de connaissances et de la génération de texte, le système est capable de fournir des réponses adaptées en temps réel aux questions posées par les utilisateurs. Il peut être facilement étendu pour intégrer davantage de données ou de modèles de langage.
