# TD 4 Monnaie Numérique

## SSH setup (2 pts)

Pour cette étape il suffit de reproduire à l'identique ce qui a déjà été fait aux TD précédents et notamment au 1.

## UFW config (2 pts)

Pour le moment nous avons autorisé que le port 22 pour ssh, si besoin nous ferons d'autres adaptations.

## Installing dependencies (2 pts)

Dans un premier temps il faut installer le langage GO. 

L'installation la plus sipmle que nous ayons trouvé est la suivante :

```shell
sudo add-apt-repository ppa:longsleep/golang-backports
sudo apt update
sudo apt install golang-go
```
Neanmoins il semblerait que ce n'est pas une installation officielle, mais elle a fonctionné pour nous.

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

On place la commande ci dessus débutant avec "export" dans le dossier `~/.bashrc` et `~/.bash_profile` pour pouvoir lancer la commande `geth` a tout moment.

## Connect Geth to our group's private network (2 pts)

Pour initialiser geth avec notre fichier genesis on crée un dossier *ibftInit/* dans lequel on va créer et remplir **genesis.json**. On revient ensuite à la racine et on entre la commande suivante ``geth init --datadir data init ibftInit/genesis.json`` qui va alors créer un nouveau dossier *data/*. On observe qu'on obtient bien le résultat attendu avec la bonne database 'lightchaindata' et le bon hash.

***Insérer image ici***

on viendra mettre dans ce nouveau dossier *data/* le **static-nodes.json**.

Après s'être replacé un dossier avant la commande suivante à lancer est ``PRIVATE_CONFIG=ignore geth --datadir "./data"``. Il est recommandé de retirer *'nohup'* si cette commande est présente, en effet, elle empêche l'affichage des logs et on ne peut pas savoir tout de suite si nous nous sommes correctement connecté. Si tout se passe bien voilà ce qui devrait s'afficher :

***Image 1***

***Image 2***

Pour continuer il va falloir ouvrir une nouvelle console.

## Deploy a contract (2 pts)

## Installing Tessera (2 pts)

## Configure Tessera (3 pts)

## Create a private smart contract with
