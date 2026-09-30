<h1 align="center">🐧 OverTheWire - Bandit : Level 11 -> 12</h1>

## `> quickstart`
- **Objectif** : se connecter au serveur **OverTheWire** via une connexion SSH en tant que `bandit12`
- **Commandes utilisées** : 
```bash
ls -l /home/bandit11/
tr 'A-Za-z' 'N-ZA-Mn-za-m' < data.txt
exit
ssh -p 2220 bandit12@bandit.labs.overthewire.org
```

## `> methods`
- Mot de passe stocké dans un fichier **data.txt**, où un décalage `Rot13` a été appliqué
- Commande `tr` retenu, le **Rot13** est une simple substitution de caractères, cœur de la fonction de `tr`

## `> results`

**Connexion réussie en tant que `bandit12`**.

![Connexion réussie](/bandit/13-level11to12/solution.png)

---

<p align="center">  
    <i>⬅️ <a href="/bandit/12-level10to11/rapport.md">Previous level</a></i> | <i><a href="/bandit/14-level12to13/rapport.md">Next level</a> ➡️</i>
</p>
<p align="center">  
    <i>↪️ Back to <a href="/bandit/sommaire.md">OverTheWire : Bandit</a></i>
</p>