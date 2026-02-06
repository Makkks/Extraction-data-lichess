## Qu’est-ce que qBittorrent ?

qBittorrent est un logiciel open source permettant de télécharger des fichiers
à partir de liens fournis sur Internet, notamment via des URL HTTP ou des fichiers torrent.

Dans ce projet, qBittorrent est utilisé comme un **outil de récupération contrôlée de données**,
et non comme un simple téléchargeur classique.

---

## Principe d’utilisation dans ce projet

L’utilisation de qBittorrent est volontairement simple :

1. Il suffit d’insérer une **URL HTTP** pointant vers un fichier de données open source.
2. Le téléchargement démarre progressivement.
3. L’utilisateur décide **manuellement quand arrêter** le téléchargement.

Ce contrôle manuel permet de ne récupérer qu’une partie du fichier,
en fonction de l’objectif de l’extraction.

---

## Gestion du volume de données

Les fichiers de données peuvent être très volumineux.
Plus la date recherchée est **ancienne**, plus il est nécessaire de charger
une portion importante du document pour atteindre les données souhaitées.

À l’inverse, pour des dates récentes, une partie plus réduite du fichier suffit.

L’utilisateur peut donc :
- lancer le téléchargement
- observer la progression
- mettre en pause ou arrêter manuellement lorsque la date cible est atteinte

---

## Avantages de cette approche

Cette méthode présente plusieurs avantages :

- économie importante d’espace de stockage
- rapidité de mise en œuvre
- contrôle total sur le volume de données récupérées
- utilisation d’un outil open source

Elle permet d’accéder efficacement à des données précises
sans avoir à télécharger l’intégralité des fichiers disponibles.
