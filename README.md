# Homelab MarocFinance — Infrastructure IT

Labs pratiques simulant une infrastructure enterprise réelle
basée sur le scénario d'une société financière marocaine.

## Environnement technique
- Cisco Packet Tracer (réseau)
- Windows Server 2022 (Active Directory, GPO)
- Ubuntu Server 22.04 (Linux, SSH, UFW, Cron, Bash)

## Labs réalisés

### Lab 1 — Segmentation Réseau Siège Casablanca
- Topologie hiérarchique : Core → Distribution → Accès
- 5 VLANs départementaux (Compta, RH, Direction, IT, Serveurs)
- Router-on-a-stick (inter-VLAN routing)
- ACL étendues : isolation Comptabilité / Serveur RH
- Tests de connectivité validés

### Lab 2 — Active Directory & GPO
- Déploiement Windows Server 2022 en Domain Controller
- Domaine : marocfinance.local
- Structure OUs : Casablanca → Comptabilite, RH, Direction, IT, Serveurs
- Utilisateurs et groupes de sécurité par département
- GPO politique de mots de passe (10 car., complexité, 90 jours)
- GPO verrouillage de session (5 min)
- GPO restriction panneau de configuration (Comptabilité)
- Tests validés sur poste Windows 10 joint au domaine

### Lab 3 — Administration Serveur Linux
- Ubuntu Server 22.04
- SSH sécurisé : port 2222, PermitRootLogin no, AllowGroups it
- Firewall UFW : deny par défaut, ports 2222/80/443 autorisés
- Gestion utilisateurs et groupes par département
- Script de sauvegarde automatique /etc → tar.gz avec log
- Planification cron : exécution quotidienne à 2h

## Compétences démontrées
`Cisco IOS` `VLANs` `ACL` `Router-on-a-stick`
`Windows Server 2022` `Active Directory` `GPO`
`Ubuntu Server` `SSH` `UFW` `Bash` `Cron`
