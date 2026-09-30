<h1 align="center">🐧 OverTheWire - Bandit : Level 3 -> 4</h1>

## `> quickstart`
- **Objectif** : récupérer le mot de passe du compte `bandit4` depuis `bandit3`
- **Commandes utilisées** : 
```bash
ls -la /home/bandit3/inhere/
cat /home/bandit3/inhere/...Hiding-From-You
exit
ssh -p 2220 bandit4@bandit.labs.overthewire.org
```

## `> methods`
- **Constat** : le mot de passe est stocké dans un fichier caché du répertoire `inhere`
- **Action** : affichage du contenu du répertoire `inhere`, fichiers cachés inclus, avec `ls -la`, puis lecture du fichier caché avec `cat`

## `> results`

**Connexion réussie en tant que `bandit4`**.

![Connexion réussie](/bandit/05-level3to4/solution.png)

---

<p align="center">  
    <i>⬅️ <a href="/bandit/04-level2to3/rapport.md">Previous level</a></i> | <i><a href="/bandit/06-level4to5/rapport.md">Next level</a> ➡️</i>
</p>
<p align="center">  
    <i>↪️ Back to <a href="/bandit/sommaire.md">OverTheWire : Bandit</a></i>
</p>