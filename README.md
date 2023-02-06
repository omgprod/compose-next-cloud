# compose-next-cloud

- raspberry local nextcloud, gitlab

**HOW TO USE**

pre-requist:

```
sudo apt update && sudo apt upgrade
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo apt install docker-compose-plugin
```

installation : 

```
mkdir cloud/
```
```
cd cloud
```
```
mkdir ./nextcloud/{config,data,mariadb}
```
```
mkdir ./gitlab/{config,data,logs}
```
```
curl -o docker-compose.yaml https://raw.githubusercontent.com/omgprod/compose-next-cloud/main/docker-compose.yaml
```
```
docker-compose up -d
```
