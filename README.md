# Portfolio Data Analyst — Mouniratou Ouedraogo

Étudiante en master Ingénieur commercial, option Data Management
(Haute École Francisco Ferrer, Bruxelles).

**Recherche un stage de data analyst / business analyst — 4 à 6 mois, disponible dès janvier 2027.**

**Outil utilisé :** Power BI Desktop — modélisation relationnelle, mesures DAX, colonnes calculées, tableaux de bord interactifs

---

## Stop Churn 360 — Analyse des résiliations en assurance auto

![Tableau de bord Stop Churn 360](Dashboard%20Churn%20_Mouniratou%20Ouedraogo.webp)

### Le problème

AutoProtect, assureur auto de 5 000 contrats, perd ses clients sans savoir
lesquels ni pourquoi. Aucun dispositif ne permet d'anticiper les résiliations
ni de cibler les clients à risque.

### Les données

Jeu de données simulé de 5 000 clients et contrats : âge, canal de
souscription, ancienneté, prime annuelle, sinistres sur douze mois,
statut de résiliation.

### La démarche

- Modèle Power BI à deux tables (Clients, Contrats) avec relations
- Mesures DAX : taux de churn, contrats résiliés, taille du portefeuille
- Tableau de bord filtrable par canal, avec analyse par âge et par sinistralité
- Business case complet : cadrage, KPI SMART, gouvernance RGPD, recommandations

### Les résultats

| Indicateur | Valeur |
|---|---|
| Portefeuille | 5 000 contrats |
| Contrats résiliés sur l'année | 1 079 |
| Taux de churn global | **21,58 %** (marché : 12 à 15 %) |
| Canal agence | **30,02 %** |
| Canal téléphone | 20,25 % |
| Canal en ligne | 17,22 % |

**Le canal explique le churn ; la sinistralité, non.** L'agence perd près de
deux fois plus de clients que le canal en ligne. En revanche, le taux reste
stable entre 21 % et 22 % quel que soit le nombre de sinistres — ce n'est donc
pas un facteur discriminant. L'âge, lui, joue : 24,4 % chez les 18-30 ans
contre 19,8 % chez les 51-60 ans.

**Recommandation :** concentrer l'effort de rétention sur le réseau physique —
formation des agents à l'explication des hausses tarifaires, offres de
fidélisation ciblées — plutôt que sur le produit.

### Ce que j'ai appris

En affichant les étiquettes de données sur mes graphiques, j'ai constaté que
ma conclusion initiale — « le churn augmente après deux sinistres » — n'était
pas soutenue par les chiffres : l'écart entre les tranches était d'un point,
c'est-à-dire du bruit. J'ai corrigé l'analyse.

J'ai également découvert que la colonne des primes annuelles contenait des
valeurs corrompues, de l'ordre de plusieurs milliards d'euros par contrat.
J'avais d'abord tenté de les rééchelonner par une formule, avant de comprendre
qu'un diviseur constant ne peut pas corriger deux types d'erreurs différents :
le problème venait du type de données à l'import. J'ai donc retiré les montants
en euros du tableau de bord plutôt que de publier des chiffres non fiables.

### Limites

- Jeu de données simulé, non issu d'un portefeuille réel.
- Les montants en euros ont été écartés : la colonne des primes contient des
  valeurs aberrantes. Les taux, calculés sur une colonne saine, ne sont pas
  affectés.
- Le scoring prédictif (régression logistique) est spécifié dans le rapport
  mais n'est pas implémenté. C'est la suite du projet.

📄 [Rapport complet (PDF)](Rapport%20Churn%20Mouniratou_OUEDRAOGO.pdf)

---

## Club Med — Performances commerciales des villages et des marchés

### La question

Quels villages et quels marchés nationaux génèrent le plus de valeur,
et qu'est-ce qui explique les écarts entre pays ?

### Les données

Réservations Club Med de 2023 à 2025 : clients, villages, durées de séjour,
nombre de personnes, prix.

### La démarche

- Modèle Power BI à cinq tables : Clients, Village, Réservations,
  CA annuel village, CA total annuel resorts
- Mesures DAX : chiffre d'affaires, panier moyen client, total des réservations
- Rapport en trois pages : vue séjours, vue client par marché, synthèse

### Les résultats

La Suisse génère la meilleure rentabilité du portefeuille. À volume de
réservations quasi identique à l'Allemagne, elle rapporte nettement plus,
et l'écart s'explique par la durée des séjours, sensiblement plus longue.

La Belgique affiche à l'inverse la plus faible rentabilité et les séjours
les plus courts, malgré un volume supérieur au Canada.

**Recommandation :** revoir l'offre sur le marché belge. Le volume est là,
la valeur par réservation ne suit pas.

### Ce que j'ai appris

À ne pas m'arrêter au premier chiffre. Deux pays avec le même nombre de
réservations peuvent avoir des rentabilités très différentes : c'est en
cherchant la variable qui explique l'écart — ici la durée de séjour — que
l'analyse devient utile à la décision.

### Limites

- L'année 2025 étant incomplète, sa comparaison avec 2023 et 2024 porte sur
  des périodes de longueur différente.
- L'hypothèse d'un pouvoir d'achat plus élevé côté suisse reste à vérifier :
  les données disponibles ne permettent pas de l'établir.

---

## Contact

📧 mounne1@gmail.com
