# 02 — Homelab Linux virtualisé

**Contexte :** projet personnel
**Environnement :** Mac Apple Silicon · UTM · Ubuntu Server ARM64

## Objectif

Construire un petit laboratoire de machines virtuelles Linux pour pratiquer l'administration système et réseau en dehors des cours.

## Architecture

```
[ Mac (UTM) ]
   ├── VM Ubuntu Server ARM64 #1  ──┐
   └── VM Ubuntu Server ARM64 #2  ──┴── réseau virtuel UTM (ping + SSH)
```

Le lab a commencé avec deux machines virtuelles et en compte aujourd'hui davantage.

## Étapes réalisées

1. Création de machines virtuelles **Ubuntu Server ARM64** dans UTM (architecture adaptée au processeur Apple Silicon).
2. **Configuration réseau** des VM pour qu'elles communiquent entre elles.
3. **Tests de connectivité** avec `ping`.
4. Mise en place de l'**accès distant SSH** entre les machines.
5. Pratique de l'administration Linux : commandes de base, gestion des **fichiers**, des **utilisateurs** et des **permissions**.

```bash
# Exemples de commandes pratiquées
ip a                         # afficher la configuration IP
ping <ip_autre_vm>           # tester la connectivité
ssh utilisateur@<ip_autre_vm>
sudo adduser utilisateur2
chmod 640 fichier.txt
chown utilisateur2:groupe fichier.txt
```

## Problèmes rencontrés et solutions

| Problème | Solution |
|---|---|
| La VM redémarrait en boucle sur l'installateur | L'image ISO restait montée après l'installation : éjection de l'ISO du lecteur virtuel, puis redémarrage sur le disque |

## Ce que j'ai appris

- Choisir une image adaptée à l'architecture du processeur (ARM64 vs x86_64).
- Diagnostiquer un problème de démarrage de machine virtuelle.
- Les bases de l'administration Linux à distance avec SSH.
