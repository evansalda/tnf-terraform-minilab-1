# Exercice 2

- Connectez-vous sur la [console AWS](https://689995499512.signin.aws.amazon.com/console) et créez un bucket S3 avec les caractéristiques suivantes :

    - Nom : nuumfactory-s3-import-2-XX (remplacez XX par votre digit)
    - Versioning : activé
    - Un tag nommé **imported** avec pour valeur **false**

- Déclarez dans votre fichier **main.tf** le bucket S3 que vous venez de créer, avec les mêmes caractéristiques sauf pour la valeur du tag imported où vous indiquerez **true**.

- Exécutez la commande **terraform init**.

- Exécutez la commande **terraform import \<adresse-ressource\> \<identifiant-ressource\>**. Notez que l’import se fait avec succès.

- Ouvrez le fichier **terraform.tfstate** que terraform vient de créer et constatez la présence du bucket S3. Notez également que la valeur du tag **imported** est **false**.

- Exécutez la commande **terraform plan** et analysez le plan d’exécution généré : Notez que terraform va modifier la valeur du tag imported pour qu’il corresponde à celle du code.

*N.B : Terraform va également ajouter la ressource aws_s3_bucket_versioning*.

- Exécutez la commande **terraform apply -auto-approve** et constatez que le tag **imported** est bien passé à **true**.

Supprimez le bucket S3 à l'aide de la commande **terraform destroy -auto-approve**.