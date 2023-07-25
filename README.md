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
docker exec -it sonarqube sh
docker exec -it postgresql-sonarqube bash
```

## Informations

### Sonarqube

- Aucun fichier de configuration est nécessaire, Sonarqube permet de configurer les principales fonctionnalités depuis l'interface web.

- Certaines variables d'environement utilisées sont stockées dans le fichier `./.secrets/sonarqube.env` sur l'hôte.

- Les données persistantes sont dans les dossiers
  - `./sonarqube_data`
  - `./sonarqube_extensions`
  - `./sonarqube_logs`

### Postgresql

- La seule variable d'environement utilisée est stockée dans un "secrets" dans le dossier `./.secrets/` sur l'hôte.

- Les données persistantes sont dans le dossier `./postgresql_data` sur l'hôte.
