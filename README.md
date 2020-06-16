# DIND Secure env

## Before running the project
You will have to first generate the your certificats and copy it in the appropriate folder with the commands :
```bash
openssl req -newkey rsa:4096 -nodes -keyout ./certs/registry.pem -x509 -days 365 -out ./certs/registry.crt -subj "/C=''/ST=''/L=''/O=''/OU=''/CN=registry"
cp ./certs/registry.crt ./certs.d/registry\:5000/ca.crt
```

## To run the project

You can run the project with docker-compose :
```bash
docker-compose up -d
```

To make sure that all is up and running try seeing the current versino of your docker :
```bash
docker exec -it docker-client docker version
```