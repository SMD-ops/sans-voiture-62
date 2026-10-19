# Chaîne de calcul

Déposer ici les scripts du dossier `code/` du paquet `sans_voiture_62_v1-0`.

Ordre d'exécution : `build_graph.py` (graphe BD TOPO), `carreaux.py`, `access_walk.py` (marche et vélo), `build_conn.py`, `stops_walk.py`, `run_tc.py` et `csa.py` (transports en commun), `combine.py`, `detour.py`, `car.py`, `lieux.py`, `prospective.py`, puis les scripts des planches (`p*.py`), des fiches (`fiches.py`) et du GeoPackage (`gpkg_build.py`).

Les chemins d'accès aux données brutes sont à adapter. Les données brutes ne sont pas versionnées : elles se téléchargent auprès de l'INSEE, de la Géoplateforme IGN et des réseaux de transport.
