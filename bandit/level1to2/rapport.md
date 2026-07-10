<h1 align="center">🐧 OverTheWire - Bandit : Level 1 -> 2</h1>

## 🧭 Objectif
L'objectif est de trouver le mot de passe pour l'utilisateur `bandit2` en utilisant les informations trouvées avec l'utilisateur `bandit1`.
> **Note** : Le mot de passe pour l'utilisateur `bandit2`se trouve dans un fichier nommé `-` situé dans le répertoire `home directory`.

## 🛠️ Les commandes utilisés

```bash
# Je suis déjà connecté en tant que bandit1, je peux donc directement lire le fichier -
# Toujours vérifié que le fichier existe et que j'ai les permissions nécessaires pour le lire
ls -l /home/bandit1/-
# Lecture du fichier readme pour obtenir le mot de passe
cat /home/bandit1/-
# Le mot de passe pour l'utilisateur bandit2 est maintenant affiché dans le terminal.
# Je me déconnecte de bandit1 et me connecte à bandit2
exit
ssh -p 2220 bandit2@bandit.labs.overthewire.org
```

## 📌 Résultat

Après avoir exécuté la commande SSH, j'ai réussi à me connecter au serveur du jeu. Le message de bienvenue indique que je suis maintenant connecté en tant que `bandit2`.

![Connexion réussie](/bandit/level1to2/solution.png)

---

<p align="center">  <i>⬅️ <a href="/bandit/level0to1/rapport.md">Previous level</a></i> | <i><a href="/bandit/level2to3/rapport.md">Next level</a> ➡️</i></p>
<p align="center">  <i>↪️ Back to <a href="/bandit/sommaire.md">Summary</a></i> | <i>📍 From <a href="https://github.com/SybillLabs">SybillLabs</a></i></p>