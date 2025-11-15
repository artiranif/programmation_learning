# Tutoriel Git pour un Projet Réel

Ce tutoriel présente **Git** pas à pas dans le contexte d’un projet réel. Il est conçu pour être utilisé tel quel dans un fichier `.md`.

---

## 📌 Objectifs du tutoriel

* Comprendre Git avec un workflow réel.
* Savoir créer, administrer et collaborer sur un projet.
* Maîtriser les commandes essentielles.
* Savoir gérer les erreurs et les branches.

---

# 🧱 1. Installation de Git

### **Windows**

Téléchargez Git : [https://git-scm.com/download/win](https://git-scm.com/download/win)

### **Linux (Ubuntu)**

```bash
a sudo apt update && sudo apt install git
```

### **Vérifier l'installation**

```bash
git --version
```

---

# 🔧 2. Configurer Git pour la première fois

```bash
git config --global user.name "Votre Nom"
git config --global user.email "email@example.com"
```

Vérifier la config :

```bash
git config --list
```

---

# 📁 3. Créer un Projet Réel : Structure Exemple

```
mon-projet/
│   README.md
│   .gitignore
│
└── src/
    └── app.py
```

---

# 🚀 4. Initialiser un Dépôt Git

```bash
cd mon-projet
git init
```

Git crée un dossier `.git` → **ne jamais modifier à la main !**

---

# 📤 5. Ajouter et Commit les Fichiers

### Voir l’état

```bash
git status
```

### Ajouter tous les fichiers

```bash
git add .
```

### Premier commit

```bash
git commit -m "Initial commit : structure du projet"
```

---

# 🌐 6. Connecter avec GitHub / GitLab / Bitbucket

Créer un dépôt vide en ligne, puis :

```bash
git remote add origin https://github.com/votre-user/mon-projet.git

git branch -M main
git push -u origin main
```

---

# 🌿 7. Travailler avec les Branches

### Créer une branche

```bash
git checkout -b feature/authentification
```

### Travailler, puis commit

```bash
git add .
git commit -m "Ajout base authentification"
```

### Pousser la branche vers le serveur

```bash
git push -u origin feature/authentification
```

---

# 🔄 8. Fusion (Merge) dans main

### Aller sur main

```bash
git checkout main
```

### Récupérer les derniers changements

```bash
git pull
```

### Fusionner

```bash
git merge feature/authentification
```

### Envoyer vers le serveur

```bash
git push origin main
```

---

# 🧯 9. Résolution des Conflits

Un conflit ressemble à :

```
<<<<<<< HEAD
version locale
=======
version distante
>>>>>>> branch-feature
```

### Étapes :

1. Ouvrir le fichier.
2. Choisir la bonne version.
3. Supprimer les marqueurs.
4. Commit :

```bash
git add .
git commit -m "Résolution de conflit dans app.py"
```

---

# 📝 10. Mettre à Jour son Projet (pull)

```bash
git pull
```

Si le code change côté serveur → **toujours pull avant de coder**.

---

# 🧹 11. Nettoyage des Branches

### Supprimer en local

```bash
git branch -d feature/authentification
```

### Supprimer côté serveur

```bash
git push origin --delete feature/authentification
```

---

# 🔍 12. Historique et Navigation

### Voir l’historique

```bash
git log --oneline --graph --decorate
```

### Voir les modifications

```bash
git diff
```

---

# 🎯 13. Bonnes Pratiques dans un Projet Réel

* Toujours créer une branche pour une fonctionnalité.
* Faire des commits clairs et courts.
* Ne jamais travailler directement sur `main`.
* Utiliser des messages explicites :

  * `fix: correction bug login`
  * `feat: ajout dashboard`
  * `refactor: optimisation de la classe User`

---

# 🧠 14. Commandes Résumé

```bash
git init
git status
git add .
git commit -m "message"
git push
git pull
git branch
git checkout -b nom-branche
git merge nom-branche
```

---

# 📦 15. Exemple Complet de Workflow

```bash
# Récupérer le projet
git clone https://github.com/votre-user/projet.git

# Créer une fonctionnalité
git checkout -b feat/profil

# Développer, puis commit
git add .
git commit -m "feat: ajout page profil"

# Envoyer la branche
git push -u origin feat/profil

# Merge via GitHub ou en local
```

---

# ✔️ Conclusion

Ce tutoriel offre les bases essentielles pour utiliser Git dans un projet réel. Vous pouvez maintenant l’étendre, l'améliorer ou l'utiliser pour former d’autres développeurs.
