# compose-next-cloud

- raspberry local nextcloud, local gitlab

**HOW TO USE**

- install : 

mkdir cloud/

cd cloud

mkdir ./nextcloud/{config,data,mariadb}

mkdir ./gitlab/{config,data,logs}

curl -o docker-compose.yaml https://raw.githubusercontent.com/omgprod/compose-next-cloud/main/docker-compose.yaml
