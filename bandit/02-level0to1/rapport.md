<h1 align="center">🐧 OverTheWire - Bandit : Level 0 -> 1</h1>

## 🧭 Objectif
L'objectif est de trouver le mot de passe pour l'utilisateur `bandit1` en utilisant les informations trouvées avec l'utilisateur `bandit0`.
> **Note** : Le mot de passe pour l'utilisateur `bandit1`se trouve dans un fichier nommé `readme` situé dans le répertoire `home directory`.

## 🛠️ Les commandes utilisés

```bash
# Je suis déjà connecté en tant que bandit0, je peux donc directement lire le fichier readme
# Toujours vérifié que le fichier existe et que j'ai les permissions nécessaires pour le lire
ls -l /home/bandit0/readme
# Lecture du fichier readme pour obtenir le mot de passe
cat /home/bandit0/readme
# Le mot de passe pour l'utilisateur bandit1 est maintenant affiché dans le terminal.
# Je me déconnecte de bandit0 et me connecte à bandit1
exit
ssh -p 2220 bandit1@bandit.labs.overthewire.org
```

## 📌 Résultat

Après avoir exécuté la commande SSH, j'ai réussi à me connecter au serveur du jeu. Le message de bienvenue indique que je suis maintenant connecté en tant que `bandit1`.

![Connexion réussie](/bandit/02-level0to1/solution.png)

---

<p align="center">  <i>⬅️ <a href="/bandit/01-level0/rapport.md">Previous level</a></i> | <i><a href="/bandit/03-level1to2/rapport.md">Next level</a> ➡️</i></p>
<p align="center">  <i>↪️ Back to <a href="/bandit/sommaire.md">Summary</a></i> | <i>📍 From <a href="https://github.com/SybillLabs">SybillLabs</a></i></p>