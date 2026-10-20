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

Sources et licences

## Données sources

Toutes les données utilisées sont publiques.

- INSEE : Filosofi 2021 (carreaux de 200 m), Base permanente des équipements 2025, recensement 2022 à l'IRIS, aires d'attraction des villes 2020.
- IGN : BD TOPO (édition du 15/09/2026), RGE ALTI, BD ORTHO, Plan IGN et service de géocodage de la Géoplateforme.
- Horaires GTFS de 16 réseaux : TER Hauts-de-France, réseaux régionaux du Pas-de-Calais, du Nord et de la Somme, Tadao, Artis, Mouvéo, Sitac, Marinéo, CA2BM, DK'Bus et Évéole.
  
## Licences du dépôt

Le code, la note technique et les résultats agrégés (planches de l'atlas, tableaux, fiches intercommunales) sont publiés sous Licence Ouverte 2.0.

Le GeoPackage, les fichiers de connexions et la carte interactive (index.html) contiennent des données dérivées des horaires de transport en commun. Quatre des seize réseaux utilisés les publient sous ODbL 1.0, qui impose le partage à l'identique : ces fichiers sont donc diffusés sous ODbL, y compris pour la part issue des autres réseaux. Le fichier LICENCE.txt détaille le périmètre de chaque licence.
Données sources

Les fichiers d'origine ne sont pas redistribués. Chaque jeu reste soumis à la licence de son producteur.
Donnée 	Producteur 	Licence
BD TOPO, RGE ALTI, Plan IGN, BD ORTHO, géocodage 	IGN, Géoplateforme 	Licence Ouverte 2.0
Filosofi 2021 carroyé, BPE 2025, recensement 2022, IRIS 	Insee 	Licence Ouverte 2.0
Aires d'attraction des villes 2020 	Insee 	Licence Ouverte 2.0

Horaires GTFS (jour de référence : mardi 17 novembre 2026). Licences relevées sur data.gouv.fr le 19 octobre 2026.
Réseau 	Producteur du jeu 	Licence
Tadao 	Tadao 	ODbL
Sitac (Calais) 	Zenbus 	ODbL
Évéole (Douaisis) 	Évéole 	ODbL
DK'Bus (Dunkerque) 	Communauté urbaine de Dunkerque 	ODbL
Mouvéo 	Communauté d'agglomération du Pays 	Licence Ouverte 2.0
Marinéo 	Communauté d'agglomération du Boulonnais 	Licence Ouverte 2.0
CA2BM 	Communauté d'agglomération de Béthune-Bruay 	Licence Ouverte 2.0
Réseau routier régional, Nord (59) et Somme (80) 	Région Hauts-de-France 	Non renseignée
Artis (Arras) 	Communauté urbaine d'Arras 	Non renseignée
Réseau routier régional, Pas-de-Calais (62) 	Région Hauts-de-France 	[à confirmer]
TER Hauts-de-France 	[à confirmer] 	[à confirmer]

Les jeux dont la licence n'est pas renseignée n'ont fait l'objet d'aucune vérification auprès du producteur à la date indiquée.
Attribution

Pour les réseaux sous ODbL, la mention est : « Contient des données issues du réseau [nom], publiées sur transport.data.gouv.fr sous licence ODbL. »

Pour les autres données : « Source : IGN, Insee, producteurs des réseaux de transport. Traitement : SMD, 2026. »
Réutiliser les données dérivées
Toute base de données construite à partir du GeoPackage, des fichiers de connexions ou de index.html doit être publiée sous ODbL. Une carte, une image ou un graphique produit à partir de ces fichiers peut être diffusé sous une autre licence, avec la mention de la source et de la licence des données.

## Limites

- Pour 17 % des habitants, les effectifs du carreau sont des valeurs imputées par l'INSEE (carreaux de moins de 11 ménages). La catégorie, qui dépend du lieu, n'est pas affectée.
- Le transport à la demande et les navettes ne figurent pas dans les données ouvertes. Le réseau Ilévia (métropole lilloise) n'a pas pu être intégré.
- Les horaires d'ouverture et la capacité des équipements ne sont pas connus.
- Les résultats portent sur un seul jour de référence, le mardi 17 novembre 2026, en période scolaire.

## Réalisation

SMD, octobre 2026.
