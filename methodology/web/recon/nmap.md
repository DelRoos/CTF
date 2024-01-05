

# Rapport d'Analyse Nmap

## Informations Générales
- **Adresse IP du Serveur :** [Adresse IP du serveur cible]
- **Date et Heure de l'Analyse :** [Date et heure de l'analyse]

## 1. Scan de Ports
### Commande :
```bash
nmap -p 80,443,8080,8000 [Adresse IP du serveur]
```
### But :
Cette commande vise à identifier les ports ouverts sur le serveur. Dans un contexte de CTF, elle est utile pour déterminer quels services sont disponibles et peuvent être des cibles potentielles.

### Analyse :
Le scan de ports a révélé plusieurs services actifs, y compris des services web standard sur les ports 80 et 443, un service SSH sur le port 22, et un service web alternatif sur le port 8080. Cela fournit une base pour la sélection des cibles potentielles.

**Terminologie Technique :**
- **Scan de Ports :** Processus d'exploration des ports d'une machine pour déterminer quels services sont actifs et écoutent sur ces ports.
- **Ports Ouverts :** Ports sur lesquels des services sont actifs et accessibles.
- **Services Détectés :** Les applications ou processus qui écoutent sur les ports ouverts.

## 2. Scan de Versions Détaillées
### Commande :
```bash
nmap -sV [Adresse IP du serveur]
```
### But :
L'objectif de cette commande est d'obtenir des informations détaillées sur les versions des services en cours d'exécution. Cela permet d'identifier des vulnérabilités spécifiques associées à ces versions.

### Analyse :
La détection de versions a permis d'identifier Apache 2.4.18 et OpenSSH 7.2p2. Ceci est crucial pour évaluer les risques potentiels en recherchant des vulnérabilités connues associées à ces versions.

**Terminologie Technique :**
- **Détection de Versions :** Processus permettant d'identifier les versions spécifiques des services.
- **Vulnérabilités Connues :** Failles de sécurité documentées et pour lesquelles des correctifs ou des solutions existent.

## 3. Scripts NSE Pertinents
### Commande :
```bash
nmap --script=vuln [Adresse IP du serveur]
```
### But :
L'utilisation de scripts NSE ciblés sur les vulnérabilités permet une analyse automatisée des faiblesses potentielles du serveur. Cela accélère l'identification des points d'entrée possibles.

### Analyse :
L'exécution de scripts NSE dédiés à la détection de vulnérabilités a permis de repérer des points faibles spécifiques du serveur, offrant ainsi des pistes pour des attaques ciblées.

**Terminologie Technique :**
- **NSE (Nmap Scripting Engine) :** Moteur de scripts intégré à Nmap permettant d'automatiser diverses tâches, y compris la détection de vulnérabilités.
- **Vulnérabilités :** Faiblesses ou points faibles dans un système qui peuvent être exploités pour compromettre la sécurité.

## 4. Détection du Système d'Exploitation
### Commande :
```bash
nmap -O [Adresse IP du serveur]
```
### But :
La détection du système d'exploitation permet d'adapter les stratégies d'attaque en fonction du système cible, améliorant ainsi la pertinence des exploits à envisager.

### Analyse :
La détection a indiqué que le serveur utilise probablement un système Linux. Cette information est cruciale pour choisir des exploits adaptés à ce système d'exploitation spécifique.

**Terminologie Technique :**
- **Détection d'OS :** Processus visant à déterminer le système d'exploitation utilisé par la machine cible.
- **Exploits :** Techniques ou codes utilisés pour tirer parti de vulnérabilités et compromettre un système.

## 5. Scan Rapide
### Commande :
```bash
nmap -T4 [Adresse IP du serveur]
```
### But :
Un scan rapide est privilégié dans les situations où la rapidité est cruciale, par exemple dans un CTF. Cela permet d'obtenir des résultats significatifs de manière plus rapide.

### Analyse :
Le scan rapide a fourni des informations rapidement, ce qui est essentiel dans un CTF où la rapidité est une priorité.

**Terminologie Technique :**
- **Parallélisme :** Le nombre d'opérations simultanées effectuées par le scan.
- **Rapidité :** La vitesse à laquelle le scan est effectué.

## 6. Éviter la Résolution DNS et le Ping
### Commande :
```bash
nmap -n -Pn [Adresse IP du serveur]
```
### But :
Éviter la résolution DNS et les requêtes de ping permet de gagner du temps en se concentrant sur le scan des ports sans des étapes préliminaires non essentielles.

### Analyse :
La désactivation de la résolution DNS et de la découverte d'hôtes par ping a accéléré le processus sans compromettre les informations pertinentes.

**Terminologie Technique :**
- **Résolution DNS :** Processus de traduction des noms de domaine en adresses IP.
- **Ping :** Méthode utilisée pour déterminer la disponibilité d'un hôte en envoyant des paquets et

 en attendant une réponse.

## 7. Découverte de Scripts Vulnérables pour les Services Web
### Commande :
```bash
nmap --script=http-vuln* [Adresse IP du serveur]
```
### But :
L'utilisation de scripts spécifiques à la détection de vulnérabilités HTTP cible les services web, des cibles fréquentes dans un CTF.

### Analyse :
Cette commande a identifié des vulnérabilités potentielles spécifiques aux services web, fournissant des pistes pour des attaques orientées web.

**Terminologie Technique :**
- **Vulnérabilités HTTP :** Faiblesses de sécurité spécifiques aux services web.
- **Scripts NSE :** Scripts spécifiques écrits pour le Nmap Scripting Engine.

## 8. Option Aggressive Scan
### Commande :
```bash
nmap -A [Adresse IP du serveur]
```
### But :
L'option Aggressive Scan combine plusieurs fonctionnalités pour obtenir une analyse complète en une seule commande.

### Analyse :
L'utilisation de cette option a fourni une analyse exhaustive avec la détection de versions, d'OS et l'exécution de scripts, offrant une vue complète du serveur.

**Terminologie Technique :**
- **Analyse Aggressive :** Une approche de scan complète et intensive.
- **Détection de Versions, d'OS, et Scripts :** Processus d'identification des versions des services, du système d'exploitation, et l'exécution de scripts.

## 9. Réduction des Scripts Non-Intrusifs
### Commande :
```bash
nmap --script=default [Adresse IP du serveur]
```
### But :
L'utilisation de scripts non-intrusifs est essentielle lorsque des actions intrusives peuvent être limitées. Cela garantit une analyse sans perturbation excessive du serveur.

### Analyse :
L'exécution de scripts par défaut a permis d'obtenir des informations sans risque d'interférence majeure avec le serveur.

**Terminologie Technique :**
- **Scripts par Défaut :** Ensemble de scripts inclus dans `nmap` qui sont considérés comme non-intrusifs.
- **Actions Intrusives :** Des actions qui pourraient perturber ou compromettre le fonctionnement normal du serveur.
