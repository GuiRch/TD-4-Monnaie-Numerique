# TD 4 Monnaie Numérique

## SSH setup (2 pts)

## UFW config (2 pts)

## Installing dependencies (2 pts)

Dans un premier temps il faut installer le langage GO. 

L'installation la plus sipmle que nous ayons trouvé est la suivante :

```shell
sudo add-apt-repository ppa:longsleep/golang-backports
sudo apt update
sudo apt install golang-go
```
Neanmoins il semblerait que ce n'est pas une installation officielle, mais elle a fonctionné pour nous 

Pour plus de détails voir : https://github.com/golang/go/wiki/Ubuntu

## Installing Quorum (2 pts)

Pour insatller Quorum on suit les instructions présentes dans le fichier `BUILDING.md` présent dans le dossier `quorum` de `quorum-21.7.1.tar.gz`

![build quorum](https://user-images.githubusercontent.com/62909821/136551001-7e422ddb-4c4f-4803-b314-381f7ab94f23.PNG)

Pour vérifier que tout est bien installer on lance la commande : 

```shell
export PATH=$PATH:/home/administrateur1/quorum/build/bin
geth version 
```

Si tout s'est déroulé correctement on obtient quelque chose du style :

![geth version path](https://user-images.githubusercontent.com/62909821/136555434-71d166fc-0d3f-4295-ace3-12961495a673.PNG)

On place la commande ci dessus dans le dossier `~/.bashrc` pour pouvoir lancer la commande `geth` a tout moment.

## Connect Geth to our group's private network (2 pts)

https://docs.goquorum.consensys.net/en/stable/Tutorials/Private-Network/Create-IBFT-Network/
Genesis file and static-node.json file attached below

## Deploy a contract (2 pts)

## Installing Tessera (2 pts)

## Configure Tessera (3 pts)

## Create a private smart contract with
