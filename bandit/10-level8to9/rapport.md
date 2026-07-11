<h1 align="center">🐧 OverTheWire - Bandit : Level 8 -> 9</h1>

## 🧭 Objectif
L'objectif est de trouver le mot de passe pour l'utilisateur `bandit9` en utilisant les informations trouvées avec l'utilisateur `bandit8`.
> **Note** : Le mot de passe pour l'utilisateur `bandit9`se trouve dans le fichier `data.txt` et c'est la seule ligne de texte qui n'apparait qu'une seule fois dans le fichier.

## 🛠️ Les commandes utilisés

```bash
# Je suis déjà connecté en tant que bandit8, je peux donc directement trouver le fichier data.txt.
ls -l /home/bandit8/
sort data.txt | uniq -u
    # sort pour trier les lignes du fichier data.txt
    # uniq -u pour ne garder que les lignes uniques du fichier data.txt
# Le mot de passe pour l'utilisateur bandit9 est maintenant affiché dans le terminal.
# Je me déconnecte de bandit8 et me connecte à bandit9
exit
ssh -p 2220 bandit9@bandit.labs.overthewire.org
```

## 📌 Résultat

Après avoir exécuté la commande SSH, j'ai réussi à me connecter au serveur du jeu. Le message de bienvenue indique que je suis maintenant connecté en tant que `bandit9`.

![Connexion réussie](/bandit/10-level8to9/solution.png)

---

<p align="center">  <i>⬅️ <a href="/bandit/09-level7to8/rapport.md">Previous level</a></i> | <i><a href="/bandit/11-level9to10/rapport.md">Next level</a> ➡️</i></p>
<p align="center">  <i>↪️ Back to <a href="/bandit/sommaire.md">Summary</a></i> | <i>📍 From <a href="https://github.com/SybillLabs">SybillLabs</a></i></p>