# RTSTutoriel

Projet servant de template pour créer un jeu en RTS sous unreal engine 5 en BP

## Prérequis
- Unreal Engine 5.7 (Toutes versions inférieurs ne sont pas supportées)

## Structure du project

```
_Main/
├─ Blueprint/
│  ├─ Building/
│  ├─ BuildingType/
│  ├─ Enum/
│  ├─ GameMode/
│  ├─ HUD/
│  ├─ Interface/
│  ├─ Player/
│  ├─ PlayerController/
│  ├─ Ressource/
│  ├─ UI/
│  ├─ Unit/
│  ├─ UnitGroup/
│  ├─ UnitType/
├─ Level/
│  ├─ DevMap.umap
├─ Material/
│  ├─ Building/
│  │  ├─ Focus/
│  ├─ Unit/
│  │  ├─ ValidConstruction/
Asset/
├─ Misc/ # Personnalisable, non pris en charge.
```
### Les règles de structure

La logique de la structure du project est que chaque `Feature` aura son propre dossier, mais peut être dépendant d'un autre dossier.
Tout ficher qui n'est pas de logique (non-blueprint) dois être dans un autre dossier que celui du `Blueprint`, le fichier doit être mis dans un dossier portant le nom de la `Feature`, Si le fichier est dépendant d'une classe blueprint, le dossier de la feature doit être un sous dossier d'un dossier portant le nom de la `Feature` de la classe `Blueprint`.  p. ex. `Material/Building/Focus`.

La raison de cette structure permet de savoir à quoi correspond les fichiers grâce aux noms des dossiers contenant la `Feature`. Mais il faudra attention, car la structure peut être à lire au fur et à mesure que le projet grossit.

## _Main
Ce dossier contient tous le jeu.

### Blueprint
Ce dossier contient toute la logique du jeu. Donc si vous créez une nouvelle `Feature`, il sera préférable de le mettre dans ce dossier.
pour l'instant, le dossier ne respect pas à la lettre les règles de structure du project, car le dossier contient des Static Mesh (`SM`).


## Asset
Tous les assets qui viennent de FAB. (N'a pas de règle précis)



