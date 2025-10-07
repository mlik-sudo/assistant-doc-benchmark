# 🧪 Assistant Documentation Benchmark

> Benchmark scientifique de plusieurs LLMs pour identifier le meilleur assistant de préparation de documentation technique pour Claude CLI.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## 🎯 Objectif

Comparer **7 assistants IA** (Web Apps + CLIs) pour déterminer lequel prépare les meilleurs **packages documentation** pour un agent CLI comme Claude Code.

### Assistants Testés

**Web Apps (5)** :
- 🤖 Gemini Pro
- 💬 ChatGPT 5 (Minimum, Medium, High)
- 🔍 Perplexity

**CLIs (2)** :
- 🖥️ Gemini CLI 2.5 Pro
- 💻 ChatGPT 5 Codex CLI

---

## 🚀 Quick Start

### Option 1 : Suivre le Benchmark Complet

```bash
# 1. Clone le repo
git clone https://github.com/[TON-USERNAME]/assistant-doc-benchmark.git
cd assistant-doc-benchmark

# 2. Commence par START-HERE.md
open START-HERE.md

# 3. Suis GUIDE-VISUEL.md pour les tests
open GUIDE-VISUEL.md
```

### Option 2 : Test Rapide (1h30)

Si tu veux juste tester quelques assistants :

```bash
# Teste seulement :
# - Gemini Pro Web
# - ChatGPT 5 Medium
# - Perplexity

# Voir GUIDE-VISUEL.md pour les instructions
```

---

## 📂 Structure du Projet

```
assistant-doc-benchmark/
├── 🌟 START-HERE.md              # Point d'entrée (commence ici)
├── 🎯 GUIDE-VISUEL.md            # Guide complet étape par étape
├── ⚡ COMMANDES-CLI-QUICK.md     # Commandes CLI (copier-coller)
├── 🧪 prompt-test-computer-use.md # Prompt de test
├── 📊 matrice-comparaison.md     # Grille d'évaluation
├── 📋 PLAN-FINAL.md              # Vue d'ensemble
├── 🖥️ PHASE-CLI-TEST.md         # Guide détaillé CLI
├── 📝 instructions-assistant.md  # Instructions pour Phase 2
└── resultats/
    ├── phase1/      # Résultats Web Apps
    ├── phase-cli/   # Résultats CLIs
    ├── phase2/      # Auto-optimisé (optionnel)
    └── phase3/      # Avancé (optionnel)
```

---

## 🧪 Méthodologie

### Phase 1 : Baseline Web Apps (~2h30)

Tester les 5 assistants web avec le même prompt pour comparer :
- Complétude de la documentation
- Précision technique
- Utilisabilité pour un agent CLI
- Qualité des alertes et pièges
- Efficacité (concision)

### Phase CLI : Test des Agents CLI (~20 min)

Comparer les versions CLI avec les versions Web pour :
- Gemini Pro Web vs Gemini CLI 2.5 Pro
- ChatGPT 5 Web (Medium) vs Codex CLI (Medium)

**Question** : Les CLIs sont-ils meilleurs que les Web Apps ?

### Phase 2 : Auto-Optimisé (Optionnel)

Demander à chaque LLM de réécrire les instructions pour s'auto-optimiser.

---

## 📊 Critères d'Évaluation

Chaque assistant est noté sur **10 points** :

| Critère | Points | Description |
|---------|--------|-------------|
| **Complétude** | 2 | Tous les éléments présents |
| **Précision Technique** | 2 | Code fonctionnel, commandes correctes |
| **Utilisabilité** | 2 | Format respecté, ready-to-use |
| **Alertes & Pièges** | 2 | Erreurs courantes identifiées |
| **Efficacité** | 2 | Concis, va droit au but |

---

## 🎓 Cas d'Usage : Gemini Computer Use API

Le test utilise comme cas concret : **intégrer l'API Gemini 2.5 Computer Use dans Gemini CLI**.

Cette API permet d'automatiser des interfaces web (click, type, scroll) via un loop screenshot → action → screenshot.

**Pourquoi ce cas ?**
- Complexité technique réelle
- Nécessite doc officielle + exemples
- Requiert code ready-to-use
- Pièges potentiels à identifier

---

## 🏆 Résultats Attendus

Après les tests, tu obtiendras :

1. **Classement des assistants** (score /10)
2. **Comparaison Web vs CLI** (lequel est meilleur ?)
3. **Mode optimal** pour ChatGPT 5 (min/med/high)
4. **Recommandation finale** : Quel assistant utiliser pour préparer des docs ?

---

## 🛠️ Prérequis

### Pour les Tests Web Apps
- Comptes actifs : Gemini Pro, ChatGPT 5, Perplexity
- API Key Gemini (pour le contexte du test)

### Pour les Tests CLI
- Node.js installé
- CLIs installés :
  ```bash
  npm install -g @google/gemini-cli@latest
  npm update -g @openai/codex
  ```
- Authentification :
  ```bash
  gemini /auth
  codex login
  ```

---

## 📖 Guide de Démarrage Détaillé

### Étape 1 : Préparation (5 min)

1. Clone le repo
2. Lis `START-HERE.md`
3. Prépare :
   - API Key Gemini
   - URLs documentation Computer Use
   - Connexion aux comptes

### Étape 2 : Tests Web (2h30)

1. Ouvre `GUIDE-VISUEL.md`
2. Pour chaque assistant :
   - Copie le prompt de `prompt-test-computer-use.md`
   - Colle dans l'assistant
   - Sauvegarde la réponse dans `resultats/phase1/`
3. Remplis `matrice-comparaison.md`

### Étape 3 : Tests CLI (20 min)

1. Ouvre `COMMANDES-CLI-QUICK.md`
2. Exécute les commandes CLI
3. Compare Web vs CLI dans `PHASE-CLI-TEST.md`

### Étape 4 : Analyse (30 min)

1. Compare tous les résultats
2. Identifie le meilleur assistant
3. Documente tes observations

---

## 🤝 Contributions

Ce projet est un template de benchmark. N'hésite pas à :
- Ajouter d'autres LLMs à tester
- Proposer d'autres cas d'usage
- Améliorer les critères d'évaluation
- Partager tes résultats

### Comment Contribuer

1. Fork le repo
2. Crée une branche : `git checkout -b feature/nouveau-test`
3. Commit : `git commit -m "Ajout test Kimi 2"`
4. Push : `git push origin feature/nouveau-test`
5. Ouvre une Pull Request

---

## 📝 License

MIT License - Utilise librement pour tes propres benchmarks !

---

## 📬 Contact

Si tu as des questions ou veux partager tes résultats : ouvre une Issue !

---

## 🙏 Remerciements

- **Claude CLI** pour l'inspiration du cas d'usage
- **Google Gemini** pour l'API Computer Use
- **OpenAI** pour ChatGPT 5 et Codex CLI
- **Perplexity** pour leurs capacités de recherche

---

**Bon benchmark ! 🚀**

*Star ⭐ ce repo si tu le trouves utile !*
