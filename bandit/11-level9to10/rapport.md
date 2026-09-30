<h1 align="center">🐧 OverTheWire - Bandit : Level 9 -> 10</h1>

## `> quickstart`
- **Objectif** : récupérer le mot de passe du compte `bandit10` depuis `bandit9`
- **Commandes utilisées** : 
```bash
ls -l /home/bandit9/
strings data.txt | grep '=='
exit
ssh -p 2220 bandit10@bandit.labs.overthewire.org
```

## `> methods`
- **Constat** : le mot de passe se trouve dans `data.txt`, parmi les rares chaînes lisibles d'un contenu majoritairement illisible, précédé de plusieurs caractères `=`
- **Action** : extraction des chaînes lisibles de `data.txt` avec `strings`, puis filtrage des lignes contenant `==` avec `grep`

## `> results`

**Connexion réussie en tant que `bandit10`**.

![Connexion réussie](/bandit/11-level9to10/solution.png)

---

<p align="center">  
    <i>⬅️ <a href="/bandit/10-level8to9/rapport.md">Previous level</a></i> | <i><a href="/bandit/12-level10to11/rapport.md">Next level</a> ➡️</i>
</p>
<p align="center">  
    <i>↪️ Back to <a href="/bandit/sommaire.md">OverTheWire : Bandit</a></i>
</p>