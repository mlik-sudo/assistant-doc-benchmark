# 🖥️ Phase CLI - Test des Agents CLI

## 🎯 Objectif

Comparer les **agents CLI** avec les **web apps** pour identifier si les CLIs sont plus performants pour préparer des packages documentation.

---

## 🧪 Tests CLI à Effectuer

### Test CLI #1 : Gemini CLI 2.5 Pro

**Setup (si pas déjà fait)** :
```bash
# Vérifier installation
gemini --version

# Si pas installé :
npm install -g @google/gemini-cli@latest

# S'authentifier (si pas déjà fait)
gemini /auth
```

**Commande de test** :
```bash
# Copier le prompt dans un fichier temporaire
cat > /tmp/prompt-computer-use.txt << 'EOF'
[COLLER LE CONTENU DE prompt-test-computer-use.md ICI]
EOF

# Exécuter avec Gemini CLI
gemini ask --file /tmp/prompt-computer-use.txt > ~/Documents/assistant-doc-benchmark/resultats/phase-cli/gemini-cli-2.5-pro.md
```

**Alternative (méthode interactive)** :
```bash
# Méthode interactive
gemini shell

# Puis coller le prompt directement
[COLLER LE PROMPT]

# Copier la réponse et sauvegarder dans :
# ~/Documents/assistant-doc-benchmark/resultats/phase-cli/gemini-cli-2.5-pro.md
```

**Temps estimé** : 5-10 min

---

### Test CLI #2 : ChatGPT 5 Codex CLI (Medium)

**Setup (si pas déjà fait)** :
```bash
# Vérifier installation
codex --version

# Si pas installé ou mise à jour nécessaire :
npm update -g @openai/codex

# S'authentifier (si pas déjà fait)
codex login
```

**Commande de test** :
```bash
# Le fichier /tmp/prompt-computer-use.txt existe déjà du test précédent

# Exécuter avec Codex CLI (mode medium)
codex ask --mode medium --file /tmp/prompt-computer-use.txt > ~/Documents/assistant-doc-benchmark/resultats/phase-cli/chatgpt5-codex-cli-medium.md
```

**Alternative (méthode interactive)** :
```bash
# Méthode interactive
codex shell --mode medium

# Puis coller le prompt directement
[COLLER LE PROMPT]

# Copier la réponse et sauvegarder dans :
# ~/Documents/assistant-doc-benchmark/resultats/phase-cli/chatgpt5-codex-cli-medium.md
```

**Temps estimé** : 5-10 min

---

## 📊 Comparaison CLI vs Web

Après les tests CLI, on comparera :

### Gemini : Web vs CLI
| Critère | Gemini Pro Web | Gemini CLI 2.5 Pro | Gagnant |
|---------|---------------|-------------------|---------|
| Score /10 | ? | ? | ? |
| Temps | ? | ? | ? |
| Complétude | ? | ? | ? |
| Précision | ? | ? | ? |
| Utilisabilité | ? | ? | ? |

**Conclusion Gemini** : [Web OU CLI est meilleur car...]

---

### ChatGPT 5 : Web vs CLI
| Critère | ChatGPT 5 Web (Medium) | ChatGPT 5 Codex CLI (Medium) | Gagnant |
|---------|----------------------|---------------------------|---------|
| Score /10 | ? | ? | ? |
| Temps | ? | ? | ? |
| Complétude | ? | ? | ? |
| Précision | ? | ? | ? |
| Utilisabilité | ? | ? | ? |

**Conclusion ChatGPT 5** : [Web OU CLI est meilleur car...]

---

## 🏆 Résultats Attendus

**Hypothèse** :
- 🤔 Les CLIs pourraient être **meilleurs** car :
  - Plus de contrôle
  - Moins de contraintes d'interface
  - Optimisés pour le code
  - Accès direct aux modèles sans UI overhead

**OU**

- 🤔 Les Web Apps pourraient être **meilleurs** car :
  - Interface optimisée pour les tâches complexes
  - Features visuelles (markdown preview, etc.)
  - Plus de modes disponibles (min/med/high)

**On verra ! 🧪**

---

## 📝 Ajout à la Matrice Finale

Ces 2 tests CLI seront ajoutés à `matrice-comparaison.md` :

| # | Assistant | Mode/Modèle | Phase | Score /10 | Temps | Notes |
|---|-----------|-------------|-------|-----------|-------|-------|
| ... | ... | ... | ... | ... | ... | ... |
| 14 | Gemini CLI | 2.5 Pro | CLI Test | ? | ? min | |
| 15 | ChatGPT 5 Codex | Medium CLI | CLI Test | ? | ? min | |

---

## 🎯 Ordre de Test Recommandé

1. ✅ **D'abord** : Phase 1 (Web Apps - 5 tests)
2. ✅ **Ensuite** : Phase CLI (2 tests)
3. ✅ **Comparer** : Web vs CLI pour chaque plateforme
4. ✅ **Décider** : Quel assistant utiliser (Web ou CLI ?)
5. ⏸️ **Optionnel** : Phase 2 (Auto-optimisé) si besoin

---

## 💡 Questions pour Claude lors du Test CLI

Après avoir fait les tests CLI, partage avec Claude :

1. **Les résultats CLI** (les 2 fichiers markdown)
2. **Tes observations** :
   - Facilité d'utilisation CLI vs Web ?
   - Différences de qualité ?
   - Différences de vitesse ?
   - Lequel tu préfères ?

Claude analysera et te dira **quel assistant utiliser** (Web ou CLI) pour les prochaines tâches ! 🚀

---

*Note : Créer d'abord le dossier `resultats/phase-cli/`*
