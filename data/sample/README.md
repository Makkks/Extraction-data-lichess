# Données échantillon

## Description

Ce dossier contient un **échantillon de données** issu de l’extraction complète
réalisée à partir des bases open source de Lichess.

Les lignes présentes dans ce fichier ont été **choisies au hasard**
parmi l’ensemble des parties extraites.
Elles ne représentent pas un sous-ensemble spécifique ni un cas particulier.

L’objectif de cet échantillon est uniquement de :
- montrer le **format des données**
- illustrer les **colonnes disponibles**
- permettre une compréhension rapide du dataset

Les données complètes ne sont pas partagées dans ce repository.

---

## Fichier contenu

- `games_sample.txt`  
  Échantillon de parties d’échecs extrait du jeu de données complet.

---

## Colonnes disponibles

Le fichier échantillon contient les colonnes suivantes :

- `game_id` : identifiant unique de la partie
- `utc_date` : date de la partie
- `utc_time` : heure de début de la partie
- `time_control` : cadence de jeu
- `termination` : type de fin de partie
- `eco` : code ECO de l’ouverture
- `opening_name` : nom de l’ouverture
- `num_moves` : nombre total de coups joués
- `white_elo` : classement du joueur avec les blancs
- `black_elo` : classement du joueur avec les noirs
- `elo_diff` : différence de classement entre les joueurs
- `result` : résultat de la partie (format PGN)
- `winner` : vainqueur de la partie (blancs, noirs ou nul)

---

## Remarque

Cet échantillon est fourni à titre illustratif.
Il permet de comprendre la structure des données sans exposer
le volume complet ni les fichiers bruts d’origine.
