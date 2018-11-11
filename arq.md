# Arq

Arq est un logiciel de sauvegarde pour mac et windows. 
L'application et plutôt  orientée sauvegarde de post utilisateurs.

Elle permet de faire des sauvegardes vers de multiple destination. Vers des services de cloud public ou des serveurs personnels.

Le service fait des sauvegardes automatiques avec un versionning toutes les heurs ou tous les jours selon le besoin.
Il est ensuite possible de récupérer une version d'un fichier spécifique en revenant sur les sauvegardes effectuées.

Il est possible de spécifier des réseaux sur lesquels faire la sauvegarde explicitement, ou de ne faire la sauvegarde qu'en mode AC. Limiter la bande passante, ou inclure de partages réseaux lors de la sauvegarde.

#### Aperçu de quelques services compatible

![1541954622471](/home/joel/Switchdrive/HEIG/S-5/AIT/Labos/presentation/img/1541954622471.png)

## Configuration

Description et illustration de la configuration pour faire les backups vers AWS S3 et Glacier.

- Après l'installation de Arq, choisir de faire la sauvegarde sur AWS S3 et Glacier.

![1541410845677](./img/1541410845677.png)

- Récupérer les clés de connexions depuis le compte amazone :
  L'administrateur aura créé l'utilisateur IAM depuis la plateforme Amazone.

![1541412469247](./img/1541412469247.png)

- Choisir un nom de bucket et configurer le lieu de sauvegarde des données :

  ![1541412572934](./img/1541412572934.png)

- Créer une nouvelle sauvegarde

  ![1541412913726](./img/1541412913726.png)

- Choisir le type de service a utiliser.
  ![1541413012893](./img/1541413012893.png)

- Choisir un mot de passe
  ![1541413171238](/home/joel/.config/Typora/typora-user-images/1541413171238.png)

- écrire le mot de passe sur un bout de papier

  ![1541413259930](./img/1541413259930.png)

- Arq fera la sauvegarde une fois par heure
  ![1541413373193](./img/1541413373193.png)



- Par défaut Arq sauvegarde tout le disque C:\ de l'ordinateur. Il est possible de customiser les données qui vont être sauvée afin de ne garder que les informations importantes.

  ![1541413531500](./img/1541413531500.png)



- il est ensuite possible de restaurer les données en choisissant exactement de fichier dans une sauvegarde spécifique.

  ![1541414610402](./img/1541414610402.png)

