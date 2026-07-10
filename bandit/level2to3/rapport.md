<h1 align="center">🐧 OverTheWire - Bandit : Level 2 -> 3</h1>

## 🧭 Objectif
L'objectif est de trouver le mot de passe pour l'utilisateur `bandit3` en utilisant les informations trouvées avec l'utilisateur `bandit2`.
> **Note** : Le mot de passe pour l'utilisateur `bandit3`se trouve dans un fichier nommé `--spaces in this filename--` situé dans le répertoire `home directory`.

## 🛠️ Les commandes utilisés

```bash
# Je suis déjà connecté en tant que bandit2, je peux donc directement lire le fichier --spaces in this filename--
# Toujours vérifié que le fichier existe et que j'ai les permissions nécessaires pour le lire
ls -l /home/bandit2/--spaces in this filename--
# Lecture du fichier --spaces in this filename-- pour obtenir le mot de passe
cat /home/bandit2/--spaces in this filename--
# Le mot de passe pour l'utilisateur bandit3 est maintenant affiché dans le terminal.
# Je me déconnecte de bandit2 et me connecte à bandit3
exit
ssh -p 2220 bandit3@bandit.labs.overthewire.org
```

## 📌 Résultat

Après avoir exécuté la commande SSH, j'ai réussi à me connecter au serveur du jeu. Le message de bienvenue indique que je suis maintenant connecté en tant que `bandit3`.

![Connexion réussie](/bandit/level2to3/solution.png)

---

<p align="center">  <i>⬅️ <a href="/bandit/level1to2/rapport.md">Previous level</a></i> | <i><a href="/bandit/level3to4/rapport.md">Next level</a> ➡️</i></p>
<p align="center">  <i>↪️ Back to <a href="/bandit/sommaire.md">Summary</a></i> | <i>📍 From <a href="https://github.com/SybillLabs">SybillLabs</a></i></p>