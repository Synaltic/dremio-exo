# Dremio : Appropriation Couches Sémantiques

Ce référentiel est maintenu par Synaltic.
http://synaltic.fr

Nous avons souvent blogué autour de Dremio
https://www.synaltic.fr/blog/category/dremio

Ici, il s'agit de fournir une configuration minimale pour aider à la découverte de Dremio et ses couches sémantique.

# contenu

La stack est simpliste :
une base de données PostgreSQL, Dremio, un fichier JSON.
A la fin il s'agit de fédérer les données, construire et structurer les couches de données à des fins d'analyses.

```
├── data
│   ├── postgres-docker
│   │   ├── db
│   │   │   └── university-session1.sql
│   │   └── Dockerfile
│   └── uni2.json
├── docker-compose.yml
└── README
```

# Obtenir ce référentiel

vous pouvez rapatrier ce référentiel

```
git clone https://github.com/Synaltic/dremio-exo.git
```

# Lancement de la stack

Pour lancer la stack il vous faut docker, docker-compose.
Depuis le dossier où vous avez tiré le référentiel :

```
docker-compose pull
docker-compose up --build --no-start
docker-compose start
```

ouvrir http://localhost:9047

# Comprendre Dremio

Avant de vous lancer parcourez par exemple Dremio Université
https://university.dremio.com/

- **D101 - Dremio Fundamentals**
  - https://university.dremio.com/courses/course-v1:dremio+D101+2018D101/about
- **D103 - Dremio for Data Consumers**
  - https://university.dremio.com/courses/course-v1:dremio+D103+2019/about

# Objectif du didacticiel

A partir de la source de données PostgreSQL et du fichier JSON, il est question de construire des vues pour obtenir des couches sémantiques facilitant l'analyse des données à des utilisateurs métiers et consommateurs de données dites applicatives.
