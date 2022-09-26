# easy-docker-registry
Spin up a Docker Registry with authentication and TLS encryption in a few seconds.

## authentication
```bash
sudo apt install apache2-utils -y
cd auth
htpasswd -Bc registry.password :username: # create password file, remove -c if you want to add more users
cd ..
```

## add SSL certificate
Do use the following naming convention for the certificate files:
```bash
nano cert/cert.pem # paste public key
nano cert/private.pem # paste private key
```

## hostname
```bash
nano .env # change the hostname to your domain
```

## start services
```bash
docker-compose up # add -D to run in background
```