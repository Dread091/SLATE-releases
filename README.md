# SLATE — releases

**SLATE** génère des missions DCS World pour des groupes de 10 à 20 pilotes : campagne
dynamique par secteurs, forces ennemies finies (chaque perte est définitive), tableau de
missions F10, IA alliée, logistique et scoring, prévu pour un serveur dédié 24/7.

Ce dépôt ne contient que les versions téléchargeables. Le code source n'est pas public.

## Télécharger

Prenez le zip `SLATE-<version>-win64.zip` de la dernière version dans
[**Releases**](https://github.com/Dread091/SLATE-releases/releases/latest).

Windows 64 bits, aucune installation requise (pas besoin de Python). Dézippez le dossier
`SLATE` où vous voulez, de préférence hors de `Program Files`.

## Démarrage rapide

1. Glissez un scénario `.yaml` (par ex. `SLATE_Missions\SLATE_Syria_v1.yaml`) sur
   `slate-build.bat`. Le `.miz` est créé à côté du `.yaml`.
2. Copiez le `.miz` dans `Saved Games\DCS\Missions` (ou dans celui du serveur dédié).
3. Pour garder la progression de la campagne entre deux reboots, commentez
   `sanitizeModule('io')` et `sanitizeModule('lfs')` dans
   `<DCS>\Scripts\MissionScripting.lua`.

En ligne de commande, depuis le dossier `SLATE` :

```bat
slate build SLATE_Missions\SLATE_Syria_v1.yaml
slate build SLATE_Missions\SLATE_Syria_v1.yaml --seed 42
slate validate SLATE_Missions\SLATE_Syria_v1.yaml
```

## Documentation

Chaque zip contient :

- `LISEZMOI.txt` : installation, serveur, sauvegardes, problèmes courants ;
- `Manuel_Integrateur.md` : guide complet pour créer ou modifier un scénario.

`slate.exe` n'est pas signé : Windows SmartScreen peut afficher un avertissement
(« Informations complémentaires » puis « Exécuter quand même »).

## Licence

[PolyForm Noncommercial 1.0.0](https://polyformproject.org/licenses/noncommercial/1.0.0/) :
usage non commercial uniquement. Les composants tiers (python-dcs, MOOSE, AIEN,
Splash Damage…) restent sous leur propre licence ; voir `THIRD_PARTY.txt` dans le zip.
