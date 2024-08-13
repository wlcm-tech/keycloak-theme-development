# Keycloak Theme Development

An example development environment setup to build Keycloak themes

## How to get started

### Spin up Keycloak

Start required container (keycloak+postgres) using the follow command:

`docker compose up -d` 

You can proof if the container is running with the command:

`docker ps` 

Access the Administration Console via `http://localhost:8080/`

You can also use the provided scripts to stop and start the container.

### (optional) Extract themes

This step is optional, although I strongly suggest extracting the themes from the container.
They are often the only reliable source on how things are implemented.

You can find a couple of helpful scripts in the scripts folder.

The jar can be extracted with this command:

`./scripts/exportThemes.sh`

## Use the Tailwind Example

Log in as admin. The .env file is not being used at the moment, therefore the values are hardcoded into the docker-compose.yml file

Create a realm called for example "test", then navigate into your realm as Admin

In the admin console you can go in your Realm settings to the "Themes" part. There you can choose the tailwind-example for your login screen and confirm it with "save".

Open the account page in a browser in order to see the theme in action:

`http://localhost:8080/realms/test/account`

You don't need to restart the container in order to see any changes to the templates

