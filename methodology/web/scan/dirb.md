
# Rapport d'Analyse dirb

## Informations Générales
- **Cible du Scan :** [URL du site web cible]
- **Date et Heure du Scan :** [Date et heure du scan]

## 1. Scan avec Liste de Mots (`common.txt`)
### Commande :
```bash
dirb https://www.example.com/ /usr/share/dirb/wordlists/common.txt
```
### Objectif :
Le scan avec une liste de mots vise à découvrir des répertoires et fichiers cachés en utilisant une liste de mots couramment utilisés.

### Analyse :
Le scan a identifié des répertoires et fichiers potentiellement intéressants en utilisant une liste de mots courants.

**Exemple de Réponse :**
```
+ https://www.example.com/admin/ (CODE : 200)
+ https://www.example.com/test/ (CODE : 403)
+ https://www.example.com/backup/ (CODE : 404)
```

## 2. Scan Aggressif avec Extension Spécifique
### Commande :
```bash
dirb https://www.example.com/ /usr/share/dirb/wordlists/common.txt -X .php,.html
```
### Objectif :
Le scan aggressif avec une extension spécifique vise à cibler uniquement les fichiers avec des extensions particulières.

### Analyse :
Le scan a été focalisé sur les fichiers avec les extensions spécifiées, fournissant des informations plus précises sur les fichiers potentiellement vulnérables.

**Exemple de Réponse :**
```
+ https://www.example.com/index.php (CODE : 200)
+ https://www.example.com/login.php (CODE : 200)
+ https://www.example.com/about.html (CODE : 200)
```

## 3. Utilisation d'un Proxy (`--proxy`)
### Commande :
```bash
dirb https://www.example.com/ /usr/share/dirb/wordlists/common.txt --proxy http://monproxy:port
```
### Objectif :
L'utilisation d'un proxy permet de masquer l'origine du scan.

### Analyse :
Le scan a été effectué en utilisant le proxy spécifié, ce qui peut être utile pour maintenir l'anonymat.

**Exemple de Réponse :**
```
+ https://www.example.com/admin/ (CODE : 200)
+ https://www.example.com/test/ (CODE : 403)
+ https://www.example.com/backup/ (CODE : 404)
```

## Conclusion
L'analyse `dirb` avec les paramètres sélectionnés a permis d'identifier des répertoires et fichiers cachés sur le site web cible. Ces informations peuvent être utilisées pour évaluer la sécurité du site, détecter des points d'entrée potentiels, ou encore pour une évaluation plus approfondie de la surface d'attaque.
