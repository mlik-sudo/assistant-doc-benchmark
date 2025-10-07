# ⚡ Commandes CLI - Quick Reference

## 🔧 Installation & Setup

### Gemini CLI
```bash
# Installer
npm install -g @google/gemini-cli@latest

# Vérifier version
gemini --version

# S'authentifier
gemini /auth
```

### Codex CLI (ChatGPT 5)
```bash
# Installer/Mettre à jour
npm update -g @openai/codex

# Vérifier version
codex --version

# S'authentifier
codex login
```

---

## 🧪 Commandes de Test (Copier-Coller)

### Préparation (une seule fois)
```bash
# Créer le fichier prompt
cat > /tmp/prompt-computer-use.txt << 'EOF'
[OUVRIR prompt-test-computer-use.md ET COLLER TOUT LE CONTENU ICI]
EOF
```

### Test Gemini CLI
```bash
gemini ask --file /tmp/prompt-computer-use.txt > ~/Documents/assistant-doc-benchmark/resultats/phase-cli/gemini-cli-2.5-pro.md
```

### Test Codex CLI (Medium)
```bash
codex ask --mode medium --file /tmp/prompt-computer-use.txt > ~/Documents/assistant-doc-benchmark/resultats/phase-cli/chatgpt5-codex-cli-medium.md
```

---

## 🔄 Méthodes Alternatives (Interactif)

### Gemini CLI - Mode Shell
```bash
# Lancer shell interactif
gemini shell

# Puis coller le prompt directement
# Copier la réponse et sauvegarder manuellement dans :
# ~/Documents/assistant-doc-benchmark/resultats/phase-cli/gemini-cli-2.5-pro.md
```

### Codex CLI - Mode Shell
```bash
# Lancer shell interactif (mode medium)
codex shell --mode medium

# Puis coller le prompt directement
# Copier la réponse et sauvegarder manuellement dans :
# ~/Documents/assistant-doc-benchmark/resultats/phase-cli/chatgpt5-codex-cli-medium.md
```

---

## ✅ Vérification Post-Test

```bash
# Vérifier que les fichiers ont été créés
ls -lh ~/Documents/assistant-doc-benchmark/resultats/phase-cli/

# Devrait afficher :
# gemini-cli-2.5-pro.md
# chatgpt5-codex-cli-medium.md

# Vérifier le contenu (aperçu)
head -20 ~/Documents/assistant-doc-benchmark/resultats/phase-cli/gemini-cli-2.5-pro.md
head -20 ~/Documents/assistant-doc-benchmark/resultats/phase-cli/chatgpt5-codex-cli-medium.md
```

---

## 🐛 Troubleshooting

### Si Gemini CLI ne trouve pas la commande
```bash
# Réinstaller
npm uninstall -g @google/gemini-cli
npm install -g @google/gemini-cli@latest

# Vérifier PATH
echo $PATH

# Si besoin, ajouter npm global à PATH dans ~/.zshrc :
export PATH="$PATH:$(npm prefix -g)/bin"
source ~/.zshrc
```

### Si Codex CLI ne trouve pas la commande
```bash
# Réinstaller
npm uninstall -g @openai/codex
npm install -g @openai/codex

# Même vérification PATH que ci-dessus
```

### Si authentification échoue
```bash
# Gemini : Réessayer
gemini /auth

# Codex : Réessayer
codex login

# Si problème persiste : Vérifier que tu es bien abonné
```

---

**Prêt pour les tests CLI ! 🚀**
