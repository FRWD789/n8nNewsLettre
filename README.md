# n8n NewsLettre – Automatisation d'une Newsletter avec n8n

Projet réalisé dans le cadre du **Projet 3 : Explorer une technologie à l'aide de l'intelligence artificielle**. Ce dépôt contient notre exploration de n8n, une plateforme open-source d'automatisation, ainsi que le prototype permettant de générer et envoyer automatiquement une newsletter.

## Équipe

- **Maher Ben Hdibi**

## Sujet du projet

Développer un système automatisé capable de :

- Récupérer du contenu depuis différentes sources (API d'actualités, flux RSS, blogs…)
- Résumer automatiquement les articles via une IA
- Générer un format de newsletter en texte ou HTML
- Envoyer automatiquement l'email via un GMAIL
- Planifier l'envoi (ex. quotidien ou hebdomadaire)

Ce projet explore les capacités de n8n en matière de workflows avancés, intégration API, nodes IA, automatisation d'emails et orchestration/scheduling.

## Fonctionnalités prévues

- Collecte automatique d'articles (HTTP Request, RSS Reader)
- Utilisation d'un modèle IA (OpenAI/Gemini) pour résumer le contenu
- Formatage automatique du texte
- Génération d'un template HTML pour la newsletter
- Envoi avec Email Node
- Planification avec Cron Trigger
- Export JSON des workflows dans le dossier `/workflows/`

## Organisation du dépôt

```
.
├── /workflows/        → Workflows n8n exportés en JSON
├── /docs/             → Notes, captures, schémas
├── journal.md         → Journal de bord hebdomadaire
└── README.md          → Description du projet
```

## Prototype

Le prototype final permettra d'envoyer automatiquement une newsletter contenant une sélection d'actualités générées et résumées par une IA.

Une démonstration de 10 minutes présentera :

- Le workflow n8n et son architecture globale
- Les nodes utilisés et leurs interactions
- Le fonctionnement complet du pipeline
- Les limites et possibilités d'amélioration

## Ressources

**GitHub Repository:** https://github.com/FRWD789/n8nNewsLettre

## Utilisation de l'IA dans le projet

L'IA a été utilisée pour :

- Comparer les technologies d'automatisation (n8n, Zapier, Make)
- Définir l'architecture du workflow
- Générer ou corriger du code dans les nodes Function
- Documenter le projet (README, journal, planification)
- Produire des explications techniques et du contenu de newsletter

