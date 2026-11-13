# Analyse d’une transaction Bitcoin sur TestNet4

**Auteur :** [BAHSAIN Mohamed]  
**Formation :** Master FinTech / Blockchain  
 TP3 — GitHub et projets blockchain

## 1. Question étudiée
Comment une transaction Bitcoin utilise-t-elle des entrées (inputs) et des sorties (outputs), comment calcule-t-on les frais, et quel est le rôle des UTXO ?

## 2. Démarche
Le projet examine une transaction visible sur l’explorateur public Mempool.space pour le réseau Bitcoin TestNet4. Les données présentées sont celles affichées par l’explorateur au moment de la consultation. Le réseau TestNet4 est un réseau de test : il ne faut pas confondre ses unités de test avec des bitcoins ayant une valeur monétaire réelle.

## 3. Résultat principal
La transaction étudiée comporte une entrée de **0,00825474 BTC de test** et deux sorties : **0,00824333 BTC** et **0,00001000 BTC**. La différence est de **0,00000141 BTC**, soit **141 satoshis**, ce qui correspond aux frais affichés par l’explorateur.

## 4. Livrable
Le fichier [`analyse_transaction.md`](analyse_transaction.md) présente les données, les calculs, l’interprétation et les limites de l’étude.

## 5. Outils utilisés
- Mempool.space TestNet4 : consultation des détails de la transaction.
- GitHub : publication et versionnement du projet.
- GitHub Desktop : commits et synchronisation du dépôt.
- Assistant d’intelligence artificielle : aide à la structuration et à la rédaction ; les données de transaction et les calculs doivent être vérifiés par l’auteur.

## 6. Sources
- Transaction étudiée : https://mempool.space/testnet4/tx/e186efdf2bbda574efd5eb35d1f9071a1ddc52ac405700a5e80e810a62e423c2
- Documentation Bitcoin Developer Guide — Transactions : https://developer.bitcoin.org/devguide/transactions.html
- Mempool.space — API REST TestNet4 : https://www.mempool.space/testnet4/docs/api/rest
Ce dépôt a été publié dans le cadre du TP3 GitHub et projets blockchain. BAHSAIN MOHAMED
