# JD-XI-prog

Étude de firmware pour adapter une expérience de synthétiseur hybride inspirée du Roland JD-Xi au M-VAVE FM-1.

Ce dépôt est un projet de développement fondé sur le SDK officiel open-source du FM-1. Il ne contient pas encore de micrologiciel testé sur matériel.

## Objectif

Créer une variante du firmware FM-1 avec :

- un moteur FM et des instruments alternatives ;
- 8 pistes séquenceur ;
- MIDI DIN, USB et BLE ;
- une interface inspirée du JD-Xi ;
- des patches hybrid analog/Fm-style en simulation logicielle.

## Prérequis

- Windows x64
- SDK officiel [m-vave/fm1_open](https://github.com/m-vave/fm1_open)
- JieLi Windows toolchain 2.5.3 correspondant
- Une sauvegarde complète de la configuration et du matériel FM-1

## Développement

Téléchargez le jeu complet « Source + SDK » fourni par M-VAVE, puis placez son contenu à la racine de ce dépôt. Ne mélangez pas les SDK ou toolchains provenant de versions différentes.

La commande de compilation locale doit être exécutée depuis Windows PowerShell :

```powershell
./sdk/Build.ps1 -FirmwareOnly -Toolchain 'C:\JL\pi32'
```

Le fichier à produire est normalement :

```text
build/dx7/generated/FM1_OFFICIAL_OPEN.fwsc
```

## Sécurité

Sauvegardez les projets, banques DX7 et échantillons avant toute mise à jour. Aucun `.fwsc` produit par ce dépôt n’est actuellement validé matériellement.
