# 03 — Serveur web Debian à domicile

**Contexte :** travaux pratiques BTS (module U7 — cybersécurité des services informatiques)
**Environnement :** machine virtuelle Debian · serveur web Apache · poste client Windows

## Objectif

Mettre en place, chez soi, un serveur web Debian accessible depuis un poste Windows par un **nom de domaine local** plutôt que par son adresse IP.

## Étapes réalisées

1. Installation d'une **machine virtuelle Debian**.
2. Configuration d'une **adresse IP fixe**.
3. **Test de l'accès Internet** depuis la VM.
4. Installation et démarrage du serveur web **Apache** :

```bash
sudo apt update
sudo apt install apache2
sudo systemctl status apache2   # vérifier que le service est actif
```
5. Sur le poste **Windows**, ajout d'une entrée dans le fichier `hosts` pour associer un nom local à l'adresse IP de la VM :

```
# C:\Windows\System32\drivers\etc\hosts
192.168.X.20    prenom.lan
```

6. Vérification : ouverture de `http://prenom.lan` dans le navigateur du poste Windows.

## Ce que j'ai appris

- La **résolution de noms** : le fichier `hosts` est consulté avant le DNS, ce qui permet de nommer une machine sans serveur DNS.
- L'importance d'une **IP fixe** pour un serveur : si l'adresse change, le nom ne pointe plus vers la bonne machine.
