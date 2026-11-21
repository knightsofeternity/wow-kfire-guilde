# KFIRE Guilde

L'add-on de guilde des Knights of Eternity pour WoW Forever (interface 16001) : page Guilde,
profils, demandes, artisanat, événements, statistiques de présence et quêtes en commun.
Détails dans [`KFireGuilde/README.md`](KFireGuilde/README.md).

Normalement, c'est le client [KFIRE](https://github.com/knightsofeternity/kfire-client) qui
l'installe dans Forever, quand la case « KFIRE Guilde » est cochée. Il y ajoute `Propose.lua`
(le pseudo KFIRE du joueur) et lit ensuite la photo de la guilde laissée dans les SavedVariables.

## Documents

- [`docs/kfire-guilde-cahier.md`](docs/kfire-guilde-cahier.md) : le cahier des charges, lots 1 à 5, et la recette.
- [`docs/kfire-guilde-liaison.md`](docs/kfire-guilde-liaison.md) : ce que l'add-on, le client et le serveur KFIRE s'échangent.

## Installation à la main

Copier le dossier `KFireGuilde/` dans `Interface/AddOns/` de WoW Forever.

## Tests

Un banc hors jeu en Lua 5.1 simule plusieurs joueurs de la guilde. Sans Lua installé :

```bash
docker run --rm -v "$PWD":/w -w /w alpine:3.20 sh -c "apk add -q lua5.1 >/dev/null 2>&1 && lua5.1 test/guilde.lua"
```
