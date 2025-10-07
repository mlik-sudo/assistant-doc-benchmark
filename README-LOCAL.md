# 🧪 Benchmark Assistant Documentation

## 🎯 Objectif

Tester plusieurs LLMs pour identifier le meilleur "Assistant Documentation" capable de préparer des packages techniques pour Claude CLI.

## 📁 Fichiers

- `prompt-test-computer-use.md` - Prompt à copier-coller dans les LLMs
- `matrice-comparaison.md` - Grille d'évaluation à remplir
- `instructions-assistant.md` - Instructions complètes pour l'assistant (à utiliser en Phase 2)
- `resultats/` - Dossier pour sauvegarder les réponses des LLMs

## 🧪 Phases du Test

### Phase 1 : Baseline Web Apps (Mes Instructions)
Copier-coller le prompt dans les **applications web** :
- [ ] Gemini Pro (mode standard)
- [ ] ChatGPT 5 (minimum)
- [ ] ChatGPT 5 (medium)
- [ ] ChatGPT 5 (high)
- [ ] Perplexity (mode standard)

Sauvegarder chaque résultat dans `resultats/phase1/`

### Phase CLI : Test des Agents CLI 🆕
Tester les **interfaces CLI** (voir `PHASE-CLI-TEST.md`) :
- [ ] Gemini CLI 2.5 Pro
- [ ] ChatGPT 5 Codex CLI (medium)

Sauvegarder dans `resultats/phase-cli/`

**Objectif** : Comparer Web vs CLI pour identifier le meilleur

### Phase 2 : Auto-Optimisé (Optionnel)
Demander à chaque LLM de réécrire les instructions pour s'auto-optimiser
- [ ] Gemini Pro auto-optimisé
- [ ] ChatGPT 5 Min auto-optimisé
- [ ] ChatGPT 5 Med auto-optimisé
- [ ] ChatGPT 5 High auto-optimisé
- [ ] Perplexity auto-optimisé

Sauvegarder dans `resultats/phase2/`

### Phase 3 : Avancé (Optionnel)
- [ ] Perplexity Deep Search
- [ ] Perplexity + Claude 4.5
- [ ] Perplexity + autres modèles
- [ ] (Optionnel) Kimi 2, GLM...

Sauvegarder dans `resultats/phase3/`

## 📊 Évaluation

Remplir `matrice-comparaison.md` avec :
- Score /10 pour chaque assistant
- Notes qualitatives
- Temps de génération
- Forces et faiblesses

## 🏆 Livrable Final

À partager avec Claude :
1. Matrice remplie
2. Top 3 des assistants
3. Recommandation finale
4. Tous les packages générés (dans `resultats/`)

## 📝 Méthodologie

1. **Tester dans l'ordre** : Phase 1 d'abord, puis décider si Phase 2/3
2. **Sauvegarder tout** : Copier-coller chaque réponse dans un fichier séparé
3. **Évaluer immédiatement** : Noter pendant que c'est frais
4. **Comparer objectivement** : Utiliser les critères de la matrice

## ⏱️ Estimation Temps

- Phase 1 (Web Apps) : ~2h30 (5 tests)
- Phase CLI : ~20 min (2 tests)
- Phase 2 (Auto-optimisé) : ~2h30 (5 tests)
- Phase 3 (Avancé) : ~1-2h (variables)
- Évaluation : ~1h

**Total Phase 1 + CLI** : ~3h (recommandé pour commencer)
**Total complet** : 7-8 heures

## 🚀 Démarrage Rapide

1. Crée le dossier `resultats/phase1/`
2. Ouvre `prompt-test-computer-use.md`
3. Copie le prompt
4. Colle dans Gemini Pro
5. Sauvegarde la réponse : `resultats/phase1/gemini-pro-baseline.md`
6. Répète pour les autres LLMs
7. Remplis `matrice-comparaison.md`

Bon courage ! 🎯
