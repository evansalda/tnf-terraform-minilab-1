# Exercice 1

- Connectez-vous sur la [console AWS](https://689995499512.signin.aws.amazon.com/console) et créez un bucket S3 avec les caractéristiques suivantes :

    - Nom : nuumfactory-s3-import-XX (remplacez XX par votre digit)
    - Versioning : activé
    - Un tag nommé **school** avec pour valeur **nuumfactory**

- Déclarez dans votre fichier **main.tf** le bucket S3 que vous venez de créer, avec exactement les mêmes caractéristiques.

- Exécutez la commande terraform import : **terraform import \<adresse-ressource\> \<identifiant-ressource\>** (dans le cas d’un bucket S3, l’identifiant est son nom).

- Ouvrez le fichier terraform.tfstate que terraform vient de créer et constatez la présence du bucket S3.

- Exécutez la commande terraform plan et analysez le plan d’exécution généré : Vous devriez avoir un warning et aucune action à réaliser, ou 1 ressource à ajouter. Rapprochez vous du formateur si vous avez besoin d’explications sur ce plan d’exécution.

- Exécutez la commande terraform apply -auto-approve.

Vous avez importé votre bucket S3 avec succès.