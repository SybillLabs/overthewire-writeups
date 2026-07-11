<h1 align="center">🐧 OverTheWire - Bandit : Level 4 -> 5</h1>

## 🧭 Objectif
L'objectif est de trouver le mot de passe pour l'utilisateur `bandit5` en utilisant les informations trouvées avec l'utilisateur `bandit4`.
> **Note** : Le mot de passe pour l'utilisateur `bandit5`se trouve dans un fichier lisible seulement par l'humain et se trouvant dans le dossier `inhere` situé dans le répertoire `home directory`.

## 🛠️ Les commandes utilisés

```bash
# Je suis déjà connecté en tant que bandit4, je peux donc directement trouver le dossier inhere et le fichier lisible seulement par l'humain
# Toujours vérifié que le dossier et le fichier existent et que j'ai les permissions nécessaires pour le lire
ls -l /home/bandit4/inhere/
# Maintenant il faut trouver le bon fichier lisible seulement par l'humain
file /home/bandit4/inhere/* | grep "ASCII text"
    # "ASCII text" permet de savoir que le fichier est lisible seulement par l'humain
# Lecture du fichier lisible seulement par l'humain pour obtenir le mot de passe
cat /home/bandit4/inhere/-file07
# Le mot de passe pour l'utilisateur bandit5 est maintenant affiché dans le terminal.
# Je me déconnecte de bandit4 et me connecte à bandit5
exit
ssh -p 2220 bandit5@bandit.labs.overthewire.org
```

## 📌 Résultat

Après avoir exécuté la commande SSH, j'ai réussi à me connecter au serveur du jeu. Le message de bienvenue indique que je suis maintenant connecté en tant que `bandit5`.

![Connexion réussie](/bandit/06-level4to5/solution.png)

---

<p align="center">  <i>⬅️ <a href="/bandit/05-level3to4/rapport.md">Previous level</a></i> | <i><a href="/bandit/07-level5to6/rapport.md">Next level</a> ➡️</i></p>
<p align="center">  <i>↪️ Back to <a href="/bandit/sommaire.md">Summary</a></i> | <i>📍 From <a href="https://github.com/SybillLabs">SybillLabs</a></i></p>