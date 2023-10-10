# Exercice 3

- Connectez-vous sur la [console AWS](https://689995499512.signin.aws.amazon.com/console) et créez un bucket S3 avec les caractéristiques suivantes :

    - Nom : nuumfactory-s3-import-XX (remplacez XX par votre digit)
    - Versioning : activé
    - Un tag nommé **school** avec pour valeur **nuumfactory**

- Dans un fichier nommé **main.tf**, déclarez un bucket S3 avec les mêmes caractéristiques que celui que vous venez de créer manuellement.

En vous appuyant sur la [documentation officielle de terraform](https://developer.hashicorp.com/terraform/language/import), utilisez le bloc **import{}** pour importer le bucket S3 nuumfactory-s3-import-XX.