# Extraction des données

## Rôle de cette partie

Cette section du projet regroupe la logique d’extraction et de préparation
des données issues des bases open source de Lichess.

L’extraction repose sur un notebook unique, qui permet de transformer
des données brutes volumineuses en un fichier structuré et exploitable.

---

## Principe général

Le processus est le suivant :

1. Les données brutes sont récupérées via un fichier PGN compressé (.pgn.zst),
   issu des bases publiques de Lichess.
2. L’utilisateur contrôle manuellement la durée de l’extraction
   en décidant quand arrêter le traitement.
3. Le notebook lit les données progressivement, sans charger le fichier entier en mémoire.
4. Les parties sont filtrées selon des critères simples (date, cadence, complétude).
5. Les informations essentielles sont sélectionnées.
6. Un fichier CSV final est généré pour l’analyse ou la visualisation.

Cette approche permet de garder un contrôle total sur le volume de données traité.

---

## Notebook principal

Le notebook suivant contient l’ensemble du processus d’extraction :

- `Extraction lichess.ipynb`

Il regroupe :
- la lecture du fichier brut
- le filtrage des parties
- la sélection des variables
- la création du fichier CSV final

---

## Variables extraites

Le notebook permet d’extraire et de construire notamment les variables suivantes :

- `game_id` : identifiant unique de la partie
- `utc_date` : date de la partie
- `utc_time` : heure de début
- `time_control` : cadence de jeu
- `termination` : type de fin de partie
- `eco` : code d’ouverture
- `opening_name` : nom de l’ouverture
- `num_moves` : nombre de coups joués
- `white_elo` : classement du joueur avec les blancs
- `black_elo` : classement du joueur avec les noirs
- `elo_diff` : différence de classement
- `result` : résultat au format PGN
- `winner` : vainqueur de la partie (blancs, noirs ou nul)

Ces variables ont été choisies pour permettre une analyse simple
du déroulement et des résultats des parties.

---

## Sortie du processus

Le résultat de l’extraction est un fichier CSV :

- un fichier complet généré localement
- un fichier d’exemple (échantillon) partagé dans le repository

Le CSV final peut être utilisé dans des outils comme :
Excel, Google Sheets, Looker Studio ou tout outil de data visualisation.

---

## Remarque

Les données brutes complètes ne sont pas versionnées dans ce repository.
Seuls des exemples sont fournis afin d’illustrer le format des données
sans publier l’intégralité des fichiers sources.
