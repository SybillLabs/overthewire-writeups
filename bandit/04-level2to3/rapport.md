<h1 align="center">🐧 OverTheWire - Bandit : Level 2 -> 3</h1>

## `> quickstart`
- **Objectif** : récupérer le mot de passe du compte `bandit3` depuis `bandit2`
- **Commandes utilisées** : 
```bash
ls -l /home/bandit2/--spaces in this filename--
cat /home/bandit2/--spaces in this filename--
exit
ssh -p 2220 bandit3@bandit.labs.overthewire.org
```

## `> methods`
- **Constat** : le mot de passe est stocké dans un fichier nommé `--spaces in this filename--`, situé dans le répertoire personnel de `bandit2`
- **Action** : lecture du fichier avec `cat`, en donnant son chemin absolu pour que les tirets initiaux ne soient pas interprétés comme des options

## `> results`

**Connexion réussie en tant que `bandit3`**.

![Connexion réussie](/bandit/04-level2to3/solution.png)

---

<p align="center">  
    <i>⬅️ <a href="/bandit/03-level1to2/rapport.md">Previous level</a></i> | <i><a href="/bandit/05-level3to4/rapport.md">Next level</a> ➡️</i>
</p>
<p align="center">  
    <i>↪️ Back to <a href="/bandit/sommaire.md">OverTheWire : Bandit</a></i>
</p>