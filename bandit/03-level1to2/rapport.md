<h1 align="center">🐧 OverTheWire - Bandit : Level 1 -> 2</h1>

## `> quickstart`
- **Objectif** : récupérer le mot de passe du compte `bandit2` depuis `bandit1`
- **Commandes utilisées** : 
```bash
ls -l /home/bandit1/-
cat /home/bandit1/-
exit
ssh -p 2220 bandit2@bandit.labs.overthewire.org
```

## `> methods`
- **Constat** : le mot de passe est stocké dans un fichier nommé `-`, situé dans le répertoire personnel de `bandit1`
- **Action** : lecture du fichier avec `cat`, en donnant son chemin absolu pour que le nom `-` ne soit pas interprété comme l'entrée standard

## `> results`

**Connexion réussie en tant que `bandit2`**.

![Connexion réussie](/bandit/03-level1to2/solution.png)

---

<p align="center">  
    <i>⬅️ <a href="/bandit/02-level0to1/rapport.md">Previous level</a></i> | <i><a href="/bandit/04-level2to3/rapport.md">Next level</a> ➡️</i>
</p>
<p align="center">  
    <i>↪️ Back to <a href="/bandit/sommaire.md">OverTheWire : Bandit</a></i>
</p>