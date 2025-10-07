# 🤝 Guide de Contribution

Merci de vouloir contribuer à ce projet ! Voici comment tu peux aider.

## 🎯 Types de Contributions

### 1. Ajouter un Nouveau LLM à Tester

Si tu veux ajouter un nouvel assistant (ex: Kimi 2, GLM-4, Claude Sonnet, etc.) :

1. Ajoute-le dans `matrice-comparaison.md`
2. Crée un guide de test dans `GUIDE-VISUEL.md`
3. Exécute le test avec `prompt-test-computer-use.md`
4. Partage tes résultats dans une Pull Request

### 2. Proposer un Nouveau Cas d'Usage

Le test actuel utilise "Gemini Computer Use API". Tu peux proposer d'autres cas :

- Intégration d'une autre API
- Setup d'un projet complexe
- Migration de codebase
- Documentation d'architecture

**Comment** :
1. Crée un nouveau dossier `cas-usage/[NOM]/`
2. Copie et adapte `prompt-test-computer-use.md`
3. Documente les résultats

### 3. Améliorer les Critères d'Évaluation

Si tu penses que les critères (Complétude, Précision, etc.) peuvent être améliorés :

1. Ouvre une Issue pour discussion
2. Propose une modification de `matrice-comparaison.md`
3. Explique pourquoi c'est plus pertinent

### 4. Partager Tes Résultats

Tu as effectué le benchmark ? Génial !

1. Crée un dossier `resultats-communaute/[TON-NOM]/`
2. Ajoute tes fichiers de résultats
3. Inclus un `ANALYSE.md` avec tes observations
4. Pull Request !

## 📝 Process de Contribution

### 1. Fork & Clone

```bash
# Fork le repo sur GitHub
# Puis clone ton fork
git clone https://github.com/[TON-USERNAME]/assistant-doc-benchmark.git
cd assistant-doc-benchmark
```

### 2. Crée une Branche

```bash
git checkout -b feature/[NOM-FEATURE]
# Exemples :
# - feature/ajout-kimi-2
# - feature/cas-usage-api-rest
# - fix/typo-readme
```

### 3. Fais Tes Modifications

- Code propre et documenté
- Suis le style existant
- Teste tes modifications

### 4. Commit

```bash
git add .
git commit -m "Description claire de ce que tu as fait"
```

**Format de commit recommandé** :
- `feat: Ajout test Kimi 2`
- `fix: Correction typo dans README`
- `docs: Amélioration guide CLI`
- `test: Ajout résultats benchmark Phase 1`

### 5. Push & Pull Request

```bash
git push origin feature/[NOM-FEATURE]
```

Puis ouvre une Pull Request sur GitHub avec :
- Titre clair
- Description de ce que tu as fait
- Pourquoi c'est utile
- Screenshots si applicable

## ✅ Checklist Avant PR

- [ ] Code testé
- [ ] Documentation mise à jour si nécessaire
- [ ] Pas de fichiers de résultats personnels (sauf si c'est le but de la PR)
- [ ] Commit message descriptif
- [ ] Respect du style existant

## 🐛 Rapporter un Bug

Ouvre une Issue avec :
- **Titre** : Résumé du bug
- **Description** : Ce qui se passe vs ce qui devrait se passer
- **Étapes pour reproduire**
- **Environnement** : OS, versions, etc.
- **Screenshots** si applicable

## 💡 Proposer une Feature

Ouvre une Issue avec :
- **Titre** : Nom de la feature
- **Problème** : Quel besoin ça résout ?
- **Solution proposée** : Comment ça marcherait
- **Alternatives** : Autres approches envisagées

## 📬 Questions ?

Ouvre une Issue avec le tag `question` !

## 🙏 Merci !

Chaque contribution, petite ou grande, est appréciée ! 🎉
