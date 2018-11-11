Dans le cadre d'une entreprise de 50 personnes :  
- Prix ? 
  - Application Arq : 50$ / post

  - Storage (AWS):

    - Les tarifs de AWS S3 (Glacier) change légérement suivant les régions choisies.

      Ici vous avez un exemple avec la régio USA Est :

  ![1541960230533](/home/zutt/Documents/sync/Heig/AIT/AIT/img/tarif.png)

  - Accès aux données (AWS) :

    - Les tarifs de AWS S3 (Glacier) change légérement suivant les régions choisies.

      Ici vous avez un exemple avec la régio USA Est :

    ![1541960449268](/home/zutt/Documents/sync/Heig/AIT/AIT/img/tarifAcces.png)

  - Les Tarifs de AWS étant définis à l'utilisation et ayant des tarifs spécifiques pour chaque action ceux-ci sont donc complexes, vous trouverez plus d'information ici : https://aws.amazon.com/fr/s3/pricing/

    Cependant ils restent totalement accéssible pour une entreprise de 50 personnes.

- Sécurité, confidentialité, fiabilité
  - Les sauvegardes sont chiffrée du côté application par Arq avec une passphrase choisie par l'utilisateur.
  - Les sauvegardes sont faites toutes les heures et peuvent être restaurée indépendamment.
  - Amazon permet de choisir une destination de sauvegarde dans un datacenter spécifique, il est donc possible de configurer arq pour faire une sauvegarde vers plusieurs destinations géographiques et donc avoir plusieurs copies des fichiers.
  - La fiabilité des sauvegardes restes propre à la fiabilité qu'offre Amazon. Pour son service AWS. Si celui-ci n'est plus disponnible les sauvegardes ne le sont plus également.
  - La sécurité de S3/Glacier est très complète, mais très complèxe. Cependant les configurations de bases suffisent généralement.

- Facilité d'utilisation 
  - Pour utilisateur
    - Une fois le logiciel Arq installé et configuré, l'utilisateur n'a rien à faire pour assurer que la sauvegarde soit effectuées. 
    - Le logiciel est relativement intuitif, il est donc facile pour un utilisateur de comprendre comment faire pour retrouver un fichier et le restaurer.
  - Pour administrateur
    - La mise en place des comptes et buckets AWS n'est pas très intuitive de par la compléxité d'AWS mais avec un tutoriel adapté cela reste rapide à mettre en place. La force d'AWS réside dans sont nombre infinie de configurations possible et une gestion de droits ultra personnalisable.
    - De pars le chiffrement des données par Arq vous ne verrez pas les données de vos utilisateurs, Cependant sur la page IAM vous pourrez vérifier la dernière date ou un utilisateur c'est connecté et à donc effectué un backup.

- Temps de backup, (création du backup, récupération)

  - Le temps de backup est relatif à la bande passante d'ont on dispose, et de la quantité de donnée à sauvegarder.

- Déploiement du logiciel (Administrateur)
  - facilité d'installation
    - L'installation du logiciel est relativement intuitive il est donc possible de faire une documentation simple et de demander à chaque employé de faire l'installation par lui même. 
    - Au niveau de la configuration des comptes sur AWS cela peut prendre un peu de temps mais n'as besoin d'être fait qu'une fois pour chaque utilisateur. Une fois que compté créé et les clés d'authentification récupérées. Le logicile va faire le travail de création de l'espace de stockage d'ont il a besoin lui même.
    - disponible pour MacOS 10.7+ et Windows 7+ (.NET 4.5.1+)
  - Monitoring (voir l'utilisation des clients)
    - AWS permet via IAM de vérifier la dernière connection d'un client
    - AWS permet via IAM de gérer les droits des groupes et des utilisateurs de manière très précise et permet de créer ses propre "policy". Par contre cela nécéssite une bonne connaissance dans les outils AWS.
  - automatisation
    - La sauvegarde est entièrement automatique et ne demande aucune intervention humain.

- Support technique

  - AWS propose pour tout ses services un support technique performant et complet.
    - https://console.aws.amazon.com/support/home#/?nc2=h_l2_su
  - Arq ne propose pas de support technique à pars une adresse email de contacte.
    - [support@arqbackup.com](mailto:support@arqbackup.com)

- Scalabilité

  - S3 / Glacier étant du cloud, ces services s'adapte à votre utilisation (le tarif aussi), ils supportement sans problème la charge.

- Documentation

  - AWS s3 propose une document complète mais assez complexe.
    - glacier : https://docs.aws.amazon.com/glacier/index.html#lang/fr_fr
    - S3 : https://docs.aws.amazon.com/s3/index.html#lang/fr_fr
  - Arq possède une documentation complète
    - https://www.arqbackup.com/docs/arqbackup/