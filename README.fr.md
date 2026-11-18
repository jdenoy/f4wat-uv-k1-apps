# Apps UV-K1 / UV-K5 v3 (F4WAT)

*[English](README.md) · Français*

Applications overlay pour le firmware F4HWN d'Armel sur les radios Quansheng UV-K1 et UV-K5 v3. Elles tournent par-dessus le firmware sans le remplacer. Ce dépôt sert de point de distribution pour trouver la dernière version à jour de chaque app, notamment pour les postes de l'ADRASEC 27.

Les apps ici sont des outils de réception, de décodage et de radiogoniométrie. Aucune n'émet.

## Apps disponibles

| App | Version | Taille | Rôle | Télécharger |
|-----|---------|--------|------|-------------|
| Scan 406 | 1.9 | 4564 o | Balaye les canaux Cospas-Sarsat 406 MHz, lève une alarme sur une salve et passe la main à EPIRB 406 pour le décodage | [Scan406-v1.9.app](apps/scan406/Scan406-v1.9.app?raw=true) |
| EPIRB 406 | 3.6 | 5022 o | Décode sur la radio les balises de détresse 406 MHz de première génération : identifiant 15 hex, pays, protocole, position, contrôle BCH | [EPIRB406-v3.6.app](apps/epirb406/EPIRB406-v3.6.app?raw=true) |
| Sig Finder | 2.1 | 3669 o | Radiogoniométrie avec une antenne directive ; détecte le balayage caractéristique d'une balise de détresse 121,5 / 243 MHz et l'affiche | [SigFinder-v2.1.app](apps/sigfind/SigFinder-v2.1.app?raw=true) |

Chaque app vit dans `apps/<nom>/`. Le nom de fichier porte la version. Quand une nouvelle version sort, le fichier versionné est ajouté à côté de l'ancien et le tableau ci-dessus pointe vers la dernière. Les versions précédentes restent disponibles dans le dossier.

## Prérequis

Un firmware F4HWN (Labs ou Fusion) récent sur la radio, avec l'API app de niveau 3 ou plus. Scan 406 et Sig Finder ont besoin d'EPIRB 406 installé pour le passage de main. Le firmware et son code source sont chez Armel : https://github.com/armel/uv-k1-k5v3-firmware-custom

## Installation

Ces fichiers `.app` se chargent sur la radio avec l'outil de chargement d'apps overlay du firmware F4HWN. Le nom du fichier n'a pas d'importance pour la radio : la version et le nom affichés viennent de l'en-tête de l'app. Voir la documentation du firmware pour la procédure de chargement.

## Source et licence

Ces apps sont dérivées du firmware F4HWN d'Armel. Le code source complet de chaque app est public dans son dépôt, branche `feature_update_v7` :

- Scan 406 : `App/apps/scan406/`
- EPIRB 406 : `App/apps/epirb406/`
- Sig Finder : `App/apps/sigfind/` (dérivée de l'app FoxHunt d'Armel)

Dépôt amont : https://github.com/armel/uv-k1-k5v3-firmware-custom

## Usage

Outils radioamateurs et de secours (ADRASEC). Réception et décodage uniquement. Respecter la réglementation radioamateur en vigueur.

73, Johan F4WAT
