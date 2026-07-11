<h1 align="center">🐧 OverTheWire - Bandit : Level 10 -> 11</h1>

## 🧭 Objectif
L'objectif est de trouver le mot de passe pour l'utilisateur `bandit11` en utilisant les informations trouvées avec l'utilisateur `bandit10`.
> **Note** : Le mot de passe pour l'utilisateur `bandit11`se trouve dans le fichier `data.txt` dans l'une des rares `strings`lisible par l'humain et précédé par plusieurs `=`.

## 🛠️ Les commandes utilisés

```bash
# Je suis déjà connecté en tant que bandit10, je peux donc directement trouver le fichier data.txt.
ls -l /home/bandit10/
strings data.txt | grep ==
    # strings pour afficher les chaînes de caractères lisibles par un humain dans le fichier data.txt
    # | grep == pour ne garder que les chaînes de caractères précédées par plusieurs =
# Le mot de passe pour l'utilisateur bandit11 est maintenant affiché dans le terminal.
# Je me déconnecte de bandit10 et me connecte à bandit11
exit
ssh -p 2220 bandit11@bandit.labs.overthewire.org
```

## 📌 Résultat

Après avoir exécuté la commande SSH, j'ai réussi à me connecter au serveur du jeu. Le message de bienvenue indique que je suis maintenant connecté en tant que `bandit11`.

![Connexion réussie](/bandit/12-level10to11/solution.png)

---

<p align="center">  <i>⬅️ <a href="/bandit/11-level9to10/rapport.md">Previous level</a></i> | <i><a href="/bandit/13-level11to12/rapport.md">Next level</a> ➡️</i></p>
<p align="center">  <i>↪️ Back to <a href="/bandit/sommaire.md">Summary</a></i> | <i>📍 From <a href="https://github.com/SybillLabs">SybillLabs</a></i></p>