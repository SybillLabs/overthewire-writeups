<h1 align="center">🐧 OverTheWire - Bandit : Level 3 -> 4</h1>

## 🧭 Objectif
L'objectif est de trouver le mot de passe pour l'utilisateur `bandit4` en utilisant les informations trouvées avec l'utilisateur `bandit3`.
> **Note** : Le mot de passe pour l'utilisateur `bandit4`se trouve dans un fichier caché se trouvant dans le dossier `inhere` situé dans le répertoire `home directory`.

## 🛠️ Les commandes utilisés

```bash
# Je suis déjà connecté en tant que bandit3, je peux donc directement trouver le dossier inhere et le fichier caché
# Toujours vérifié que le dossier et le fichier existent et que j'ai les permissions nécessaires pour le lire
ls -l /home/bandit3/inhere/
# Lecture du fichier caché pour obtenir le mot de passe
cat /home/bandit3/inhere/...Hiding-From-You
# Le mot de passe pour l'utilisateur bandit4 est maintenant affiché dans le terminal.
# Je me déconnecte de bandit3 et me connecte à bandit4
exit
ssh -p 2220 bandit4@bandit.labs.overthewire.org
```

## 📌 Résultat

Après avoir exécuté la commande SSH, j'ai réussi à me connecter au serveur du jeu. Le message de bienvenue indique que je suis maintenant connecté en tant que `bandit4`.

![Connexion réussie](/bandit/level3to4/solution.png)

---

<p align="center">  <i>⬅️ <a href="/bandit/level2to3/rapport.md">Previous level</a></i> | <i><a href="/bandit/level4to5/rapport.md">Next level</a> ➡️</i></p>
<p align="center">  <i>↪️ Back to <a href="/bandit/sommaire.md">Summary</a></i> | <i>📍 From <a href="https://github.com/SybillLabs">SybillLabs</a></i></p>