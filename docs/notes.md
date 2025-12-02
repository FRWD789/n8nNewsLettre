# Notes du Lab n8n — Automatisation Newsletter
## 1. Installation de n8n

**Méthode choisie : npm (Node.js)**

Commandes utilisées :

```bash
node -v                # vérifier que Node.js est installé
npm install n8n -g     # installer n8n globalement
n8n -v                 # vérifier l'installation
n8n                     # lancer n8n
```


## 2. Apprentissage : c'est quoi n8n ?

n8n est un outil d'automatisation no code. 
Il permet de connecter des applications entre elles (Gmail, Discord, Notion, Google Sheets, Stripe, etc.) et de créer des actions automatiques sans coder. Un peu comme Zapier ou Make.

## Les éléments de base

### Workflow

Un workflow est une suite d'actions automatisées. Exemple :

```
[Trigger] → [Read Emails List] → [Send Email]
```

### Nodes (blocs)

Chaque node réalise une action, par exemple :

* Un node pour envoyer un email
* Un node pour lire un fichier
* Un node pour attendre une heure précise
* Un node pour publier sur Twitter

### Notes Importantes
- Structure workflow critique : L'ordre des nœuds est essentiel (Merge → Function format → ChatGPT → Function combine → Function HTML)
- Noms de nœuds : À adapter selon votre workflow spécifique
- Coûts optimisés : 1 appel ChatGPT au lieu de 15 (économies significatives)
- Performance : Exécution complète en quelques secondes au lieu de minutes
- Modularité : Chaque nœud Function peut être testé indépendamment