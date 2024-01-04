# Keycloak Image for Raspberry Pi

For more information, see the [Running Keycloak in a container guide](https://www.keycloak.org/server/containers).

## Build the image

It is possible to download the Keycloak distribution from a URL:

To build the image from a Raspberry Pi environment

    docker build --build-arg KEYCLOAK_DIST=http://<HOST>:<PORT>/keycloak-<VERSION>.tar.gz . -t <YOUR_TAG>

To build the image from a non-Raspberry PI environment

    docker buildx build --platform linux/arm/v7 --build-arg KEYCLOAK_DIST=http://<HOST>:<PORT>/keycloak-<VERSION>.tar.gz . --push -t <YOUR_TAG>
