# Installation de Hydra sur Debian 12

Pour installer **Hydra** sur Debian 12, suivez les étapes ci-dessous.

## 1. Mise à jour du système

Tout d'abord, assurez-vous que votre système est à jour :

```bash
sudo apt update && sudo apt upgrade -y
```

## 2. Installation des dépendances nécessaires

```bash
sudo apt install build-essential libssl-dev libssh-dev libidn11-dev libpcre3-dev libgtk2.0-dev \
libmariadb-dev-compat libpq-dev libsvn-dev libgpgme-dev git zlib1g-dev libgcrypt20-dev -y
```

## 3. Téléchargement de Hydra

```bash
git clone https://github.com/vanhauser-thc/thc-hydra.git
```

## 4. Compilation de Hydra

```bash
cd thc-hydra
./configure
make
```

## 5. Installation de Hydra

```bash
sudo make install
```

## 6. Vérification de l'installation

```bash
hydra -h
```

# Installation de Nmap

```bash
sudo apt install nmap -y
```

### Explications

* Hydra
Hydra est un outil de "force brute" utilisé pour tester la sécurité des mots de passe sur divers services en réseau, comme SSH, FTP, HTTP, MySQL, et bien d'autres. Il essaie une liste de combinaisons de noms d'utilisateur et de mots de passe sur un service ciblé jusqu'à trouver les bonnes informations d'identification, ce qui peut aider les administrateurs système à identifier et à corriger des failles de sécurité dans leurs systèmes avant qu'elles ne soient exploitées par des attaquants.

* Nmap
Nmap (Network Mapper) est un outil de balayage et de découverte de réseau. Il est utilisé pour explorer les réseaux et vérifier la sécurité des systèmes en identifiant les hôtes connectés, les ports ouverts, les services disponibles, et les informations sur les versions des logiciels. Nmap est couramment utilisé pour effectuer des audits de sécurité, détecter les vulnérabilités, et cartographier la topologie des réseaux.

En résumé, Hydra est principalement utilisé pour tester la robustesse des mots de passe, tandis que Nmap sert à cartographier et analyser les réseaux pour identifier les services exposés et les vulnérabilités potentielles.