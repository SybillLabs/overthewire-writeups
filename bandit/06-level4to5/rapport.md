<h1 align="center">🐧 OverTheWire - Bandit : Level 4 -> 5</h1>

## `> quickstart`
- **Objectif** : récupérer le mot de passe du compte `bandit5` depuis `bandit4`
- **Commandes utilisées** : 
```bash
ls -l /home/bandit4/inhere/
file /home/bandit4/inhere/* | grep "ASCII text"
cat /home/bandit4/inhere/-file07
exit
ssh -p 2220 bandit5@bandit.labs.overthewire.org
```

## `> methods`
- **Constat** : le mot de passe est stocké dans le seul fichier lisible par un humain du répertoire `inhere`
- **Action** : identification du type de chaque fichier du répertoire `inhere` avec `file`, filtrage des fichiers de type texte (`ASCII text`) avec `grep`, puis lecture du fichier retenu avec `cat`

## `> results`

**Connexion réussie en tant que `bandit5`**.

![Connexion réussie](/bandit/06-level4to5/solution.png)

---

<p align="center">  
    <i>⬅️ <a href="/bandit/05-level3to4/rapport.md">Previous level</a></i> | <i><a href="/bandit/07-level5to6/rapport.md">Next level</a> ➡️</i>
</p>
<p align="center">  
    <i>↪️ Back to <a href="/bandit/sommaire.md">OverTheWire : Bandit</a></i>
</p>