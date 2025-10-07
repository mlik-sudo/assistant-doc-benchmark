# 🧪 Prompt de Test - Assistant Documentation

## À copier-coller dans : Gemini Pro / ChatGPT 5 / Perplexity

---

**CONTEXTE** :

Tu es un assistant spécialisé dans la préparation de documentation technique pour Claude CLI, un agent d'automatisation qui exécute des tâches de développement.

Claude travaille dans un environnement macOS, utilise Python/TypeScript/Bash, et a besoin de packages documentation **prêts à l'emploi** pour accomplir des tâches sans avoir à chercher lui-même.

**TÂCHE** :

Prépare un **package documentation complet** pour la tâche suivante :

> **"Intégrer l'API Gemini 2.5 Computer Use dans Gemini CLI"**

**INFORMATIONS FOURNIES** :

1. **Gemini CLI** est un outil existant qui utilise déjà l'API Gemini
   - Localisation : `/Users/sahebmlik/cli-agents-optimization/gemini-cli/`
   - Config actuelle : `.gemini/settings.json`
   - Il a déjà des MCPs installés (Chrome DevTools notamment)

2. **Gemini 2.5 Computer Use** :
   - Nouveau modèle spécialisé : `gemini-2.5-pro` avec tool `computer_use`
   - Permet d'automatiser des interfaces web (click, type, scroll)
   - Fonctionne en loop : screenshot → action → screenshot
   - Preview disponible via Google AI Studio et Vertex AI
   - Docs officielles : https://cloud.google.com/vertex-ai/generative-ai/docs/model-reference/computer-use
   - Optimisé pour browsers, bon pour mobile UI, pas encore pour desktop OS

3. **Environnement de Claude** :
   - OS : macOS (Darwin 25.0.0)
   - Shell : zsh
   - Package managers : npm, pip, brew
   - API Key Gemini déjà configurée (variable `GEMINI_API_KEY`)
   - Playwright déjà installé localement

**FORMAT ATTENDU** :

Livre un package selon cette structure :

```markdown
# 📋 Package Documentation - Gemini Computer Use API

## 🎯 Objectif de la Tâche
[Résumé en 2-3 lignes]

## 📚 Documentation Clé

### 1. Quickstart
[3-5 étapes essentielles pour démarrer]

### 2. API Reference (pertinente uniquement)
[Seulement les endpoints/méthodes nécessaires pour CETTE tâche]
- Endpoint/Méthode : `...`
- Paramètres requis : `...`
- Exemple de requête : `...`
- Réponse attendue : `...`

### 3. Configuration Requise
- Variables d'environnement : `...`
- Dépendances à installer : `...`
- Fichiers de config à modifier : `...`

### 4. Exemples de Code (Ready-to-Use)
```language
// Code complet, fonctionnel, commenté
// Que Claude peut copier-coller directement
```

### 5. Pièges & Solutions
⚠️ **Erreur courante #1** : [Description]
✅ **Solution** : [Comment l'éviter]

[Répéter pour chaque piège identifié]

### 6. Comparaison d'Approches (si applicable)
| Approche A | Approche B | Recommandation |
|-----------|-----------|----------------|
| ...       | ...       | ✅ ... car...   |

### 7. Checklist Pré-Exécution
- [ ] Item 1
- [ ] Item 2
- [ ] ...

### 8. Scripts Proposés

**Script 1 : Installation**
```bash
# Commandes bash prêtes à exécuter
```

**Script 2 : Test rapide**
```bash
# Commande de vérification
```

### 9. Métriques de Success
✅ La tâche est réussie si :
- [ ] Critère 1
- [ ] Critère 2
- [ ] ...

### 10. Ressources Externes
- [Titre lien](url)
```

**CONTRAINTES IMPORTANTES** :

1. ✅ **Concis mais complet** : Pas de blabla, seulement l'essentiel
2. ✅ **Code ready-to-use** : Pas de pseudo-code, du vrai code exécutable
3. ✅ **Compatibilité macOS** : Toutes les commandes doivent fonctionner sur macOS
4. ✅ **No preamble** : Évite "Here is...", "Based on...", va droit au but
5. ✅ **Exemples concrets** : Utilise de vrais exemples, pas "votre-api-key"

**CE QUE CLAUDE DOIT POUVOIR FAIRE AVEC TON PACKAGE** :

Après avoir lu ton package, Claude doit être capable de :
- ✅ Installer toutes les dépendances (commandes exactes)
- ✅ Configurer l'environnement (fichiers à modifier)
- ✅ Copier-coller du code fonctionnel
- ✅ Tester que ça marche (commande de vérification)
- ✅ Éviter les pièges courants (grâce à tes alertes)

**COMMENCE MAINTENANT** : Prépare le package documentation complet.
