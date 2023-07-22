# SRV-Sonarqube

## Lancement du conteneur

```shell
docker compose up --build -d
```

## Arrêt du conteneur

```shell
docker compose down --remove-orphans
```

## Rentrer dans le conteneur

```shell
docker exec -it sonarqube bash
docker exec -it postgresql-sonarqube bash
```

## Informations

### sonarqube

- Fichier de configuration `/odoo.conf` doit être à la racine du dossier (attention il n'est pas dans le repo git car il est dans le .gitignore). Le fichier est lu automatiquement par le service dans le conteneur.

- Les données persistantes sont dans le dossier `./odoo_data` sur l'hôte.

### Postgresql

- La seule variable d'environement utilisée est stockée dans un "secrets" dans le dossier `./.secrets/` sur l'hôte.

- Les données persistantes sont dans le dossier `./postgresql_data` sur l'hôte.
