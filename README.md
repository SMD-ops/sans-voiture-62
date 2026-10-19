# Sans voiture, que reste-t-il ?

Un indicateur de dépendance à la voiture pour les besoins essentiels du quotidien. Étude pilote sur le Pas-de-Calais, octobre 2026.

- Carte interactive : https://VOTRE-COMPTE.github.io/sans-voiture-62/
- Atlas de 13 planches (PDF) et GeoPackage des résultats : page [Releases](../../releases) du dépôt

## L'indicateur

Pour chaque carreau habité de 200 m, l'indicateur compte combien des huit besoins du panier sont accessibles sans voiture : commerce alimentaire, boulangerie, médecin généraliste, pharmacie, école élémentaire, collège, bureau de poste ou France Services, pôle d'emploi.

Un besoin est accessible s'il est atteint en 15 minutes à pied, ou en 30 minutes porte-à-porte en transport en commun (45 minutes pour le pôle d'emploi), un mardi ordinaire. La marche suit les rues et chemins de la BD TOPO et tient compte de la pente. Les temps en transport en commun sont des médianes sur les départs du mardi 17 novembre 2026, marche et attente comprises.

| Catégorie | Besoins accessibles sans voiture | Part des habitants |
| --- | --- | --- |
| Autonome sans voiture | 8 sur 8 | 41 % |
| Largement autonome | 5 à 7 | 26 % |
| Partiellement dépendant | 1 à 4 | 24 % |
| Captif de la voiture | aucun | 9 % |

Dans le Pas-de-Calais, 123 000 habitants ne peuvent satisfaire aucun des huit besoins sans voiture. Le vélo, le vélo à assistance électrique et la marche lente d'une personne âgée sont traités en couches complémentaires, hors indicateur principal.

## Contenu du dépôt

| Élément | Contenu |
| --- | --- |
| `index.html` | Carte interactive, en un seul fichier avec ses données. Elle fonctionne hors ligne ; les fonds IGN et la recherche à l'adresse demandent une connexion. |
| `code/` | Scripts Python de la chaîne de calcul |
| Releases | Atlas PDF et GeoPackage `sans_voiture_62_v1-0.gpkg` |

## Données sources

Toutes les données utilisées sont publiques.

- INSEE : Filosofi 2021 (carreaux de 200 m), Base permanente des équipements 2025, recensement 2022 à l'IRIS, aires d'attraction des villes 2020.
- IGN : BD TOPO (édition du 15/09/2026), RGE ALTI, BD ORTHO, Plan IGN et service de géocodage de la Géoplateforme.
- Horaires GTFS de 16 réseaux : TER Hauts-de-France, réseaux régionaux du Pas-de-Calais, du Nord et de la Somme, Tadao, Artis, Mouvéo, Sitac, Marinéo, CA2BM, DK'Bus et Évéole.

## Limites

- Pour 17 % des habitants, les effectifs du carreau sont des valeurs imputées par l'INSEE (carreaux de moins de 11 ménages). La catégorie, qui dépend du lieu, n'est pas affectée.
- Le transport à la demande et les navettes ne figurent pas dans les données ouvertes. Le réseau Ilévia (métropole lilloise) n'a pas pu être intégré.
- Les horaires d'ouverture et la capacité des équipements ne sont pas connus.
- Les résultats portent sur un seul jour de référence, le mardi 17 novembre 2026, en période scolaire.

## Licence

Les résultats, la carte et l'atlas sont diffusés sous [Licence Ouverte 2.0](https://www.etalab.gouv.fr/licence-ouverte-open-licence/) (Etalab). Les données INSEE et IGN utilisées sont publiées sous la même licence. Chaque flux GTFS a sa propre licence, à consulter auprès du réseau concerné.

## Réalisation

SMD, octobre 2026.
