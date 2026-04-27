
# 🧩 Community Database for the Altered TCG Cards

[![Fork me on GitHub](https://img.shields.io/badge/Fork%20me%20on-GitHub-blue?logo=github&style=for-the-badge)](https://github.com/AlteredCommunity/databases/fork)

> 💬 **Want to contribute or discuss this project? Join our community on Discord:**  
> [https://discord.gg/SNjWv2hD](https://discord.gg/SNjWv2hD)

---

## Goal

This project aims to gather as many cards from the **Altered** TCG as possible in a community-driven repository,  
without overloading the official servers with API requests.

🎯 **Why?**  
Repeated API calls can trigger throttling or server overload.  
We therefore recommend using this local JSON database first before making HTTP requests.

---

## Card ID Format

Card identifiers follow this structure:

```
ALT_SET_BOOSTER_FACTION_NUM_RARITY_VERSION
```

- `ALT`: fixed prefix
- `SET`: the card’s set (e.g., `ALIZE`)
- `BOOSTER`: booster type (e.g., `B`)
- `FACTION`: the card’s faction (e.g., `LY`)
- `NUM`: card number (e.g., `31`)
- `RARITY`: card rarity (`C`, `U`, `R`, etc.)
- `VERSION`: version number (e.g., `16`)

---

## Folder Structure

Files are stored using the following path pattern:

```
./SET/FACTION/NUM/ID.json
```

### Example

For the card ID:

```
ALT_ALIZE_B_LY_31_U_16
```

The file path will be:

```
./ALIZE/LY/31/ALT_ALIZE_B_LY_31_U_16.json
```

---

## Translations

Each card JSON file must include a top-level key called `translations`.

This key contains localized versions of the card as a dictionary, using **locale codes like `en-en`, `fr-fr`, `de-de`, etc.**  
Each value should mirror the structure of the main card JSON.

### Example structure:

```json
{
  "id": "ALT_ALIZE_B_LY_31_U_16",
  "type": "unit",
  "cost": 3,
  ...
  "translations": {
    "fr-fr": {},
    "nl-nl": {}
  }
}
```

---

## Goals

- Easy navigation and access by set / faction / number
- Prevent folders from becoming overcrowded
- Scalable and consistent structure
- Native support for multilingual content
- Minimize API calls to Altered servers

---

## Example File Tree

```
.
└── ALIZE
    └── LY
        └── 31
            └── ALT_ALIZE_B_LY_31_U_16.json
```

---

## Contributing

We welcome all contributions!

- You can **fork this repository** and start adding cards as you gather them.
- Once you've collected a good number of cards, feel free to **submit a pull request** with your additions.
- Before starting, it’s a good idea to check our **community discord** to see **who is working on what**, and avoid duplicating efforts.

---

# 🧩 Base de données communautaire des cartes du TCG Altered

[![Fork me on GitHub](https://img.shields.io/badge/Fork%20me%20on-GitHub-blue?logo=github&style=for-the-badge)](https://github.com/AlteredCommunity/databases/fork)

> 💬 **Vous souhaitez contribuer ou discuter du projet ? Rejoignez la communauté sur Discord :**  
> [https://discord.gg/SNjWv2hD](https://discord.gg/SNjWv2hD)

---

## Objectif

Ce projet vise à référencer un maximum de cartes du TCG **Altered** dans un dépôt communautaire,  
sans surcharger inutilement les serveurs officiels via des requêtes API.

🎯 **Pourquoi ?**  
Les appels répétés à l'API publique peuvent entraîner des limitations (`throttle`) ou surcharges.  
Nous recommandons donc d’utiliser cette base de données **en local**, en consultant d’abord nos fichiers JSON avant d’effectuer un appel HTTP.

---

## Format des identifiants

Les identifiants de cartes suivent cette structure :

```
ALT_SET_BOOSTER_FACTION_NUM_RARETE_VERSION
```

- `ALT` : préfixe fixe
- `SET` : le set de la carte (ex. `ALIZE`)
- `BOOSTER` : le type de booster (ex. `B`)
- `FACTION` : la faction de la carte (ex. `LY`)
- `NUM` : numéro de la carte (ex. `31`)
- `RARETE` : rareté (`C`, `U`, `R`, etc.)
- `VERSION` : version de la carte (ex. `16`)

---

## Arborescence des fichiers

Les fichiers sont enregistrés selon la structure suivante :

```
./SET/FACTION/NUM/ID.json
```

### Exemple

Pour l’identifiant :

```
ALT_ALIZE_B_LY_31_U_16
```

Le chemin du fichier sera :

```
./ALIZE/LY/31/ALT_ALIZE_B_LY_31_U_16.json
```

---

## Traductions

Chaque fichier JSON de carte doit contenir une clé principale appelée `translations`.

Cette clé contient un dictionnaire de versions localisées de la carte, avec des **codes de locale au format `en-en`, `fr-fr`, `de-de`, etc.**  
Chaque entrée reprend la même structure que le JSON principal.

### Exemple de structure :

```json
{
  "id": "ALT_ALIZE_B_LY_31_U_16",
  "type": "unit",
  "cost": 3,
  ...
  "translations": {
    "fr-fr": {},
    "nl-nl": {}
  }
}
```

---

## Objectifs

- Navigation facile par set / faction / numéro
- Éviter les dossiers trop chargés
- Structure cohérente et évolutive
- Prise en charge native du multilingue
- Éviter les appels superflus aux serveurs d'Altered

---

## Exemple d’arborescence

```
.
└── ALIZE
    └── LY
        └── 31
            └── ALT_ALIZE_B_LY_31_U_16.json
```

---

## Contribuer

Toutes les contributions sont les bienvenues !

- Vous pouvez **forker ce dépôt** et commencer à ajouter les cartes au fur et à mesure de votre collecte.
- Une fois un certain nombre de données rassemblées, vous pouvez **faire une pull request** pour les intégrer au projet.
- Avant de commencer, pensez à consulter notre **discord communautaire** afin de vérifier **qui s’occupe de quoi**, et éviter les doublons.