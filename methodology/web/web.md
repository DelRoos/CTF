

# Catégorie : Web

### 1. Reconnaissance

- **Objectif :** Identifier des faiblesses potentielles sur le site et collecter des informations cruciales.

- **Outils utilisés :**
  - `nmap` : Découvrir les services en cours d'exécution sur le serveur.
  - `whatweb` : Identifier les technologies web utilisées.
  - `theHarvester` : Collecter des informations sur le domaine.

#### Résultats

- Adresse IP : [Adresse IP du serveur]
- Technologies : Apache, PHP, MySQL
- Informations WHOIS : Propriétaire - [Nom de l'entreprise], administrateur - [Nom de l'administrateur]

### 2. Scanning

- **Objectif :** Détecter des vulnérabilités potentielles ou des points d'entrée cachés.

- **Outils utilisés :**
  - `dirb` ou `gobuster` : Scanner de répertoires pour découvrir des pages cachées.
  - `nikto` : Scanner de vulnérabilités web.

#### Résultats

- Ports ouverts : 80 (HTTP), 443 (HTTPS)
- Répertoires découverts : /admin, /uploads

### 3. Analyse des vulnérabilités

- **Objectif :** Détecter et exploiter des vulnérabilités web pour obtenir le flag.

- **Outils utilisés :**
  - `sqlmap` : Exploiter les failles SQL.
  - `Burp Suite` : Tester les failles XSS.

#### Résultats

- Vulnérabilité SQL dans la page de connexion.
- Injection XSS persistante dans la fonction de recherche.

### 4. Exploitation

- **Objectif :** Utiliser les vulnérabilités pour obtenir le flag.

- **Outils utilisés :**
  - `Metasploit` : Automatiser l'exploitation des vulnérabilités.
  - `sqlmap` : Exploiter les failles SQL.

#### Résultats

- Accès à la base de données avec les identifiants récupérés.
- Contrôle de session utilisateur via l'injection XSS persistante.

### 5. Recherche du Flag

- **Objectif :** Identifier la présence du flag dans la base de données ou dans les fichiers du serveur.

- **Outils utilisés :**
  - Consultation directe de la base de données avec des outils comme `phpMyAdmin`.
  - Recherche dans les fichiers du serveur avec des commandes telles que `grep`.

#### Résultats

- Identification du flag : `{FLAG_WEB_123}`
