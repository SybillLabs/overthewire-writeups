<h1 align="center">🐧 OverTheWire - Bandit : Level 11 -> 12</h1>

## `> quickstart`
- **Objectif** : récupérer le mot de passe du compte `bandit12` depuis `bandit11`
- **Commandes utilisées** : 
```bash
ls -l /home/bandit11/
tr 'A-Za-z' 'N-ZA-Mn-za-m' < data.txt
exit
ssh -p 2220 bandit12@bandit.labs.overthewire.org
```

## `> methods`
- **Constat** : le mot de passe se trouve dans `data.txt`, chiffré par substitution **ROT13**
- **Action** : décodage du contenu de `data.txt` avec `tr`, chaque lettre étant remplacée par celle située 13 rangs plus loin, résultat lu directement en sortie standard

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