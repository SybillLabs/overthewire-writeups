<h1 align="center">🐧 OverTheWire - Bandit : Level 5 -> 6</h1>

## `> quickstart`
- **Objectif** : récupérer le mot de passe du compte `bandit6` depuis `bandit5`
- **Commandes utilisées** : 
```bash
ls -l /home/bandit5/inhere/
find /home/bandit5/inhere/ -type f -size 1033c ! -executable -exec file {} \; | grep "ASCII text"
cat /home/bandit5/inhere/maybehere07/.file2
exit
ssh -p 2220 bandit6@bandit.labs.overthewire.org
```

## `> methods`
- **Constat** : le mot de passe est stocké dans un fichier situé quelque part sous le répertoire `inhere`, dont les propriétés sont connues :
    - lisible par un humain
    - taille : 1033 octets
    - non exécutable
- **Action** : recherche des fichiers sous `inhere` avec `find`, en filtrant sur le type fichier, la taille de 1033 octets et l'absence de droit d'exécution, identification du type de chaque fichier trouvé avec `file`, puis filtrage des fichiers texte (`ASCII text`) avec `grep`, et lecture du fichier retenu avec `cat`

## `> results`

**Connexion réussie en tant que `bandit6`**.

![Connexion réussie](/bandit/07-level5to6/solution.png)

---

<p align="center">  
    <i>⬅️ <a href="/bandit/06-level4to5/rapport.md">Previous level</a></i> | <i><a href="/bandit/08-level6to7/rapport.md">Next level</a> ➡️</i>
</p>
<p align="center">  
    <i>↪️ Back to <a href="/bandit/sommaire.md">OverTheWire : Bandit</a></i>
</p>