# Exercice 1

- Connectez-vous sur la [console AWS](https://689995499512.signin.aws.amazon.com/console) et créez un bucket S3 avec les caractéristiques suivantes :

    - Nom : nuumfactory-s3-import-XX (remplacez XX par votre digit)
    - Versioning : activé
    - Un tag nommé **school** avec pour valeur **nuumfactory**

- Dans un fichier nommé **main.tf**, déclarez un bucket S3 avec les mêmes caractéristiques que celui que vous venez de créer manuellement.

- Exécutez la commande **terraform init**.

- Exécutez la commande **terraform import \<adresse-ressource\> \<identifiant-ressource\>** (dans le cas d’un bucket S3, l’identifiant est son nom) et assurez-vous d'obtenir le message **"Import prepared!"**.

- Ouvrez le fichier terraform.tfstate que terraform vient de créer et constatez la présence du bucket S3.

- Exécutez la commande **terraform plan** et analysez le plan d’exécution généré : Vous devriez avoir une ressource à ajouter. Il s'agit en effet de la resource dédiée au versioning du bucket qui bien que paramétré dans le bucket, doit être ajouté dans le tfstate.

- Exécutez la commande **terraform apply -auto-approve**.

Vous avez importé votre bucket S3 avec succès.

Supprimez le bucket S3 à l'aide de la commande **terraform destroy -auto-approve**.