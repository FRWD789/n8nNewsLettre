# Journal de bord
### Ressources Utilisées
- Documentation n8n : Nœuds Function, Merge, ChatGPT, RSS, Email
- ChatGPT pour génération de contenu et débogage
- Documentation OpenAI pour optimisation des prompts
- Tailwind CSS + CSS vanilla pour styling email
- IA:claude+chatGPT pour debuger

## Semaine du 17/11/2025
- Nom : Maher Ben Hdibi
- Tâches réalisées : Installation de n8n, création du workflow Google Sheets → Gmail (lab01)
- Apprentissages : Comment connecter Google Sheets et Gmail dans n8n
- Apprentissages fait avec L'ia :  Installation de n8n, création d'un workflow sur n8n
- Difficultés rencontrées : Aucune, tout a fonctionné
- Objectifs semaine suivante : 
    - Génération automatique du contenu de la newsletter avec ChatGPT (ou un agent AI), tester l’envoi automatique
    - Adapter le contenu selon un contexte précis ou un template donné

## Semaine du 24/11/2025
- Nom : Maher Ben Hdibi
### Tâches Réalisées

**Workflow n8n**
- Intégration de nœuds avancés (edit fields, OpenAI) pour enrichir les données
- Merge des sorties pour automatiser l'envoi d'emails

**Mise en place d'une automation de newsletter**
- Configuration du workflow automatique de bout en bout
- Intégration des services externes (OpenAI)

### Apprentissages

- Connexion et synchronisation entre Google Sheets et Gmail via n8n
- Utilisation de nœuds de transformation de données et de fusion (Merge)
- Automatisation complète du cycle d'envoi d'emails avec données combinées
- Création de workflows n8n assistée par IA
- Génération automatique du contenu de newsletter via OpenAI

### Difficultés Rencontrées

Erreurs de formatage dues aux sorties différentes de plusieurs nœuds
Nécessité d’harmoniser les données avant le Merge

### Objectifs pour la Semaine Suivante

- Créer un template HTML personnalisé pour la newsletter
- Effectuer des tests complets d'envoi automatique avec le template final

## Semaine du 01/12/2025
- Nom : Maher Ben Hdibi
### Tâches Réalisées

**Optimisation du workflow de newsletter avec RSS**
- Migration de la source de données : open Ai → RSS Feed (15 articles par jour)
- Restructuration complète du workflow pour gérer plusieurs items
- Architecture finale : `Cron → RSS Read → Function (format) → ChatGPT  → Function (HTML generator)→Google Sheet →Merge → Email`

**Développement du template HTML professionnel**
- Design minimaliste et moderne avec gradient violet
- Section "Executive Summary" affichant le résumé généré par ChatGPT
- Section "Today's Stories" listant tous les articles RSS avec métadonnées
- Responsive design pour tous les appareils
- Styles inline pour compatibilité email clients

**Intégration ChatGPT + RSS**
- Injection du résumé ChatGPT dans le template HTML
- Agrégation des 15 articles RSS avant envoi à ChatGPT (1 appel vs 15)
- Formatage automatique du contenu ChatGPT (markdown → HTML)
- Séparation claire Executive Summary / Full Stories

**Gestion des données**
- Création d'une fonction "Format Items" pour préparer les données pour ChatGPT
- Passage des données complètes au générateur HTML final

### Apprentissages
- Architecture de workflows complexes avec multiple sources de données
- Gestion des flux de données entre nœuds ChatGPT et générateurs de contenu
- Agrégation de données avant traitement IA (optimisation coûts et performance)
- Création de templates HTML avec injection de données dynamiques
- Formatage de réponses IA pour intégration HTML
- Manipulation des structures de données imbriquées dans n8n
- Design d'emails professionnels avec gradients CSS et typographie moderne
### Difficultés Rencontrées
- **Extraction des données ChatGPT** : Structure de réponse complexe `output[0].content[0].text`
- **Passage des données RSS** : Les articles n'étaient pas transmis au nœud final (architecture de workflow incorrecte)
- **Type casting** : Erreur `text.replace is not a function` - nécessité de convertir les données en string
- **Merge de données hétérogènes** : Fusion du résumé ChatGPT + liste d'articles RSS + métadonnées
- **Filtrage des items** : Distinction entre les données ChatGPT et les articles RSS pour éviter les doublons
### Objectifs semaine suivante : 
 **Nouvelle Newsletter Spécialisée** : Music Releases Aggregator
- Spotify - Nouvelles pistes/playlists (API Spotify Web)
- SoundCloud - Nouveaux tracks d'artistes suivis (API SoundCloud)
- Beatport - Nouveaux releases et charts électronique (Web scraping ou API)
- News électronique générale - House, Afro-House, Deep Tech (RSS feeds + sources spécialisées)
