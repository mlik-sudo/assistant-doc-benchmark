# 📋 Changelog

Toutes les modifications notables de ce projet seront documentées ici.

Le format est basé sur [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

## [1.0.0] - 2025-10-07

### 🎉 Release Initiale

#### Ajouté
- **Système de benchmark complet** pour 7 assistants IA
  - 5 Web Apps : Gemini Pro, ChatGPT 5 (3 modes), Perplexity
  - 2 CLIs : Gemini CLI 2.5 Pro, Codex CLI
- **Guides détaillés** :
  - `START-HERE.md` - Point d'entrée
  - `GUIDE-VISUEL.md` - Guide étape par étape
  - `COMMANDES-CLI-QUICK.md` - Commandes CLI
  - `PHASE-CLI-TEST.md` - Guide CLI détaillé
  - `PLAN-FINAL.md` - Vue d'ensemble
- **Méthodologie scientifique** :
  - Critères d'évaluation (5 critères, 10 points)
  - Grille de comparaison (`matrice-comparaison.md`)
  - Process reproductible
- **Cas d'usage concret** :
  - Test sur Gemini Computer Use API
  - Prompt de test ready-to-use
  - Instructions détaillées pour l'assistant
- **Structure organisée** :
  - Dossiers pour résultats (phase1, phase-cli, phase2, phase3)
  - Templates pour auto-optimisation
  - Documentation Phase 2 et Phase 3
- **Documentation complète** :
  - README avec badges et quickstart
  - LICENSE MIT
  - CONTRIBUTING guide
  - INFO sur ChatGPT 5 vs Codex

#### Features Clés
- ✅ Comparaison Web vs CLI
- ✅ Tests multi-modes (min/med/high pour ChatGPT 5)
- ✅ Phase auto-optimisation (optionnelle)
- ✅ Extensible à d'autres LLMs
- ✅ Reproductible scientifiquement

#### Structure Fichiers
```
10 fichiers de documentation
4 dossiers de résultats
16 fichiers totaux (+ LICENSE + CONTRIBUTING)
```

---

## [Unreleased]

### Prévu
- [ ] Résultats de benchmark communautaires
- [ ] Cas d'usage additionnels
- [ ] Tests avec Kimi 2, GLM-4
- [ ] Automatisation CI/CD
- [ ] Dashboard de visualisation des résultats

---

## Comment Contribuer

Lis [CONTRIBUTING.md](CONTRIBUTING.md) pour savoir comment ajouter :
- Nouveaux LLMs
- Nouveaux cas d'usage
- Tes propres résultats
- Améliorations des critères

---

**Format** : [Version] - Date YYYY-MM-DD
**Types** : Ajouté, Modifié, Supprimé, Corrigé, Sécurité
