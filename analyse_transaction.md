# Analyse d’une transaction Bitcoin sur TestNet4 : entrées, sorties, frais et UTXO

## 1. Introduction
Bitcoin utilise un modèle de transaction fondé sur les sorties de transactions précédentes. Une transaction consomme une ou plusieurs sorties disponibles et crée de nouvelles sorties. Ce mécanisme permet de suivre les unités dépensables sans tenir un simple solde de compte centralisé.

Cette étude utilise une transaction affichée sur l’explorateur Mempool.space pour Bitcoin TestNet4. TestNet4 est un environnement de test ; les unités utilisées dans cette étude ne représentent pas des bitcoins ayant une valeur monétaire réelle.

## 2. Présentation de la transaction
- **Identifiant (TXID) :** `e186efdf2bbda574efd5eb35d1f9071a1ddc52ac405700a5e80e810a62e423c2`
- **Explorateur :** https://mempool.space/testnet4/tx/e186efdf2bbda574efd5eb35d1f9071a1ddc52ac405700a5e80e810a62e423c2
- **État indiqué :** confirmée dans le bloc 144881.
- **Entrées :** une entrée de 0,00825474 BTC.
- **Sorties :** 0,00824333 BTC et 0,00001000 BTC.
- **Frais affichés :** 141 satoshis.
- **Taux de frais affiché :** 1,01 sat/vB.

Les valeurs ci-dessus proviennent de la page de l’explorateur consultée pour cette étude. Elles doivent être revérifiées sur le lien avant la remise.

## 3. Calcul des frais
Dans une transaction Bitcoin ordinaire, les frais correspondent à la différence entre la somme des entrées et la somme des sorties.

**Somme des entrées :**
0,00825474 BTC

**Somme des sorties :**
0,00824333 + 0,00001000 = 0,00825333 BTC

**Différence :**
0,00825474 − 0,00825333 = 0,00000141 BTC

Un bitcoin correspond à 100 000 000 satoshis. Donc :
0,00000141 × 100 000 000 = **141 satoshis**.

Le calcul correspond aux frais affichés par l’explorateur. Cela illustre comment les frais peuvent être vérifiés à partir des montants de la transaction.

## 4. Comprendre les entrées et les sorties
### Entrée (input)
L’entrée fait référence à une sortie créée par une transaction antérieure. Elle indique quelle sortie est dépensée et fournit les données nécessaires pour satisfaire les conditions de dépense de cette sortie.

### Sorties (outputs)
Une transaction peut créer plusieurs sorties. Dans cet exemple, les deux sorties ont des montants différents. L’une peut correspondre au paiement destiné au bénéficiaire et l’autre à une autre destination, par exemple une sortie de monnaie rendue. Toutefois, sans analyse supplémentaire des scripts et du contexte des adresses, il ne faut pas affirmer avec certitude laquelle correspond à quel rôle.

## 5. Le rôle des UTXO
UTXO signifie *Unspent Transaction Output*, soit une sortie de transaction non dépensée. Une sortie qui n’a pas encore été dépensée peut servir d’entrée à une transaction ultérieure. Lorsqu’une sortie est dépensée, elle ne peut pas être dépensée une seconde fois dans la chaîne valide.

Le portefeuille Bitcoin calcule le montant disponible à partir des UTXO qu’il contrôle. Il ne s’agit donc pas simplement d’un solde stocké dans un compte comme dans une base de données bancaire classique.

## 6. Confirmation et frais
L’explorateur indique que la transaction a été confirmée dans un bloc. Une confirmation signifie que la transaction a été incluse dans un bloc de la chaîne. Les frais servent d’incitation économique aux mineurs pour inclure les transactions ; leur niveau peut varier selon la taille de la transaction et la demande du réseau.

## 7. Conclusion
L’analyse montre que les montants d’une transaction Bitcoin peuvent être contrôlés à partir des entrées, des sorties et des frais. Dans cet exemple, la différence entre l’entrée et les deux sorties est de 141 satoshis, ce qui correspond au montant de frais affiché. La notion d’UTXO explique comment les sorties non dépensées deviennent les entrées de transactions futures.

## 8. Limites
Cette étude porte sur une transaction unique et sur les données présentées par un explorateur public. Elle ne permet pas d’identifier les personnes derrière les adresses ni de conclure avec certitude à la finalité économique de chaque sortie. Les données doivent être vérifiées au moment de la remise.

## Sources
1. Mempool.space, transaction TestNet4 : https://mempool.space/testnet4/tx/e186efdf2bbda574efd5eb35d1f9071a1ddc52ac405700a5e80e810a62e423c2
2. Bitcoin Developer Guide, “Transactions” : https://developer.bitcoin.org/devguide/transactions.html
3. Mempool.space, API REST TestNet4 : https://www.mempool.space/testnet4/docs/api/rest

## Vérification des résultat
Les montants des entrées et des sorties ont été comparés. La différence entre les deux correspond aux frais de transaction affichés par l’explorateur. Cette vérification permet de contrôler la cohérence arithmétique des données étudiées.
3.
