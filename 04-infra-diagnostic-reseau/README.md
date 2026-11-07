# 04 — Services d'infrastructure et diagnostic réseau

**Contexte :** travaux pratiques BTS SIO
**Thèmes :** DNS · DHCP · Windows Server · Nmap

## Objectif

Découvrir les services réseau de base d'une infrastructure d'entreprise et les outils de diagnostic.

## Travaux réalisés

- Découverte des services **DNS** (résolution de noms) et **DHCP** (attribution automatique des adresses IP).
- Prise en main de **Windows Server**.
- Diagnostic de la connectivité et de la configuration IP :

```bash
ping <adresse>     # tester la connectivité
ipconfig /all      # configuration IP sous Windows
ip a               # configuration IP sous Linux
```

- Initiation au **scan réseau avec Nmap** sur mon propre lab, pour identifier les ports ouverts et les services :

```bash
nmap <adresse_du_lab>
nmap -sV <adresse_du_lab>   # détecter les services et leurs versions
```

> Les scans Nmap sont réalisés uniquement sur mes propres machines ou dans le cadre des TP. Scanner un réseau sans autorisation est illégal.

## Ce que j'ai appris

- Le rôle du DNS et du DHCP dans un réseau d'entreprise.
- Une méthode de diagnostic : vérifier la configuration IP, puis la connectivité, puis les services.
- Comment un attaquant ou un administrateur peut cartographier les services exposés d'une machine.
