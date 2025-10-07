# 🎯 Guide Visuel - Benchmark Assistant Documentation

## 📋 Phase 1 : Baseline (Commence ici !)

### ✅ Préparation
```
1. Prépare ta documentation Computer Use (URLs)
2. Vérifie ton API Key Gemini
```

### 🧪 Test 1 : Gemini Pro

```
1. Ouvre Gemini Pro App
2. Copie le contenu de : prompt-test-computer-use.md
3. Colle dans Gemini Pro
4. Attends la réponse
5. Copie TOUTE la réponse
6. Colle dans : resultats/phase1/gemini-pro-baseline.md
```

**⏱️ Temps estimé** : 10-15 min

---

### 🧪 Test 2 : ChatGPT 5 (Minimum)

```
1. Ouvre ChatGPT 5 App (ou ChatGPT 5 Codex)
2. Active : Mode "Minimum"
3. Copie le contenu de : prompt-test-computer-use.md
4. Colle dans ChatGPT 5
5. Attends la réponse
6. Copie TOUTE la réponse
7. Colle dans : resultats/phase1/chatgpt5-min-baseline.md
```

**⏱️ Temps estimé** : 10-15 min

---

### 🧪 Test 3 : ChatGPT 5 (Medium)

```
1. Dans ChatGPT 5 App
2. Active : Mode "Medium"
3. Copie le contenu de : prompt-test-computer-use.md
4. Colle dans ChatGPT 5
5. Attends la réponse
6. Copie TOUTE la réponse
7. Colle dans : resultats/phase1/chatgpt5-med-baseline.md
```

**⏱️ Temps estimé** : 10-15 min

---

### 🧪 Test 4 : ChatGPT 5 (High)

```
1. Dans ChatGPT 5 App
2. Active : Mode "High"
3. Copie le contenu de : prompt-test-computer-use.md
4. Colle dans ChatGPT 5
5. Attends la réponse (plus long)
6. Copie TOUTE la réponse
7. Colle dans : resultats/phase1/chatgpt5-high-baseline.md
```

**⏱️ Temps estimé** : 15-20 min

---

### 🧪 Test 5 : Perplexity

```
1. Ouvre Perplexity App
2. Mode : Standard (défaut)
3. Copie le contenu de : prompt-test-computer-use.md
4. Colle dans Perplexity
5. Attends la réponse
6. Copie TOUTE la réponse
7. Colle dans : resultats/phase1/perplexity-baseline.md
```

**⏱️ Temps estimé** : 10-15 min

---

### 📊 Évaluation Phase 1

```
1. Ouvre : matrice-comparaison.md
2. Pour chaque test (#1-5) :
   - Lis le package généré
   - Note /10 selon les critères
   - Écris tes observations
3. Compare les 5 résultats
4. Identifie le meilleur
```

**⏱️ Temps estimé** : 30-45 min

---

## 🖥️ Phase CLI - Test des Agents CLI

### 🧪 Test CLI #1 : Gemini CLI 2.5 Pro

```bash
# 1. Vérifier que Gemini CLI est installé et authentifié
gemini --version
# Si besoin : npm install -g @google/gemini-cli@latest
# Si besoin : gemini /auth

# 2. Copier le prompt
cat > /tmp/prompt-computer-use.txt << 'EOF'
[COLLER LE CONTENU DE prompt-test-computer-use.md]
EOF

# 3. Exécuter avec Gemini CLI
gemini ask --file /tmp/prompt-computer-use.txt > ~/Documents/assistant-doc-benchmark/resultats/phase-cli/gemini-cli-2.5-pro.md
```

**⏱️ Temps estimé** : 5-10 min

---

### 🧪 Test CLI #2 : ChatGPT 5 Codex CLI (Medium)

```bash
# 1. Vérifier que Codex CLI est installé et authentifié
codex --version
# Si besoin : npm update -g @openai/codex
# Si besoin : codex login

# 2. Exécuter avec Codex CLI (mode medium)
codex ask --mode medium --file /tmp/prompt-computer-use.txt > ~/Documents/assistant-doc-benchmark/resultats/phase-cli/chatgpt5-codex-cli-medium.md
```

**⏱️ Temps estimé** : 5-10 min

---

### 📊 Comparaison Web vs CLI

Après les tests CLI, compare dans `PHASE-CLI-TEST.md` :
- Gemini Pro Web vs Gemini CLI 2.5 Pro
- ChatGPT 5 Web (Medium) vs ChatGPT 5 Codex CLI (Medium)

**Question** : Web ou CLI est meilleur pour préparer des packages ?

---

## 🎯 Décision : Continuer ?

**Après Phase 1 + CLI** :
- Tu as testé 7 assistants (5 web + 2 CLI)
- Identifié les meilleurs
- Comparé Web vs CLI

**Si différences significatives** :
→ Continue Phase 2 (Auto-optimisé)

**Si résultats similaires** :
→ Choisis le meilleur et utilise-le !

---

## 📋 Phase 2 : Auto-Optimisé (Optionnel)

### Prompt Phase 2

```markdown
Tu es [Gemini Pro / ChatGPT o1 / Perplexity].

Voici des instructions pour un "Assistant Documentation"
destiné à préparer des packages pour Claude CLI :

[COLLER LE CONTENU DE : instructions-assistant.md]

Tâche : Réécris ces instructions pour être OPTIMAL
pour toi-même. Adapte :
- Le format qui maximise TES capacités
- Le niveau de détail qui TE convient
- Les exemples qui t'aident LE PLUS
- Le style qui TE rend le plus efficace

Garde le même objectif (préparer packages pour Claude),
mais optimise pour TES forces.
```

### Tests Phase 2

Répète les tests avec les instructions auto-optimisées :
- Gemini Pro auto
- ChatGPT 5 Min auto
- ChatGPT 5 Med auto
- ChatGPT 5 High auto
- Perplexity auto

Sauvegarde dans `resultats/phase2/`

---

## 📊 Comparaison Finale

```
1. Compare Baseline vs Auto-optimisé
2. Identifie le MEILLEUR des 8 tests
3. Recommande à Claude quel assistant utiliser
```

---

## 🏆 Livraison à Claude

Partage avec Claude :
```
1. matrice-comparaison.md (remplie)
2. Top 3 assistants + pourquoi
3. Dossier resultats/ complet
```

Claude analysera et te dira quel assistant utiliser ! 🎯

---

## ⚡ Raccourcis

**Juste tester Phase 1 (minimum)** :
```
1. Gemini Pro
2. ChatGPT 5 (un seul mode)
3. Perplexity
= 3 tests en 1h30
```

**Test complet Phase 1** :
```
1. Gemini Pro
2. ChatGPT 5 (3 modes: min/med/high)
3. Perplexity
= 5 tests en 2h30
```

**Test Phase 1 + Phase 2** :
```
10 tests en 5h
```

**Test exhaustif avec Phase 3** :
```
15+ tests en 7-8h
(+ ChatGPT 5 Codex CLI, Perplexity variants)
```

---

**Commence simple, étends si nécessaire ! 🚀**
