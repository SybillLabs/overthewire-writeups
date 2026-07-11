<h1 align="center">🐧 OverTheWire - Bandit : Level 9 -> 10</h1>

## 🧭 Objectif
L'objectif est de trouver le mot de passe pour l'utilisateur `bandit10` en utilisant les informations trouvées avec l'utilisateur `bandit9`.
> **Note** : Le mot de passe pour l'utilisateur `bandit10`se trouve dans le fichier `data.txt` dans l'une des rares `strings`lisible par l'humain et précédé par plusieurs `=`.

## 🛠️ Les commandes utilisés

```bash
# Je suis déjà connecté en tant que bandit9, je peux donc directement trouver le fichier data.txt.
ls -l /home/bandit9/
strings data.txt | grep ==
    # strings pour afficher les chaînes de caractères lisibles par un humain dans le fichier data.txt
    # | grep == pour ne garder que les chaînes de caractères précédées par plusieurs =
# Le mot de passe pour l'utilisateur bandit10 est maintenant affiché dans le terminal.
# Je me déconnecte de bandit9 et me connecte à bandit10
exit
ssh -p 2220 bandit10@bandit.labs.overthewire.org
```

## 📌 Résultat

Après avoir exécuté la commande SSH, j'ai réussi à me connecter au serveur du jeu. Le message de bienvenue indique que je suis maintenant connecté en tant que `bandit10`.

![Connexion réussie](/bandit/11-level9to10/solution.png)

---

<p align="center">  <i>⬅️ <a href="/bandit/10-level8to9/rapport.md">Previous level</a></i> | <i><a href="/bandit/12-level10to11/rapport.md">Next level</a> ➡️</i></p>
<p align="center">  <i>↪️ Back to <a href="/bandit/sommaire.md">Summary</a></i> | <i>📍 From <a href="https://github.com/SybillLabs">SybillLabs</a></i></p>